---
title: Установить соединение с SQL сервером
desc: Команда устанавливает соединение с SQL сервером.
---
# SQL соединение

**1.12.0**  
Команда **SQL соединение** устанавливает соединение с SQL сервером и сохраняет идентификатор соединение в переменную.

%html.sql-connection%

**SQL сервер**  
Выберите тип SQL сервера - *MySQL* или *PostgreSQL*.

**Хост**  
Укажите хост SQL сервера, к которому вы хотите подключиться. Если не указан, то будет использоваться *localhost*.

``` txt
localhost
127.0.0.1
```

**Порт**  
Укажите порт для подключения к SQL серверу. Если не указан, то будет использоваться *3306* порт для *MySQL* и *5432* порт для *PostreSQL*.

**Имя пользователя**  
Укажите имя пользователя для подключения к серверу.

**Пароль**  
Пароль для подключения к серверу. В целях безопасности, не указывайте его явно.

**Имя базы данных**  
Укажите имя базы данных.

**Результирующая переменная**  
Укажите имя переменной, которой будет присвоен идентификатор соединения. Используйте это имя в поле **SQL соединение** в других командах для работы с базой данных.