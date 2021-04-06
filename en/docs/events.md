---
title: Working with events in the Eonza program 
desc: Documentation for handling events in the Eonza program.
img:
   events: events.png
   events-edit: events-edit.png
html:
   events: '<img src="%img.events%" style="margin: 1em 1em;"/>'
   events-edit: '<img src="%img.events-edit%" style="margin: 1em 1em;"/>'
---
# Events

Events are used to integrate Eonza with other programs and services. When an event occurs, Eonza runs the corresponding script. An event can be created in two ways:

* By [Create Event](/scripts/create-event.html) command in some script.
* By [HTTP request](run-script-http.html) from any other application (computer).

Events are processed only when the Eonza program is running.

%html.events%

## Event parameters

%html.events-edit%

**Name**  
Provide a name for the event.

**Script**  
The system name of the script. The script should have no parameters as otherwise it will expect input parameters on startup. You can use the **data** parameter in HTTP request to pass data to the script.

**Disabled**  
Check this checkbox if you want to disable event handling.

**Token**  
The token is required when [sending an HTTP request](run-script-http.html) from another computer. In this case, specify any text here. Using a token protects against unauthorized event creation.  Do not share the token with unauthorized persons.

**IP Whitelisting**  
For additional protection, you can specify the IP addresses or subnets from which HTTP requests for creating events will be accepted. By default, the subnets that are specified in the **whitelist** field in [configuration file](config.html) are checked first. Thus, if your **whitelist** field is not empty and contains all the required ip-addresses, then leave this parameter empty. If you have defined this parameter and want to use the *Create Event* command or send HTTP requests *localhost:port/api/event* on the same computer, then add the following subnets: ::1/128, 127.0.0.0/31.
