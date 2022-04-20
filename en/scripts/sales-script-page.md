---
title: Create a sales script page
desc: The command creates a sales script page.
img:
   sales-script-page: scripts/sales-script-page.png
   sales-script-page-app: scripts/sales-script-page-app.png
html:
   sales-script-page: '<img src="%img.sales-script-page%" style="margin: 1em 1em;"/>'
   sales-script-page-app: '<img src="%img.sales-script-page-app%" style="margin: 1em 1em;"/>'
---
# Sales Script Page

The **Sales Script Page** command creates a page for the sales script. You can specify the necessary text and answer options to jump to the corresponding pages. This command does nothing. To run a sales script, use the [Sales Script](sales-script.html) command.

%html.sales-script-page%

**Name**  
Specify the name of the page. Use this name in the answer choices of other pages. Selecting the option will take the user to this page.

**Title**  
The title of the page. If not specified, the title will be the same as the page name.

**Text**  
Page text. You can use HTML or Markdown text. 

```html
Hello, <span style="color: #00f"><b>world</b></span>!
```

## Answer options

**Text**  
Specify the link text for the answer option. If not specified, the title of the sales script page, which is defined in the next field, will be used.

**Sales Script Page**  
Specify the name of the sales script page that will open when the user click on it. 

[%dwnsample%](/samples/demo-sales-script.yaml)

%scriptresult%

%html.sales-script-page-app%

## Additional links

* [How to create a sales script](/docs/how-to-create-sales-script.html)
