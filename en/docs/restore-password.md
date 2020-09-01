---
title: How to recover password in Eonza program
desc: What to do if you forgot the password to log in the Eonza program.
---
# How to recover the password

Eonza does not explicitly store your login password, so you cannot recover a forgotten password. You can either set a new password or disable login by password. To do so, you need to run the program with the **-psw** option. Specify a new password or *reset* to reset the password as a value. The specified password will be saved in the settings and will be active for all subsequent launches of the program.

``` txt
.\eonza -psw=reset
eonza.exe -psw=mynewpassword
```
