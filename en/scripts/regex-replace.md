---
title: Replace regular expression matches 
desc: The command replaces all matches of the regular expression in the value of the variable.
img:
   regex-replace: scripts/regex-replace.png
html:
   regex-replace: '<img src="%img.regex-replace%" style="margin: 1em 1em;"/>'
---
# RegEx - Replace

The **RegEx - Replace** command takes the value of the variable and replaces all matches of the regular expression there. The regular expression must comply with the [RE2](https://github.com/google/re2/wiki/Syntax) specification.

%html.regex-replace%

**Variable Name**  
Specify a variable name to find and replace matches. By default, the result will be assigned to the same variable.

**Regular expression**  
Specify a regular expression. A regular expression can contain groups **(...)**. In this case, you can use the values ​​for each group in the replacement string.

**Replacement String**  
Specify the string to which all matches of the regular expression will be replaced. If the regular expression contains groups, then you can substitute their values ​​using **${i}**, where **i** is the group number starting from 1.

``` txt
Input: my@eonza.org
Regex: (\w+)@(\w+)\.(\w+)
Replacement: [${1}-x@${2}.com]
Result: [my-x@eonza.com]
```

**Result Variable**  
If you want to save the replacement result to another variable, specify its name here. By default, the result is assigned to the original variable.
