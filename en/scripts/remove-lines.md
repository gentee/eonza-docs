---
title: Remove lines in the text
desc: The command removes lines that contain the specified substrings.
img:
   remove-lines: scripts/remove-lines.png
html:
   remove-lines: '<img src="%img.remove-lines%" style="margin: 1em 1em;"/>'
---
# Remove Lines

The **Remove Lines** command deletes lines in the text. The lines to be deleted must contain at least one of the specified substrings.

%html.remove-lines%

**Text**  
Specify the source text in which you want to remove lines. You can specify the variable name as *#varname#* or file
*<#path#\my.log>*.

**Remove lines that contain**  
The command removes lines that contain at least one of the substrings specified here. Substrings to check
are separated by line feed.

**Result variable**  
Specify the name of the variable in which the text with deleted strings will be written.
