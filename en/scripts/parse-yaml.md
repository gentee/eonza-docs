---
title: Write YAML data into variable
desc: The command parses the YAML data and stores it in an object variable.
img:
   parse-yaml: scripts/parse-yaml.png
html:
   parse-yaml: '<img src="%img.parse-yaml%" style="margin: 1em 1em;"/>'
---
# Parse YAML

The **Parse YAML** command parses YAML data and stores it in an object variable.

%html.parse-yaml%

**YAML Data**  
Specify YAML data to be parsed. If you need to parse a yaml file, then specify its name in angle brackets or read it into a variable beforehand. Below are a few options for the definition of this parameter.

``` yaml
name: Alex
list:
    - id: 123
      value: test
    - id: 56
      value: "#value# #mark#"
```

``` txt
#yamlvar#
```

``` txt
</home/user/data/settings.yaml>
```

**Result Variable**  
Specify the name of the variable to which the object with YAML data will be assigned. You can use this variable in commands and functions to work with objects. You can also get field values directly. For example, if you specify the name of the variable *yamlobj*, you can get field values for the first example as follows:

``` txt
#yamlobj.name# => Alex
#yamlobj.list[0].value# => test
#yamlobj.list[1].id# => 56
```
