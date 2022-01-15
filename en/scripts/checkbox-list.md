---
title: Create a form with a list of checkboxes
desc: The command creates a checkbox list form with one or more columns.
img:
   checkbox-list: scripts/checkbox-list.png
   checkbox-list-sample: scripts/checkbox-list-sample.png
html:
   checkbox-list: '<img src="%img.checkbox-list%" style="margin: 1em 1em;"/>'
   checkbox-list-sample: '<img src="%img.checkbox-list-sample%" style="margin: 1em 1em;"/>'
---
# Checkbox List

The **Checkbox List** command displays the array elements as a list with one or more columns. The user can check the desired records. Depending on the settings, items that are not checked will be automatically removed from the array or each item will be assigned a field with the value *true* (for selected items) or *false*.

%html.checkbox-list%

**Text**  
Specify the text that describes the displayed list and what actions will be performed on the selected items.

**Variable Name**  
Specify the name of an object variable that contains an array of strings or objects with a set of fields. If the variable contains an array of strings, in this case, the unselected elements will be removed from the array after the data is sent. If the variable contains objects with a set of fields, then it is possible to both remove unmarked items and add a field that stores the status of the element (marked or unmarked).

## Columns

If the variable object contains an array of objects with fields, then add columns that will display the values of the corresponding fields. When viewing the table, it can be sorted by any column.

**Value**  
Specify the name of the field that will be displayed in this column.

**Name**  
Specify the name of the column.

By default, unchecked items are removed from the array. If you don't want to delete items, you need to specify the name of the field that will contain the item status. Specify this field name first in the list of columns and leave **Name** blank. You can pre-assign *true* to the field so that the necessary records are marked. After the user submits the form, the value of this field will be *true* for marked records and *false* for unmarked ones. 

[%dwnsample%](/samples/checkbox-list-sample.yaml)

%scriptresult%

%html.checkbox-list-sample%
