---
title: Get a web page with a GET request
desc: The command sends a GET request and writes the response to a variable.
img:
   get-webpage: scripts/get-webpage.png
html:
   get-webpage: '<img src="%img.get-webpage%" style="margin: 1em 1em;"/>'
---
# Get Web Page

The **Get Web Page** command sends a *GET* request to the specified URL and stores the received answer in a variable. With this script you can request both web pages and small text files.

%html.get-webpage%

**URL**  
Specify the address of the web page whose content you want to receive. You can also specify additional *GET* request parameters.

``` txt
https://#mydomain#/docs/index.html
https://#mydomain#/files/script.yaml
https://www.eonza.org/api/get?id=#id#&user=#mynick#
```

**Variable Name**  
Specify the name of the variable into which the content of the web page will be written.
