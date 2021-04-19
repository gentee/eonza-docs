---
title: Installing Eonza on VPS Hosting
desc: How to install Eonza on VPS hosting.
---
# Installation on VPS hosting

Eonza is an ordinary web server which listens to a certain port and has an API. Thus, if you have VPS hosting, you can install Eonza on the server and manage your hosting from the browser. It is recommended to additionally use *NGINX* or another web server as a proxy server. Let's consider an example of Eonza installation on CentOS 64-bit with **nginx** web-server and a ready-made domain name *my-eonza-domain.org*. Assume that this domain already has a website, so let's make Eonza open in the browser at **https://www.my-eonza-domain.org:[port]**.

## Step 1. Installing Eonza

Create a directory on the server, download and save the [program distribution](/downloads/linux-amd64/eonza) for Linux there. For example, let's save the program to the */home/eonza* directory. It is better to immediately set a password for the login, to do this, run the program with the *-install* and *-psw* parameters. In this case, Eonza will create the necessary files, set the login password and finish its work.

``` txt
cd /home/eonza
./eonza -install -psw=mypassword 
```

## Step 2. Configuring Eonza

Select localhost port for Eonza program and external port for *nginx* proxy server. Open [configuration file](config.html) *eonza.yaml* in any editor and specify the following fields in the *http* section:

* *host* - host name
* *port* - the port the program will listen to.
* *open* - specify *false*, so that the program does not try to open Eonza in the browser on the server.
* *access* - specify *host*
* *jwtkey* - specify a random string for creating JWT keys.

So the settings could be something like this

``` yaml
http:
    host: www.my-eonza-domain.org
    port: 5001
    open: false
    theme: default
    access: host
    jwtkey: my-secret-jwt-key
```

For security reasons, it is recommended to define a list of "white" IP addresses and subnets. In this case, all requests from other ip-addresses will be ignored. You can specify subnets belonging to your ISP. Also, be sure to add local subnets *::1/128* and *127.0.0.0/31*. The "white" list of ip-addresses and subnets is specified in the *whiltelist* section. For example,

``` yaml
whitelist:
    - ::1/128
    - 127.0.0.0/31
    - 92.140.108.0/24
    - 92.140.109.0/24
```

Since each script runs as a separate process and occupies its own port, specify two more parameters.

* *portshift* - the difference between nginx port and real port. For example, if -1000 is specified, then *https://www.my-eonza-domain.org:4002* will correspond to *localhost:5002*.
* *cdn* - specify Eonza address so that scripts can use the js and html files already loaded in the browser.

``` yaml
portshift: -1000
cdn: https://www.my-eonza-domain.org:4001
```

## Step 3. Create systemd service

Let's register the Eonza program as a service. To do this, create a **eonza.service** file in the **/usr/lib/systemd/system** directory. The example given below is the simplest *eonza.service*, although *.service* file can have many more parameters.

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
systemctl start eonza.service
systemctl enable eonza.service
```

If you change the eonza.service file, you must run *systemctl daemon-reload* to update the settings. Use *systemctl status eonza.service* or *service eonza status* to get service status.

## Step 4. Configuring the proxy server

Using *nginx* as a proxy server, allows you to connect Eonza to an existing domain name via https protocol. Suppose that you already have a website https://www.my-eonza-domain.org with [Let's Encrypt](https://letsencrypt.org) certificate and you want to open Eonza at *https://www.my-eonza-domain.org:4001*. To do this, add the following sections to the */etc/nginx/conf.d/my-eonza-domain.org.conf* configuration file:

``` txt
map $server_port $port {
    "~^4(?P<1>[0-9]+)$" "5$1";
}

server {
    listen 4001-4100 ssl;
    server_name www.my-eonza-domain.org;
    
    ssl_certificate /etc/letsencrypt/live/my-eonza-domain.org/fullchain.pem; 
    ssl_certificate_key /etc/letsencrypt/live/my-eonza-domain.org/privkey.pem;

    ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
    ssl_prefer_server_ciphers on;

    ssl_dhparam /etc/ssl/certs/dhparam.pem;
    ssl_ciphers 'ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-AES256-GCM-SHA384:DHE-RSA-AES128-GCM-SHA256:DHE-DSS-AES128-GCM-SHA256:kEDH+AESGCM:ECDHE-RSA-AES128-SHA256:ECDHE-ECDSA-AES128-SHA256:ECDHE-RSA-AES128-SHA:ECDHE-ECDSA-AES128-SHA:ECDHE-RSA-AES256-SHA384:ECDHE-ECDSA-AES256-SHA384:ECDHE-RSA-AES256-SHA:ECDHE-ECDSA-AES256-SHA:DHE-RSA-AES128-SHA256:DHE-RSA-AES128-SHA:DHE-DSS-AES128-SHA256:DHE-RSA-AES256-SHA256:DHE-DSS-AES256-SHA:DHE-RSA-AES256-SHA:AES128-GCM-SHA256:AES256-GCM-SHA384:AES128-SHA256:AES256-SHA256:AES128-SHA:AES256-SHA:AES:CAMELLIA:DES-CBC3-SHA:!aNULL:!eNULL:!EXPORT:!DES:!RC4:!MD5:!PSK:!aECDH:!EDH-DSS-DES-CBC3-SHA:!EDH-RSA-DES-CBC3-SHA:!KRB5-DES-CBC3-SHA';
    ssl_session_timeout 1d;
    ssl_session_cache shared:SSL:50m;

    ssl_stapling on;
    ssl_stapling_verify on;
    add_header Strict-Transport-Security max-age=15768000;

    location = /ws {
        proxy_pass http://127.0.0.1:$port/ws;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "Upgrade";
        proxy_set_header Host $host;
    }
    
    location / {
        if ($http_origin ~ '^https://www.my-eonza-domain.org') {
            add_header Access-Control-Allow-Origin "$http_origin";
        }
        access_log off;
        proxy_pass http://127.0.0.1:$port;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_redirect off;
    }
}
```

These settings instruct nginx to listen on all ports from 4001 to 4100 and redirect requests to the appropriate ports 5001-5100 to localhost. It should be noted that older versions of nginx do not support *listen 4001-4100 ssl* entry. In this case, update nginx to the latest stable version or create separate partitions for multiple ports. Save the configuration file and restart nginx (*service nginx restart*). Enter *https://my-eonza-domain.org:4001* in your browser and if everything has been configured correctly, you will see the login page of Eonza program.
