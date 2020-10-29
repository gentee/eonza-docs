---
title: Write JSON data into variable
desc: The command parses the JSON data and stores it in an object variable.
img:
   parse-json: scripts/parse-json.png
html:
   parse-json: '<img src="%img.parse-json%" style="margin: 1em 1em;"/>'
---
# Parse JSON

The **Parse JSON** command parses JSON data and stores it in an object variable.

%html.parse-json%

**JSON Data**  
Specify JSON data to be parsed. If you need to parse the json file, specify its name in angle brackets. Below are a few options for the definition of this parameter.

``` json
{
    "name": "Alex",
    "list": [
        {"id": 123, "value": "test"},
        {"id": 56, "value": "#value# #mark#"}.
    ]
}
```

``` txt
#jsonvar #
```

``` txt
</home/user/data/settings.json>
```

**Result Variable**  
Specify the name of the variable to which the object with JSON data will be assigned. You can use this variable in commands and functions to work with objects. You can also get field values directly. For example, if you specify the name of the variable *jsonobj*, you can get field values for the first example as follows:

``` txt
#jsonobj.name# => Alex
#jsonobj.list[0].value# => test
#jsonobj.list[1].id# => 56
```
