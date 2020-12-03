---
title: Decrypt the file
desc: The command decrypts the specified file.
img:
   decrypt-file: scripts/decrypt-file.png
html:
   decrypt-file: '<img src="%img.decrypt-file%" style="margin: 1em 1em;"/>'
---
# Decrypt File

The **Decrypt File** command decrypts the specified file. This file must be encrypted using the [Encrypt File](encrypt-file.html) command.

%html.decrypt-file%

**File name**  
Specify the full or relative path to the file you want to decrypt. The original file will not be changed.

**Password**  
Enter the encryption password. **Do not explicitly specify passwords in scripts!**

**Destination Folder**  
The directory where the decrypted file will be saved. If it is not specified, the file will be saved to the folder of the source file.

**Output File**  
The name of the decrypted file. If not specified, the name will be the same as the original file that was encrypted.
