---
title: Send an HTTP request
desc: The script sends an HTTP request.
img:
   httprequest: scripts/httprequest.png
html:
   httprequest: '<img src="%img.httprequest%" style="margin: 1em 1em;"/>'
---
# HTTP Request

The **HTTP request** command sends the request to the specified URL and saves the received response in a variable.

%html.httprequest%

**URL**  
Specify the URL where the HTTP request will be sent.

**Method**  
Select the HTTP request method.

**Parameters**  
You can specify query parameters. To do this, add the name and value of each parameter.

**Variable Name**  
Specify the name of the variable where the server response will be written.

**Headers**  
If necessary, you can define additional request headers. For example, by default, when sending a *POST* request, the parameters are passed as form data. If you want to pass them as JSON, then add a *Content-Type* header with *application/json; charset=UTF-8* value.
