---
title: Installing Eonza on VPS Hosting
desc: How to install Eonza on VPS hosting.
---
# Installation on VPS hosting

Eonza is an ordinary web server which listens to a certain port and has an API. Thus, if you have VPS hosting, you can install Eonza on the server and manage your hosting from the browser. To do this, you must have your own site with a domain name and SSL certificate connected, because in this case Eonza works only through *https*. Consider an example of installing Eonza on CentOS 64-bit with an existing domain *my-eonza-domain.org*. Assume that this domain already has a website, so let's make Eonza open in the browser at **https://www.my-eonza-domain.org:[port]**.

## Step 1. Installing Eonza

Create a directory on the server, download and save the [program distribution](/downloads/linux-amd64/eonza) for Linux there. For example, let's save the program to the */home/eonza* directory. It is better to immediately set a password for the login, to do this, run the program with the *-install* and *-psw* parameters. In this case, Eonza will create the necessary files, set the login password and finish its work.

``` txt
cd /home/eonza
./eonza -install -psw=mypassword 
```

## Step 2. Configuring Eonza

Decide how the port will be used by the Eonza program. Open [configuration file](config.html) *eonza.yaml* in any editor and specify the following fields in the *http* section:

* *host* - the domain name
* *port* - the port the program will listen to.
* *open* - specify *false*, so that the program does not try to open Eonza in the browser on the server.
* *jwtkey* - specify a random string for creating JWT keys.
* *cert* - SSL certificate file.
* *priv* - file with the private key.

So the settings could be something like this

``` yaml
http:
    host: www.my-eonza-domain.org
    port: 5001
    open: false
    theme: default
    jwtkey: my-secret-jwt-key
    cert: "/etc/letsencrypt/live/my-eonza-domain.org/fullchain.pem"
    priv: "/etc/letsencrypt/live/my-eonza-domain.org/privkey.pem"    
```

For security reasons, it is recommended to define a list of "white" IP addresses and subnets. In this case, all requests from other ip-addresses will be ignored. You can specify subnets belonging to your ISP. Also, be sure to add local subnets *::1/128* and *127.0.0.0/31*. The "white" list of ip-addresses and subnets is specified in the *whiltelist* section. For example,

``` yaml
whitelist:
    - ::1/128
    - 127.0.0.0/31
    - 92.140.108.0/24
    - 92.140.109.0/24
```

## Step 3. Create systemd service

Let's register the Eonza program as a service. To do this, create a **eonza.service** file in the appropriate directory for the .service files. For example, in **/usr/lib/systemd/system** (CentOS) or **/lib/systemd/system** (Ubuntu). The example given below is the simplest *eonza.service*, although *.service* file can have many more parameters.

``` ini
[Unit]
Description=Eonza Service

[Service]
ExecStart=/home/eonza/eonza
WorkingDirectory=/home/eonza

[Install]
WantedBy=multi-user.target
```

Start and enable the service. Eonza will automatically start after rebooting the system.

``` txt
systemctl enable eonza.service
systemctl start eonza.service
```

If you change the eonza.service file, you must run *systemctl daemon-reload* to update the settings. Use *systemctl status eonza.service* or *service eonza status* to get service status.

This completes the installation and configuration of Eonza on VPS hosting. Specify in the browser *https: //www.my-eonza-domain.org:5001* (or another port that you specified in the settings) and, if everything was done correctly, you will see the login page of the Eonza program.
