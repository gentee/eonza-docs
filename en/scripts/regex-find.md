---
title: Find regular expression matches
desc: The command finds matches of a regular expression in the value of the variable
img:
   regex-find: scripts/regex-find.png
html:
   regex-find: '<img src="%img.regex-find%" style="margin: 1em 1em;"/>'
---
# RegEx - Find

The **RegEx - Find** command takes the value of the variable and finds the regular expression matches. The regular expression must conform to the [RE2](https://github.com/google/re2/wiki/Syntax) specification.

%html.regex-find%

**Variable Name**  
Specify a variable name to search for matches.

**Regular expression**  
Specify a regular expression. A regular expression can contain groups **(...)**. In this case, you will get additional values for each group.

**Find All Matches**  
By default, only the first match with a regular expression is searched. Click this checkbox if you want to find all regular expression matches.

**Result Variable**  
Specify the name of the object variable to which the array of found occurrences will be assigned. If you are looking for only the first match, then this variable will contain an array of strings. At the beginning there is a substring that matches the entire regular expression. If you have specified groups in a regular expression, then substrings for each group will follow. For example, you have the following text *my@eonza.org and your@eonza.com* and the resulting variable *ret*. Then, for a regular expression *(\w+)@(\w+)\.(\w+)* you get an array of strings

``` txt
// ret = [my@eonza.org my eonza org]
#ret[0]# => my@eonza.org.
#ret[2]# => eonza
```

If you search for all matches, the resulting variable will contain an array with information about each match. For the example above, you will get an array of two arrays of strings.

``` txt
// ret = [[my@eonza.org my eonza org] [your@eonza.com your eonza com]].
#ret[0][1]# => my
#ret[1][3]# => com
```
