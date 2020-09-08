---
title: Common settings for running scripts
desc: Common settings for running scripts in Eonza.
img:
   common-settings: common-settings.png
html:
   common-settings: '<img src="%img.common-settings%" style="margin: 1em 1em;"/>'
---
# Common Settings

Each script has certain parameters, but you can also define the following general settings when calling the script.

**Description**  
You can specify here any comment or explanation that will help you to understand the script operation in the future.

**If Condition**  
If you need to perform some action when certain conditions are met, then you can specify these conditions in this field instead of using the [If Statement](/scripts/if-statement.html).

%html.common-settings%

## How to define the If Condition field

The If Condition field contains a logical expression in [Gentee language](https://docs.gentee.org/). The current command will only be executed if this condition is *true*. Otherwise, the current command will be skipped.

``` go
GetVarBool("check1") || *GetVar("value1") > 5
GetVarBool ("check1")
```

If you want to check only variables for true/false in the condition, you can use a simplified notation. In this case, it is enough to specify only the variable names and logical operations **&&(AND), ||(OR), !(NOT)**. For example, if you specify *myvar*, it means that this command will be executed if the variable *myvar* exists and is not equal to an empty string, "0" and "false". If you specify *!myvar*, then the command will be executed in the opposite case.

``` txt
check1 && isopen
!myvar || todo || myvar2
```

[%dwnsample%](/samples/sample-7.yaml)
