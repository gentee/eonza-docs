---
title: Сохранить настройки SMTP сервера
desc: Команда сохраняет настройки SMTP сервера.
---
# SMTP сервер

**1.12.0**  
Команда **SMTP сервер** сохраняет указанные настройки для подключения к SMTP серверу в переменную. В дальнейшем, имя этой переменной необходимо указать в команде [Отправить письмо](send-email.html).

%html.smtp-server%

**Хост**  
Укажите хост SMTP сервера, который вы хотите использовать для отправки электронного письма.

``` txt
smtp.gmail.com
localhost
192.168.0.110
```

**Порт**  
Укажите порт для подключения к SMTP серверу. Если не указан, то будет использоваться *465* порт для SSL соединения и *25* в остальных случаях.

**Защита соединения**  
Укажите тип соединения.

* **Нет** - незащищенное соединение.
* **SSL/TSL** - безопасное соединение.

**Имя пользователя**  
Укажите имя пользователя для подключения к серверу. Как правило, оно совпадает с почтовым ящиком.

``` txt
eonza.dev@gmail.com
```

**Пароль**  
Пароль для подключения к серверу. В целях безопасности, не указывайте его явно.

**Результирующая переменная**  
Укажите имя переменной для хранения данных настроек.