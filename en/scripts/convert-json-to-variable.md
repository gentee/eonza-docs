---
title: Convert JSON to Variable
desc: The script converts a JSON string into an object variable.
img:
   convert-json-to-variable: scripts/convert-json-to-variable.png
html:
   convert-json-to-variable: '<img src="%img.convert-json-to-variable%" style="margin: 1em 1em;"/>'
---
# Convert JSON To Variable

The **Convert JSON to variable** command converts JSON-formatted text to a variable object. 

%html.convert-json-to-variable%

**JSON Format Text**  
You can specify JSON data or the name of the variable that contains JSON string.

**Variable Name**  
Specify the name of the variable to which the created object will be assigned.

For example, if you specified the following JSON string

```json
{
  "name": "John Doe",
  "company": "My Company",
  "age": 36,
  "ids": [1,2,3]
}
```

and the name of the resulting variable is *user*, then accessing the fields of the variable will return the following values

```txt
#user.name# => John Doe
#user.age# => 36
#user.ids[1]# => 2
#user.ids# => [1,2,3]
```
