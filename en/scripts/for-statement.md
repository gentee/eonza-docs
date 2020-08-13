---
title: Execute commands in a loop with a counter
desc: The command executes nested scripts while the counter changes from one value to another.
img:
   for-statement: scripts/for-statement.png
   sample-5-1: scripts/sample-5-1.png
   sample-5-2: scripts/sample-5-2.png
html:
   for-statement: '<img src="%img.for-statement%" style="margin: 1em 1em;"/>'
   sample-5-1: '<img src="%img.sample-5-1%" style="margin: 1em 1em;"/>'
   sample-5-2: '<img src="%img.sample-5-2%" style="margin: 1em 1em;"/>'
---
# For Statement

You can use this command for a loop in which the counter changes from one value to another and nested commands are executed every time the counter changes.

%html.for-statement%

**Initial value**  
Enter the initial counter value.

**Final value**  
Enter the final counter value. If it is lower than the initial value, the counter will decrease by 1.

**Index Variable**  
You can specify a variable name to get the current counter value. If no variable is specified, the counter name is *index*.

[%dwnsample%](/samples/sample-5.yaml)

%scriptresult%

%html.sample-5-1%
%html.sample-5-2%
