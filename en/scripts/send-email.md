---
title: Send Email
desc: The command sends an email.
img:
   send-email: scripts/send-email.png
html:
   send-email: '<img src="%img.send-email%" style="margin: 1em 1em;"/>'
---
# Send Email

The **Send Email** command sends an email using the specified SMTP server.

%html.send-email%

**SMTP server**  
Specify the name of the variable that contains the SMTP server settings. This variable must be defined using the [SMTP Server](smtp-server.html) command .

**From**  
Enter the email of the sender. If no sender is specified, the username to connect to the SMTP server will be used. It is recommended that the sender is the same as the username, otherwise the mail server may not send the email.

``` txt
eonzadev@gmail.com
Support Team <eonzadev@gmail.com>
```

**To**  
Specify the email of the user you want to send the email to.

``` txt
johndoe@eonza.org
John Doe <johndoe@eonza.org>
```

**Subject**  
Specify the subject line of the email.

**Body**  
Enter the content of the email. If you want to send an email with HTML markup, the text must begin with the tag *&lt;html&gt;*.

``` html
<html>
<body>
Hello, <b>#name#</b>,<br>
<p>
...
</p>
Best regards,<br>
#myinfo#
</body>
</html>
```
