---
title: Integrating Eonza with other applications
desc: How to run Eonza scripts from other applications.
---
# How to run a script from outside

**v1.16.0**  
The Eonza program allows you to run scripts from other applications. You can integrate Eonza with any program that can send HTTP requests.

First, add an event to [Task Scheduler](events.html). Be sure to specify the name of the event and the name of the script to run. If you want to send a request from the same computer, you do not need to configure anything else. Send a POST request **http://localhost:[port]/api/event** with the following parameters:

* **name** - the name of the event that will run the corresponding script.
* **data** - any text data. This data will be passed to the script in the **data** constant. The script should handle them if needed.

**[port]** - port number used by Eonza program.

For example,

``` txt
POST: http://localhost:3234/api/event
Parameters:
name: "myevent"
data: "value: 2345
  name: John Doe
  islocal: true"
```

## How to run a script from another computer

You can trigger an event in the Eonza program not only on the same computer, but also from any other computer. To do this, first [bind Eonza to a domain name](installation-on-vps-hosting.html) or static IP address. Also, specify the *Token* parameter in the event that will be triggered. It is recommended to specify more than 8 random characters as a token.

### Step 1: Get a one-time ID

Send a GET request **https://[yourdomain]:[port]/api/randid** to get a nonce. Eonza will return JSON object with **rand** field. If an error occurs, the object will contain a **error** field with the error text. The lifetime of a nonce is 3 seconds.

``` txt
GET: https://playground.eonza.org:3234/api/randid
Result:
{
    "rand": "1234567484"
}
```

### Step 2: Generate hash

You have to calculate **sha256** hash from POST request parameters. Combine the event name, the *data* parameter, the *rand* identifier, and the event token into one line. All lines are joined without spaces or other separators. Calculate the *SHA-256* hash from the resulting string.

### Step 3: Send POST request

Send POST request **https://[yourdomain]:[port]/api/event** with the following parameters:

* **name** - the name of the event that will launch the corresponding script.
**data** - any text data. This data will be passed to the script in the **data** constant. The script should process them if necessary.
**rand** - a nonce.
**sign** - SHA-256 hash that was calculated in the previous step.

If successful, a JSON object is returned with the fields *success* (true), *port* is the port of the running script, *id* is the task identifier. In case of an error, a 403 code or JSON object is returned with the *error* and *success* (false) fields.

``` txt
POST: https://playground.eonza.org:3234/api/event
Params:
Parameters:
name: "myevent"
data: "{
    "value": "2345,
    "name": "John Doe",
    "islocal": false
}"
rand: "1234567484"
sign: "034fa78bc....."
Result:
{
    "success": true, 
    { "port": 3237,
    { "id": 762373421,
}
```
