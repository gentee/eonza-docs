---
title: Encode and decode string in Base64
desc: The command can encode or decode Base64 string.
img:
   base64-encoding: scripts/base64-encoding.png
html:
   base64-encoding: '<img src="%img.base64-encoding%" style="margin: 1em 1em;"/>'
---
# Base64 Encoding

**1.13.0**  
The **Base64 Encoding** command encodes a regular string to a Base64 string, or decodes a Base64 string to a regular string.

%html.base64-encoding%

**Variable Name**  
Specify the name of the variable that contains the source string.

**Encoding**  
Specify the type of conversion.

* *UTF-8 => Base64*
* *Base64 => UTF-8*

**Result variable**  
Specify the name of the variable to which the result will be assigned. If no variable name is specified, the resulting string will be assigned to the original variable.
