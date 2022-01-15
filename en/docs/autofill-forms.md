---
title: Autofill Forms
desc: How autofill forms works in the Pro version.
img:
   autofill-forms-1: autofill-forms-1.png
   autofill-forms-2: autofill-forms-2.png
html:
   autofill-forms-1: '<img src="%img.autofill-forms-1%" style="margin: 1em 1em;"/>'
   autofill-forms-2: '<img src="%img.autofill-forms-2%" style="margin: 1em 1em;"/>'
---
# Autofill Forms

The Pro version of Eonza allows you to save values of the fields you specify in the forms when executing scripts. Password fields are not saved. To save the form fields, check the **Save Form Data** checkbox, which is displayed below all form elements.

%html.autofill-forms-1%

The next time you run the script, the previous values will be substituted in the form fields. Form data is saved separately for each user. The program can memorize several variants of values in the form. To do this, open additional fields and specify there the name for the current set of values you want to remember. 

%html.autofill-forms-2%

Subsequently, you can select the name of the value set from the drop-down list and the field values will be substituted in the form.

Forms with the same fields are considered different in different scripts and they separately store the saved sets of values. If you want the same forms to be considered different in one script, then define the **ref** parameter for them in [common settings](common-settings.html).

If you want to disable autofill fields, call the **SetSystemFlags** function in the **Source code** command.

```go
// Disable autofill
SetSystemFlags(0x10000000 | 0x0001)

// Enable autofill
SetSystemFlags(0x20000000 | 0x0001)
```
