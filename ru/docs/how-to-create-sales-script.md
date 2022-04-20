---
title: Как создать скрипт продаж или телефонный скрипт
desc: Как создать скрипт телефонный скрипт или скрипт продаж с помощью программы Eonza.
img:
   sales-script-page: scripts/sales-script-page.png
   sales-script-page-app: scripts/sales-script-page-app.png
   sales-script: scripts/sales-script.png
---
# Как создать скрипт продаж

Программа Eonza имеет специальные возможности для создания скриптов продаж или телефонных скриптов. Вы можете **бесплатно** создавать скрипты продаж и делится ими с другими людьми.

##  Шаг 1. Определите содержимое страниц скрипта

Для начала вы должны определить какие страницы будет содержать ваш скрипт. Для каждой страницы следует придумать заголовок и её содержимое. Также определите возможные варианты переходов с каждой страницы. Каждый вариант переходов должен ссылаться на другую страницу.

## Шаг 2. Создайте новый скрипт

Создайте новый скрипт в программе Eonza. В настройках скрипта укажите его имя и краткое описание.

## Шаг 3. Добавьте страницы скрипта

Для каждой страницы создaйте команду [Страница скрипта продаж](/ru/scripts/sales-script-page.html). Текст может быть в формате HTML или Markdown. Добавьте нужные варианты ответов указав имена страниц. Все варианты ответов будут отображаться в виде ссылок. Если пользователь нажимает на какой-то вариант, то он перейдёт на соответствующую страницу. Если вы оставите текст ссылки пустой, то будет отображаться имя или заголовок соответствующей страницы.

%html.sales-script-page%

## Шаг 4. Добавьте команду Скрипт продаж

После того, как вы на предыдущем шаге добавили команды для всех страниц, осталось добавить команду [Скрипт продаж](/ru/scripts/sales-script.html). В ней необходимо указать имя страницы, с которой будет начинаться скрипт продаж.

%html.sales-script%

Сейчас можно запустить готовый скрипт. Если вы хотите перенести его на другой компьютер, то экспортируйте скрипт. Для этого нажмите на кнопку Меню и выберите команду **Экспорт**. Для импорта следуеют воспользовать пунктом меню **Импорт**.

[%dwnsample%](/samples/demo-sales-script.yaml)

%scriptresult%

%html.sales-script-page-app%