---
title: Eonza Configuration
desc: The configuration of the Eonza program.
---
# Configuration

Eonza program does not require installation and is distributed as a single executable file. At the first launch it creates all the necessary directories and files.

* **log** - the directory for storing the log of the program and scripts.
* **users** - directory for storing user settings.
* **eonza(.exe)** - Eonza program.
* **eonza.eox** - binary file with data. It contains user-created scripts and common settings.
* **eonza.yaml** - configuration file.

## Config File

The main settings of the program are stored in the YAML configuration file *eonza.yaml*. Below is an example of a configuration file, which is created by default.

``` yaml
version: 0.2.0+1 (beta)
develop: false
assetsdir: ""
log:
    dir: ""
    mode: file
    level: info
users:
    dir: ""
http:
    port: 3234
    open: true
    theme: default
    access: localhost
    jwtkey: mysecretkey
```

* **version** - Eonza version.
* **develop** - specify *true* to enable developer mode.
* **assetsdir** - by default, the frontend files (html, js, png) are packed into an executable file. You can specify the directory with the unpacked files. This allows you to use modified versions of the files.

### Logging section

* **dir** - path to the directory with log-files. If it is equal to an empty line, the **log** subdirectory in the directory with the configuration file is used.
* **mode** - log type. It can be the combination of *file* and/or *stdout*. If it is not specified, then the logging is disabled. For example, *mode: file stdout*.
* **level** - logging level. May be *disable, error, warn, info*.

### Users section

* **dir** - path to the directory with user data. If it is equal to an empty line, the **users** subdirectory in the directory with configuration file is used.

### HTTP Configuration

Eonza launches a web server to display the program in a browser. Here are the settings related to the work of the web server.

* **port** is the port that the web server uses. By default, **3234**.
* **open** - specify *false* if you do not want to automatically open the tab in your browser when you start the program.
* **theme** - reserved.
* **access** - can be one of the following values:
  * *private* - access only from LAN IP.
  * *localhost* - access by domain *localhost*.
* **jwtkey** is the secret key for creating JWT authorization tokens. It is needed in case you login by  password. The key is generated automatically when the configuration file is created, but you can change it later.
