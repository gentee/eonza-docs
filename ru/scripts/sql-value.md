---
title: Выполнить SQL запрос и получить значение колонки
desc: Команда выполняет SQL запрос и сохраняет значение колонки в переменную.
---
# SQL значение

Команда **SQL значение** выполняет SQL запрос для выбора данных и записывает значение первой колонки первой найденной записи в переменную.

%html.sql-value%

**SQL соединение**  
Укажите имя переменной с идентификатором SQL соединения. Эта переменная должна быть определена в команде [SQL соединение](sql-connection.html).

**Запрос SELECT**  
Укажите SQL запрос SELECT для получения колонки из базы данных. Если запрос найдет несколько записей, то возвратится значение первой колонки первой записи. Если запрос не найдет ни одной записи, то возвратится ошибка.

``` sql
select count(*) from #dbtable#
```

**Параметры**  
Рекомендуется использовать параметры при использовании значений в SQL запросе.

Например, при использовании этого запроса вам необходимо добавить один параметр. Вы можете использовать подстановку переменных *#varname#* в значениях параметрах.

``` sql
select company from #dbtable# where code = ?
```

``` txt
#code#
```

**Результирующая переменная**  
Укажите имя переменной, которой будет присвоено полученное значение. Если запрос возвратит запись с несколькими колонками, то возвратится значение первой колонки.

``` txt
#myname#
```
