---
title: Send JSON request
desc: The script sends a JSON HTTP request.
img:
   send-json-request: scripts/send-json-request.png
html:
   send-json-request: '<img src="%img.send-json-request%" style="margin: 1em 1em;"/>'
---
# Send JSON Request

Nowadays, JSON is often used in REST API messaging. The **Send JSON Request** command sends a JSON request to the specified URL and stores the received response in an object variable. You won't need to parse the JSON response additionally.

%html.send-json-request%

**URL**  
Specify the URL where the JSON HTTP request will be sent.

**JSON**  
Specify the JSON data to be sent. By default the request sends data by **POST** method, but if this field is empty the request will be sent by **GET** method.

**Variable Name**  
Specify the name of a variable in which the server response will be written. An object variable will also be created into which the received JSON response will be parsed. For example, you've specified *myresp* in this field. Then when the server responses *{"id": 10, "state": "success"}* you can use the following values.

```txt
#myresp# => {"id": 10, "state": "success"}
#myresp.id# => 10
#myresp.state# => success
```

**Headers**  
You can define additional request headers if needed. For example, **Authorization**. You don't have to specify the *Content-Type* header. It will be added automatically with the value *application/json; charset=UTF-8*.

## Optional Parameters

You can specify additional parameters.

**response**  
The name of the object variable that will contain the response status. It will have two fields:

* *statuscode* - status code;
* *status* - response status.

For example, if you define *response: resp*, it will have the following values when the script is called successfully.

```txt
#resp.statuscode# => 200
#resp.status# => 200 OK
```

Note that if you do not define this parameter and the server returns a status code less than 200 or greater than 299, then in this case, the script will not parse the server response and returns an error. If this parameter is specified, you can handle the erroneous server response yourself.
