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

## Advanced Settings

Here you can additionally specify general settings for the commands to be run.

**params**  
In the editor, you can only specify specific states for checkboxes and dropdown lists. There may be a situation where you want the value of a checkbox or drop-down list to be determined while the script is running. Open the script in the editor and look up the names of the corresponding parameters. After that specify the desired value in *params*. For example, if the name of the checkbox parameter is *recursive* and you want the checkbox to depend on the *mycheck* variable, specify

```yaml
params:
   recursive: "#mycheck#"
```

In this case it doesn't matter what state of the checkbox is specified in the script parameters below.

**log**  
By default, the script sets the logging level that is specified in its [settings](editor-settings.html). You can change the [logging level](logging.html) by specifying this parameter.

```yaml
log: disable
```

**ref**  
For each command you can specify an identifier name. The script contains a stack of such names and you can use these names to get information about which part of the script is currently running. For example, identifier names are used when [saving form data](autofill-forms.html) in the Pro version. If you show the same forms, but want to use different autocomplete form data, then specify for each form its own *ref* parameter.

```yaml
ref: form1
```

[%dwnsample%](/samples/sample-7.yaml)
