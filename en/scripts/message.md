---
title: Show message with buttons
desc: The command shows a message with buttons.
img:
   message: scripts/message.png
   sample-6-1: scripts/sample-6-1.png
   sample-6-2: scripts/sample-6-2.png
html:
   message: '<img src="%img.message%" style="margin: 1em 1em;"/>'
   sample-6-1: '<img src="%img.sample-6-1%" style="margin: 1em 1em;"/>'
   sample-6-2: '<img src="%img.sample-6-2%" style="margin: 1em 1em;"/>'
---
# Message

The **Message** command allows you to display various types of messages with the corresponding buttons. You can also define your own set of buttons.

%html.message%

**Type**  
Specify message type. For each type, the corresponding icon and set of buttons are shown. The default buttons and the value to be returned when you click on the button are listed below.

* **Question**. Buttons: *Yes(yes)*, *No(no)*.
* **Information**. Button: *OK(ok)*
* **Warning**. Buttons: *OK(ok)*, *Cancel(cancel)*.
* **Error**. Buttons: *Repeat(retry)*, *Abort(abort)*, *Ignore(ignore)*

**Text**  
Message text. You can use HTML in the body of your message.

``` html
This is a message with <span style="color: #00f"><b>custom buttons</b></span>!
```

**Result Variable**  
Specify the name of the variable that will be assigned the value of the button clicked by the user.

## Custom buttons

You can create your own set of buttons for your message. In this case, the default buttons will be hidden.

**Name**  
Enter the name of the button.

**Value**  
Specify the value of the button that will be written to *Result variable* when this button is pressed.

[%dwnsample%](/samples/sample-6.yaml)

%scriptresult%

%html.sample-6-1%
%html.sample-6-2%
