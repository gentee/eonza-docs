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
* **eonza.eon** - binary file with notifications and other service information. Deleting this file does not affect the performance of the program.

## Config File

The main settings of the program are stored in the YAML configuration file *eonza.yaml*. Below is an example of a configuration file, which is created by default.

``` yaml
version: 1.1.0+1
mode: default
assetsdir: ""
extsdir: ""
log:
  dir: ""
  mode: file
  level: info
users:
  dir: ""
http:
  host: localhost
  port: 3234
  open: true
  theme: default
  jwtkey: s5c82473epey
playground:
  dir: ""
  summary: 0
  files: 0
  size: 0
whitelist: []
```

* **version** - Eonza version.
* **mode** - program operation mode. If not specified, the program will run in the default mode. The following options are available:
   * **default** - default mode.
   * **develop** - developer mode.
   * **playground** - safe "sandbox" mode.
* **assetsdir** - by default, the frontend files (html, js, png) are packed into an executable file. You can specify the directory with the unpacked files. This allows you to use modified versions of the files.
* **extsdir** - directory for installing extensions. Each extension is installed in a separate subdirectory.
* **whitelist** - if you installed Eonza on a remote server (hosting), we recommend specifying a "whitelist" of ip addresses in addition to password protection. In this case, specify the array of subnets from which which it is possible to connect to the program. If a request to Eonza comes from an ip-address that is not included in any of the specified networks, an error will be sent - *Access denied*. When defining the "whitelist", be sure to add the following subnetworks to it: **::1/128, 127.0.0.0/31**.

``` yaml
whitelist:
  - ::1/128
  - 127.0.0.0/31
  - 192.168.0.0/24
```

### Logging section

* **dir** - path to the directory with log-files. If it is equal to an empty line, the **log** subdirectory in the directory with the configuration file is used.
* **mode** - log type. It can be the combination of *file* and/or *stdout*. If it is not specified, then the logging is disabled. For example, *mode: file stdout*.
* **level** - logging level. May be *disable, error, warn, info*.

### Users section

* **dir** - path to the directory with user data. If it is equal to an empty line, the **users** subdirectory in the directory with configuration file is used.

### HTTP Configuration

Eonza launches a web server to display the program in a browser. Here are the settings related to the work of the web server.

* **host** - hostname (domain) by which you can access Eonza. By default, it is *localhost*. If you are installing Eonza on a VPS hosting, then specify the domain name. In this case, you should set a password, specify the *cert* and *priv* parameters. It is also recommended that you define a whitelist of IP addresses for access.
* **port** is the port that the web server uses. By default, **3234**.
* **localport** - port for the system localhost server. If not specified or equal to 0, then port + 1 is used.
* **open** - specify *false* if you do not want to automatically open the tab in your browser when you start the program.Ignored if *host* is not equal to *localhost*.
* **theme** - reserved.
* **jwtkey** is the secret key for creating JWT authorization tokens. It is needed in case you login by  password. The key is generated automatically when the configuration file is created, but you can change it later.

If *host* is not equal to *localhost*, then only *https* connection is used. Therefore, you must provide the full path to the SSL certificate and private key.

* **cert** - SSL certificate.
* **priv** - private key.

``` yaml
http:
  host: www.eonza.org
  port: 3234
  theme: default
  jwtkey: s5c82473epey
  cert: "/etc/letsencrypt/live/eonza.org/fullchain.pem"
  priv: "/etc/letsencrypt/live/eonza.org/privkey.pem"
```

### Playground Mode Settings

If you specified the **playground** program mode, you can define the following additional settings for that mode.

* **dir** - path to the directory for writing and reading the files. If it is not specified, the subdirectory in the temporary directory will be created.
* **summary** - the total size of the files. By default, it is 10 MB.
* **files** - maximum number of files. By default, 100.
* **size** - maximum file size. The default size is 5 MB.
* **tasks** - maximum number of simultaneously running scripts. By default, 2.

``` yaml
mode: playground
...
playground:
    dir: "/tmp/eonza/playground"
    summary: 20000000
    files: 250
    size: 3000000
    tasks: 3
```
