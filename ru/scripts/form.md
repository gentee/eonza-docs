---
title: Создать форму для ввода данных
desc: Команда создаёт форму для ввода данных
---
# Форма

Команда **Форма** позволяет показывать поля для ввода данных. Она дает возможность показывать поля ввода и чекбоксы в процессе выполнения скрипта. Каждый элеменет соответствует переменной и отображает её текущее значение. Пользователь может указать другие значения для соответствующей переменной.

%html.form%

## Элементы формы

Вы можете добавить в форму поля ввода и чекбоксы.

**Тип элемента**  
Укажите тип элемента формы

* **Однострочный текст**. Однострочное поле ввода.
* **Чекбокс**. 
* **Многострочный текст**. Многострочное поле ввода.

**Текст**  
Описание или наименование элемента формы.

**Имя переменной**  
Имя переменной привязанной к данному элементу. Если переменная определена, то элемент отоображает её текущее значение. После отправки формы переменная будет равна значению, которое указал пользователь.

[%dwnsample%](/samples/sample-3.yaml)

%scriptresult%

%html.sample-3-1%
%html.sample-3-2%