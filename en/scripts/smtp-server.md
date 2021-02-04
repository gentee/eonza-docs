---
title: Save SMTP server settings
desc: The command saves the SMTP server settings.
img:
   smtp-server: scripts/smtp-server.png
html:
   smtp-server: '<img src="%img.smtp-server%" style="margin: 1em 1em;"/>'
---
# SMTP Server

The **SMTP server** command saves the specified settings for connecting to the SMTP server into a variable. Further, the name of this variable should be specified in the [Send Email](send-email.html) command.

%html.smtp-server%

**Host**.  
Specify the host of the SMTP server you want to use to send the e-mail.

``` txt
smtp.gmail.com
localhost
192.168.0.110
```

**Port**.  
Specify the port to connect to the SMTP server. If not specified, *465* port will be used for SSL connection and *25* in other cases.

**Connection Security**  
Specify the type of connection.

* **None** - unsecured connection.
* **SSL/TSL** - secure connection.

**User name**  
Provide a username to connect to the server. As a rule, it is the same as an email.

``` txt
eonza.dev@gmail.com
```

**Password**.  
Password to connect to the server. For security reasons, do not specify it explicitly.

**Result Variable**  
Specify the name of the variable to store the SMTP settings.
