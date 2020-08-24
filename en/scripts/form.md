---
title: Create a data entry form
desc: The command creates a form for entering data
img:
   form: scripts/form.png
   sample-3-1: scripts/sample-3-1.png
   sample-3-2: scripts/sample-3-2.png
html:
   form: '<img src="%img.form%" style="margin: 1em 1em;"/>'
   sample-3-1: '<img src="%img.sample-3-1%" style="margin: 1em 1em;"/>'
   sample-3-2: '<img src="%img.sample-3-2%" style="margin: 1em 1em;"/>'
---
# Form

The **Form** command allows you to show fields for data entry. It allows you to show input fields and checkboxes during script execution. Each element corresponds to a variable and displays its current value. The user can specify other values for the corresponding variable.

%html.form%

## Form controls

You can add input fields and checkboxes to the form.

**Control type**  
Specify the type of form element

* **Single text**. Single line input field.
* **Checkbox**.
* **Multi-line text**. Multiline input field.
* **Select**. Displays the combo box with your elements. They should be defined in the *Additional settings* field.
* **HTML Text**. It allows you to insert any HTML text into the form. In this case, the *Text* field remains empty, and the variable in the *Variable Name* field must contain HTML text.
* **Button**. Shows the button with the name from the *Text*  field. The form can have several buttons. Form data is sent when any of the buttons is clicked. Each button must have a specified variable name. When the button is pressed, the corresponding variable is assigned *true*, and an empty line is assigned to the other buttons' variables. You can assign any value to a variable. To do it, specify it in the **initial** field in *Advanced settings*. You can also define the **default** field to be *"true "* if you want to highlight the button with a color.

``` go
{
    "initial": "mybutton",
    "default": "true"
}
```

**Text**.  
Description or name of the form element.

**Variable name**  
The name of the variable bound to this element. If the variable is defined, then the element displays its current value. After submitting the form, the variable will be equal to the value specified by the user.

**Additional settings**  
Here you can specify additional settings for form elements. These are described in [Editor Parameters](/docs/editor-parameters.html).

[%dwnsample%](/samples/sample-3.yaml)

%scriptresult%

%html.sample-3-1%
%html.sample-3-2%
