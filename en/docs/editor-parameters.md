---
title: Parameters page in Eonza editor
desc: Documentation for Parameters page in Eonza editor.
img:
   editor-parameters-1: editor-parameters-1.png
   editor-parameters-2: editor-parameters-2.png
   editor-parameters-3: editor-parameters-3.png
   editor-parameters-4: editor-parameters-4.png
   editor-parameters-5: editor-parameters-5.png
html:
   editor-parameters-1: '<img src="%img.editor-parameters-1%" style="margin: 1em 1em;"/>'
   editor-parameters-2: '<img src="%img.editor-parameters-2%" style="margin: 1em 1em;"/>'
   editor-parameters-3: '<img src="%img.editor-parameters-3%" style="margin: 1em 1em;"/>'
   editor-parameters-4: '<img src="%img.editor-parameters-4%" style="margin: 1em 1em;"/>'
   editor-parameters-5: '<img src="%img.editor-parameters-5%" style="margin: 1em 1em;"/>'
---
# Parameters

If you want to use the script in other scripts, you should often pass parameters to make the script more flexible. Here you can specify parameters that will be shown in the script card when called from other scripts.

* **Name** - parameter name. You can use it as a variable name in the Source code or in commands on the script tab (get the value - **#variable#**).  
* **Title** - the title of the parameter in the script card.
* **Type** - parameter type.
* **Advanced settings** - additional settings of the parameter as JSON object.

## Types of parameters

Parameter type | Control | Type in Source code | Additional settings
--------------|---------|---------------------|-------------
Checkbox | Checkbox | bool |
Multi-line text | Textarea | str |
Single line text | Input | str |
Select | Combobox | int/str | required
Number | Input | int |
List | Table | json | required

## Advanced settings

Additional settings must be specified as a JSON object.

* **required** - specify *true*, if the parameter must be defined. Otherwise, an error will be shown when compiling the script.
* **initial** - you can specify the initial value for input fields when the user inserts this script.

``` json
{"required": true, "initial": "Your name"}
```

* **default** - default value for the input field if the user left it empty.

``` json
{"default": "Unknown"}
```

* **optional** - specify *true* for [optional parameters](optional-parameters.html).
* **type** is the variable type for the *Select* parameter. Maybe *str* or *int*. By default, it will be of type *str*.
* **items** is the list of items for the *Select* parameter. Each item consists of two fields - *title* and *value*. The *title* field contains the name, and the *value* field contains the value of the parameter when this element is selected.

``` json
{"type": "str",
 "items":[
     {"title": "My Path", "value": "/home/user/mypath" },
     {"title": "Backup Path", "value": "/home/user/backup" },
 ]
}
```

* **list** - Description of the table columns for the *List* parameter. The *list* parameter allows the user to add several records to the table that will be processed by this script. Each *list* element consists of four fields - *name*, *title*, *type* and *options*. The *name* field specifies the column name, the *title* field specifies the column title, and the *type* field specifies the numeric field type (0 - checkbox, 1 - multi-line text, 2 - single-line text, 3 - combobox).The *options* field may contain additional settings, which are described in this section.

``` json
{"list": [
  {"name": "var", "title": "Variable name", "type": 2},
  {"name": "value", "title": "Value", "type": 1},
  {"name": "mode", "title": "Mode", "type": 3, "options": { "type": "str",
      "items": [
            {"title": "Debug", "value": "debug"},
            {"title": "Demo", "value": "demo"},
            {"title": "Release", "value": "release"}
         ]
      }}
   ]
}
```

* **output** - Array of strings. It is used if you want to display special text in *List* for checkboxes. For example, *not/yes*, *disagree/agree*, etc. The zero element corresponds to *false*, and the first element corresponds to *true*.

``` json
{"list": [
  {"name": "company", "title": "Company", "type": 2},
  {"name": "public", "title": "Public",
      "type": 0, "options": {"output": ["no", "yes"]}}
   ]
}
```

* **flags** - additional flags for parameters.
  
  * **preview** - This flag is used for parameters with *Multi-line text* type. If it is specified, you can switch to **Preview** mode when editing text. The text will be shown as HTML, Markdown or preformatted text, depending on the content of the current text.

## Example

As an example, let's create a simple script with parameters.

**Step 1.** Define one parameter with the *Single line text* type.

%html.editor-parameters-1%

**Step 2.** Let's add the output of this parameter to the Source Code using the function *Println*.

%html.editor-parameters-2%

**Step 3.** We also additionally display this parameter using the *Write To Console* command and save our script with the name *Parameters*.

%html.editor-parameters-3%

**Step 4.** Create a new script and add our script to it. Let's specify any value in the parameter input field.

%html.editor-parameters-4%

**Step 5.** Let's run this script and see two lines with our parameter in the console.

%html.editor-parameters-5%
