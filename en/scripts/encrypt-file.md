---
title: Encrypt the file
desc: The command encrypts the specified file.
img:
   encrypt-file: scripts/encrypt-file.png
html:
   encrypt-file: '<img src="%img.encrypt-file%" style="margin: 1em 1em;"/>'
---
# Encrypt File

The **Encrypt file** command encrypts the specified file and saves the encrypted data as a new file. This file can be decrypted using the [Decrypt File](decrypt-file.html) command.

%html.encrypt-file%

**File name**  
Specify the full or relative path to the file to be encrypted. The original file will not be changed.

**Algorithm**  
Select an encryption algorithm.

* *AES-256*

**Password**  
Enter the encryption password. **Do not explicitly specify passwords in scripts!**

**Destination folder**  
The directory where the encrypted file will be saved. If it is not specified, then the file will be saved to the source file folder.

**Output File**  
Name of the encrypted file. If not specified, the *.ec* extension will be appended to the source file name.
