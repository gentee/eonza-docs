---
title: Convert text between different code pages
desc: The command converts text from one codepage to another.
img:
   convert-text: scripts/convert-text.png
html:
   convert-text: '<img src="%img.convert-text%" style="margin: 1em 1em;"/>'
---
# Convert Text

The *Convert Text* command converts text from one code page to another.

%html.convert-text%

**Variable Name**  
Specify the name of the variable that contains the source string.

**Source Encoding**  
Specify the encoding which corresponds to the source string.

* *utf-8*
* *Big5 (Chinese - traditional)*
* *cp437  (IBM PC US)*
* *cp866  (MS-DOS Cyrillic Russian)*
* *EUC-KR (Korean)*
* *GBK (Chinese - simplified)*
* *KOI8-R*
* *KOI8-U*
* *Shift JIS (Japanese)*
* *windows-1250 (Central European)*
* *windows-1251 (Cyrillic)*
* *windows-1252 (Western European)*
* *windows-1253 (Greek)*
* *windows-1254 (Turkish)*
* *windows-1255 (Hebrew)*
* *windows-1256 (Arabic)*
* *windows-1257 (Baltic)*
* *windows-1258 (Vietnamese)*

**Target Encoding**  
Specify the encoding to which you want to convert the text.

**Result Variable**  
Specify the name of the variable the result will be assigned to. If no variable name is specified, the resulting string will be assigned to the original variable.
