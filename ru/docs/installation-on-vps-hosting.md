---
title: Установка Eonza на VPS хостинг
desc: Как установить Eonza на VPS хостинг.
---
# Установка на VPS хостинг

Eonza - это обычный веб-сервер, который слушает определенный порт и имеет API. Таким образом, если у вас имеется VPS хостинг, то вы можете установить Eonza на сервер и управлять вашим хостингом из браузера. Рекомендуется дополнительно использовать *NGINX* или другой веб-сервер в качестве прокси-сервера. Рассмотрим пример установки Eonza на CentOS 64-bit с веб-сервером **nginx** и готовым доменным именем *my-eonza-domain.org*. Предположим, что на данном домене уже имеется веб-сайт, поэтому сделаем так, чтобы Eonza открывалась в браузере по адресу **https://my-eonza-domain.org:[port]**. При желании, вы можете настроить nginx для использования адреса *https://my-eonza-domain.org/eonza*.

## Шаг 1. Установка Eonza

На сервере создайте директорию, скачайте и сохраните в неё [дистрибутив программы](/downloads/linux-amd64/eonza) для Linux. Например, сохраним программу в директорию */home/eonza/*. Лучше сразу установить пароль для логина, для этого запустите программу с параметрами *-install* и *-psw*. В этом случае, Eonza создаст неообходимые файлы, установит пароль для логина и закончит работу.

``` txt
cd /home/eonza
./eonza -install -psw=mypassword 
```

## Шаг 2. Настройка Eonza

Выберите localhost порт для программы Eonza и внешний порт для прокси-сервера *nginx*. Откройте [конфигурационный файл](config.html) *eonza.yaml* в любом редакторе и укажите в разделе *http* следующие поля:

* *host* - имя хоста
* *port* - порт, который будет слушать программа.
* *open* - укажите *false*, чтобы программа не пыталась открыть Eonza в браузере на сервере.
* *access* - укажите *host*
* *jwtkey* - укажите случайную строку для создания JWT ключей.

Таким образом, настройки могут быть примерно такими

``` yaml
http:
    host: my-eonza-domain.org
    port: 5050
    open: false
    theme: default
    access: host
    jwtkey: my-secret-jwt-key
```

В целях безопасности, рекомендуется определить список "белых" ip-адресов и подсетей. В этом случае, все запросы с других ip-адресов будут игнорироваться. Вы можете указать подсети принадлежащие вашему провайдеру. Также, обязательно добавьте локальные подсети *::1/128* и *127.0.0.0/31*. "Белый" список ip-адресов и подсетей указывается в разделе *whiltelist*. Например,

``` yaml
whitelist:
    - ::1/128
    - 127.0.0.0/31
    - 92.140.108.0/24
    - 92.140.109.0/24
```

## Шаг 3. Создание systemd сервиса

Зарегистрируем программу Eonza в качестве сервиса. Для этого создадим файл **eonza.service** в директории **/usr/lib/systemd/system**. Ниже приведен самый простой вариант, хотя *.service* файл может иметь гораздо больше параметров.

``` ini
[Unit]
Description=Eonza Service

[Service]
ExecStart=/home/eonza/eonza
WorkingDirectory=/home/eonza

[Install]
WantedBy=multi-user.target
```

Запускаем и подключаем наш сервис. Eonza будет автоматически запускаться после перезагрузки системы.

``` txt
systemctl start eonza.service
systemctl enable eonza.service
```

Если вы измените файл eonza.service, то необходимо выполнить *systemctl daemon-reload* для обновления настроек. Для получения статуса сервиса используйте *systemctl status eonza.service* или *service eonza status*.

## Шаг 4. Настройка прокси-сервера

Использование *nginx* в качестве прокси-сервера, позволит подключить Eonza к существующему доменному имени по https протоколу. Предположим, что уже имеется веб-сайт https://my-eonza-domain.org с [Let’s Encrypt](https://letsencrypt.org) сертификатом и мы хотим, чтобы Eonza открывалась по адресу *https://my-eonza-domain.org:5040*. Для этого в файл настроек */etc/nginx/conf.d/my-eonza-domain.org.conf* добавьте следующий раздел:

``` txt
server {
    listen 5040 ssl;
    server_name my-eonza-domain.org;
    
    ssl_certificate /etc/letsencrypt/live/my-eonza-domain.org/fullchain.pem; 
    ssl_certificate_key /etc/letsencrypt/live/my-eonza-domain.org/privkey.pem;

    ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
    ssl_prefer_server_ciphers on;

    ssl_dhparam /etc/ssl/certs/dhparam.pem;
    ssl_ciphers 'ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-AES256-GCM-SHA384:DHE-RSA-AES128-GCM-SHA256:DHE-DSS-AES128-GCM-SHA256:kEDH+AESGCM:ECDHE-RSA-AES128-SHA256:ECDHE-ECDSA-AES128-SHA256:ECDHE-RSA-AES128-SHA:ECDHE-ECDSA-AES128-SHA:ECDHE-RSA-AES256-SHA384:ECDHE-ECDSA-AES256-SHA384:ECDHE-RSA-AES256-SHA:ECDHE-ECDSA-AES256-SHA:DHE-RSA-AES128-SHA256:DHE-RSA-AES128-SHA:DHE-DSS-AES128-SHA256:DHE-RSA-AES256-SHA256:DHE-DSS-AES256-SHA:DHE-RSA-AES256-SHA:AES128-GCM-SHA256:AES256-GCM-SHA384:AES128-SHA256:AES256-SHA256:AES128-SHA:AES256-SHA:AES:CAMELLIA:DES-CBC3-SHA:!aNULL:!eNULL:!EXPORT:!DES:!RC4:!MD5:!PSK:!aECDH:!EDH-DSS-DES-CBC3-SHA:!EDH-RSA-DES-CBC3-SHA:!KRB5-DES-CBC3-SHA';
    ssl_session_timeout 1d;
    ssl_session_cache shared:SSL:50m;

    ssl_stapling on;
    ssl_stapling_verify on;
    add_header Strict-Transport-Security max-age=15768000;

    location = /ws {
        proxy_pass http://127.0.0.1:5050/ws;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "Upgrade";
        proxy_set_header Host $host;
    }
    
    location / {
        if ($http_origin ~ '^https://my-eonza-domain.org') {
            add_header Access-Control-Allow-Origin "$http_origin";
        }
        access_log off;
        proxy_pass http://127.0.0.1:5050;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_redirect off;
    }
}
```

В параметре **proxy_pass** укажите порт, который использует Eonza. Сохраните файл настроек и перезапустите nginx (*service nginx restart*). Укажите в браузере *https://my-eonza-domain.org:5040* и если всё было настроено правильно, то вы увидите страницу логина программы Eonza.
