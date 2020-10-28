---
title: Using variables and values in scripts
desc: How to use variables and their values in scripts.
---
# Variables and Values

As a rule, while the script is running, you need to store some values and get them when they are needed. Variables are used for this purpose. By default, the values of variables are stored as strings. You can assign values to variables using commands (e.g. [Set Variables](/scripts/set-variables.html)) or special functions. A variable name may consist of letters and numbers and must not contain service characters. Variable names are case-sensitive. For example, *MyName* and *myname* are different variables.

## Scope of visibility

The scope of the variable is limited by the script where it was defined. This is so that the scripts cannot influence each other. For example, you assigned the variable *name* the value *John* and called another script. This script also creates a variable with the same name *name* and value *Alex* for its purposes. If you do not limit the scope of the variables, in this case the value of your variable will change to *Alex*, which you would not want at all.

## Getting the values

To substitute a variable value in any field, just enclose the variable name between characters **#**. For example,
*#name#, #myValue#*. All found variable values will be substituted during parameter processing. Value substitution occurs during script execution and is performed recursively. Let us define the following variables:

``` go
firstname = "John"
lastname = "Doe"
name = "#firstname# #lastname#"
```

In this case, **Name: #name#** will return **Name: John Doe** because all nested values are recursively substituted. If no variable is found, the string remains unchanged. For example, if you specify *#name# #address#* for the above example, you will get **John Doe #address#** because the variable address does not exist.

Note that in fields like **Variable Name, Resulting Variable, Variable Index** etc. you only need to specify the variable names without *#* characters. You can only use *#varname#* if another variable (in this case *varname*) contains your variable name.

## Variable objects

Besides usual variables, there are variables that allow to store objects. Objects are necessary to work with JSON, YAML and similar data as well as to work with different lists. An object may contain values of the following types: **number, string, floating point number, logical value, array of objects and associative array of objects**. Different arrays are used to store the names of ordinary variables and object variables. If you specified *#myvar#*, then at the beginning there is a search among ordinary variables, if nothing is found, then an object with that name is searched. If the found object is a number, a string or a logical value, then its value will return, otherwise no substitution will occur and *#myvar#* will remain unchanged. To get the fields of an associative array, you can use square brackets or specify the name of the required field separated by a dot. In the case of a regular array, you need to use square brackets to get the element by its index. You can also use a substitution of values within square brackets. Suppose that the variable *myobj* contains the following data:

``` json
{
    "root": "/home/user",
    "index": 0,
    "app": "My Application",
    "files": [
        {
            "file": "myfile.txt",
            "size": 2543,
        },
        {
            "file": "test.txt",
            "size": 257,
        },
    ]
}
```

Then, when accessing the fields, the following values ​​will be returned

``` txt
#myobj# = #myobj#
#myobj.root# = /home/user
#myobj[app]# = My Application
#myobj.files[#myobj.index#].file# = myfile.txt
#myobj[files][1].size# = 257
```

## Reading files

If you want to get the content of a file as a value, you do not need to use the command to read the file beforehand. It is enough to specify the path to the file inside the angle brackets as a parameter. For example,

``` txt
<#mypath#/myfile.log>
<c:\temp\package.json>
<./data/settings.yaml>
```

Such parameter should not contain any additional text. Otherwise, it will be processed as plain text.
