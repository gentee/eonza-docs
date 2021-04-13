---
title: Working with the Secure Storage in the Pro version
desc: Documentation on working with the secure storage in the Pro version of Eonza.
img:
   pro-storage: pro-storage.png
   pro-storage-create: pro-storage-create.png
   pro-storage-item: pro-storage-item.png
   pro-storage-master: pro-storage-master.png
html:
   pro-storage: '<img src="%img.pro-storage%" style="margin: 1em 1em;"/>'
   pro-storage-create: '<img src="%img.pro-storage-create%" style="margin: 1em 1em;"/>'
   pro-storage-item: '<img src="%img.pro-storage-item%" style="margin: 1em 1em;"/>'
   pro-storage-master: '<img src="%img.pro-storage-master%" style="margin: 1em 1em;"/>'
---
# Storage

The storage allows you to safely store and use secret information, such as passwords and tokens, in your scripts. Before you start using the storage, you need to create it. To do that, specify the master password which will be used to decrypt and encrypt the storage using the **AES-256** algorithm.

%html.pro-storage-create%

The storage is stored on the disk in encrypted form only. If you forget the master password, you will not be able to restore the data. Note that after you start the program, the storage is encrypted. Enter the master password on the top panel or on the Storage tab for Eonza to decrypt the data. Otherwise, strings like **#@storagename#** will not be replaced with corresponding values from the storage when executing scripts.

%html.pro-storage-master%

If the master password is specified correctly, the storage will be decrypted and you can add passwords, tokens and other important information there. The column with the secret infomation is not displayed in the table.

%html.pro-storage%

**Disable**  
Disable the storage.  After clicking on this button, work with the storage will be disabled and you will need to enter the master password again.

**Change Password**  
Change the master password. To change the master password, you need to know the current password.

## Adding and editing

%html.pro-storage-item%

**Name**  
The name of the password or token that can be specified in scripts to substitute the corresponding value. To do this, use the **#@thisname#** notation. For example, you added a password to access a database named *mypassdb*. In this case, specify *#@mypassdb#* in the scripts as a password.

**Description**  
Description or comment for this storage item.

**Value**  
The password or token to be stored in the storage. When editing a record, the current value is not displayed, so leave this field blank or specify a new value.
