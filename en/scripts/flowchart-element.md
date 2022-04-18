---
title: Create Flowchart Element
desc: The command creates a flowchart element.
img:
   flowchart-element: scripts/flowchart-element.png
   flowchart-app: scripts/flowchart-app.png
html:
   flowchart-element: '<img src="%img.flowchart-element%" style="margin: 1em 1em;"/>'
   flowchart-app: '<img src="%img.flowchart-app%" style="margin: 1em 1em;"/>'
---
# Flowchart Element

**v1.27.0**  
The **Flowchart Element** command creates a page for the flowchart element. The command may contain other scripts that will be executed when you jump to this element. You can specify the necessary text and a list of further actions that will implement the transition to other flowchart elements. This command is similar to a function and only executes internal commands when jumping to that element. To run a flowchart, you must use the [Flowchart](flowchart.html) command.

%html.flowchart-element%

**Name**  
Specify the name of the element. Use this name in options for other elements. Selecting an option with this name will take the user to that element.

**Title**  
Page title. If not specified, the title will be equal to the element name.

**Text**.  
Page text. You can use text in HTML or Markdown format. 

```md
Current value: **#num#**
```

## Next actions

**Text**  
Specify the link text for the option. If not specified, the title of the element, which is defined in the next field, will be used.

**Flowchart element**  
Specify the name of the flowchart element that will be executed when this option is selected.

[%dwnsample%](/samples/demo-flowchart.yaml)

%scriptresult%

%html.flowchart-app%
