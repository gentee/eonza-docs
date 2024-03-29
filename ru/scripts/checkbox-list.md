---
title: Создать форму со списком чекбоксов
desc: Команда создаёт форму со списком чекбоксов с одной или несколькими колонками.
---
# Список чекбоксов

Команда **Список чекбоксов** показывает элементы массива в виде списка с одной или несколькими колонками. Пользователь может отметить нужные записи. В зависимости от настроек, элементы, которые не были отмечены будут автоматически удалены из массива, или каждому элементу будет присвоено поле со значением *true* (для выбранных элементов) или *false*.

%html.checkbox-list%

**Текст**  
Укажите текст, который описывает показываемый список и какие действия будут произведены с выбранными элементами.

**Имя переменной**  
Укажите имя переменной-объекта, которая содержит массив строк или объектов с набором полей. Если переменная содержит массив строк, то в этом случае, неотмеченные элементы будут удалены из массива после отправки данных. Если переменная содержит объекты с набором полей, то возможно как удаление ненужных записей, так и добавление поля, которое хранит статус элемента (отмечен или нет). 

## Колонки

Если переменная-объект содержит массив объектов с полями, то добавьте колонки, в которых будет отображаться значения соответствующих полей. При просмотре таблицы она может быть отсортирована по любому столбцу.

**Значение**  
Укажите имя поля, которое будет отображаться в этой колонке.

**Наименование**  
Укажите наименование колонки.

По умолчанию неотмеченные элементы удаляются из массива. Если вы не хотите удалять элементы, то нужно указать имя поля, которое будет содержать статус элемента. Укажите имя этого поля первым в списке колонок и оставьте **Наименование** пустым. Вы можете предварительно полю присвоить *true*, чтобы нужные записи были отмечены. После того, как пользователь отправил форму, значение этого поля будет равно *true* для отмеченных записей, а для неотмеченных - *false*. 

[%dwnsample%](/samples/checkbox-list-sample.yaml)

%scriptresult%

%html.checkbox-list-sample%
