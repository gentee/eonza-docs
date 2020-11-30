---
title: Calculate file hash
desc: The command finds the hash of the specified file and saves it to a variable.
img:
   file-hash: scripts/file-hash.png
html:
   file-hash: '<img src="%img.file-hash%" style="margin: 1em 1em;"/>'
---
# File Hash

The **File Hash** command calculates the checksum of the specified file and saves the resulting value to a variable.

%html.file-hash%

**File name**  
Specify the full or relative path to the file the hash of which needs to be calculated.

**Algorithm**  
Select the algorithm for calculating the checksum.

* *MD5*
* *SHA256*

**Result Variable**  
Specify the name of the variable to which the resulting file hash will be written. The hash value is stored as a hexadecimal string.
