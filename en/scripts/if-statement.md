---
title: Run scripts when conditions are met
desc: The command only executes nested scripts when the specified conditions are true.
img:
   if-statement: scripts/if-statement.png
   sample-4-1: scripts/sample-4-1.png
   sample-4-2: scripts/sample-4-2.png
html:
   if-statement: '<img src="%img.if-statement%" style="margin: 1em 1em;"/>'
   sample-4-1: '<img src="%img.sample-4-1%" style="margin: 1em 1em;"/>'
   sample-4-2: '<img src="%img.sample-4-2%" style="margin: 1em 1em;"/>'
---
# If Statement

The **If Statement** command executes nested commands only if the specified conditions are met. To do this, you must specify the conditions to be checked and insert scripts inside it that must be executed when the specified conditions are true.

%html.if-statement%

* **Else Variable**  

This variable is used to define consecutive calls of conditional statements.

``` go
if condition ...
else if condition2 ...
else if condition3 ...
else...
```

To implement the above example, you need to create 4 *If Statement* with the same *Else variable*. If at least one of the condition commands is met, the rest of the commands will be skipped. If none of the conditions are met, then the last command will be executed, for which no conditions need to be specified.

## Conditions

You can specify one or more conditions.

**Variable name**  
Specify the name of the variable whose value will be used in the comparison. You can also specify fields and indexes of object variables or string values.

``` txt
varname
myobj.param
list[#item#]
This is #param#
```

**Negation of Condition**  
Click this checkbox when you want to negate the condition ( true => false, false => true).

**Comparison type**  
Select the comparison operation.

* **Equal**. Check if the variable is equal to the specified value. If the value is not specified, the result will be *true*, if the variable is not defined, equal to an empty string, zero or "false".
* **File/Dir Exists**. If the value of the variable is an existing file or directory, then the result is *true*. Otherwise, *false* will be returned. If the *Variable Name* is not specified, then the parameter *Value* will be checked.
* **Environment Exists**. Returns *true* if the environment variable exists. Otherwise, it returns *false*. The name of the environment variable is taken from the variable value. You can also leave the *Variable Name* field empty and specify the environment variable in the *Value* field.  
* **RegEx Match**. Check if the value of the variable matches the regular expression. Specify the regular expression in the *Value* field.
* **Starts With**. Returns *true* if the variable starts with the specified string.

**Value**  
The value to compare the variable with.

**Next Condition**  
You can specify a combination of two conditions.

* **AND** - this and the next condition must be true.
* **OR** - At least one of the two conditions must be true.

This field is not considered in the last condition. In the case of *AND* the checking of conditions stops when there is a false condition, in the case of *OR* the conditions are not checked after the true condition. You can combine both options. In this case, the OR operation has higher priority.

``` go
A1 AND A2 AND A3 OR A4 AND A5 => A1 AND A2 AND (A3 OR A4) AND A5
```

## If and Else

Let's take a closer look at how to execute a set of commands if our conditions turned out to be false. You can define one more command with the negation of our conditions, but in this case, these same conditions will be checked again, regardless of the result of the first conditional construction. To solve this problem, we must define *Else Variable* in the main conditional and then add another *If Statement* with the same *Else Variable*. You don't need to specify any conditions in it. In this case, all its commands are executed only when the conditions in the previous command with the same *Else Variable* have not been met.

[%dwnsample%](/samples/sample-4.yaml)

%scriptresult%

%html.sample-4-1%
%html.sample-4-2%
