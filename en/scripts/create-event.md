---
title: Create event
desc: The command creates an event in the Eonza program to run the corresponding script.
img:
   create-event: scripts/create-event.png
html:
   create-event: '<img src="%img.create-event%" style="margin: 1em 1em;"/>'
---
# Create Event

The **Create Event** command creates an [event](/docs/events.html) in the Eonza program. In this case, the Eonza program will run the corresponding script.

%html.create-event%

**Event Name**  
Specify the name of the event you want to create.

**Attached data**.  
You can specify any text that will be assigned to the **data** predefined constant in the running script. The script must handle the incoming **data** constant.

``` json
{
    "num": 77,
    "path": "#outfile#",
    "list": [ 
        { "title": "First Item", "value": 11},
        { "title": "Second Item", "value": 13}
    ]
}
```
