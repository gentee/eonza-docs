---
title: Command Line Parameters
desc: Eonza command line parameters.
---
# Command Line Parameters

``` txt
eonza [-cfg=config file] [-psw=password] [-install]
```

**-cfg**  
If you want to store all settings and data separately from the executable file, Eonza allows you to specify the path to the configuration file in a command line parameter. In this case, the configuration file can have any name.

**-psw**  
With this option you can set or reset a password to connect to Eonza.  The specified password will be saved in the settings and will be active for all subsequent launches of the program. To reset the password, specify *reset* as the parameter value.

**-install**  
If this parameter is specified, the program will only create all necessary files and directories and finish its work. It can be used in combination with the *-psw* parameter to set a password. If the program has already been installed, running with this parameter will not affect anything.

## Examples

``` txt
/usr/bin/eonza /home/user/data/eonza/myeonza.yaml
eonza.exe ../data/eonza.yaml
./eonza -psw=mypassword
```
