---
title: How to create a sales script or a phone script
desc: How to create a phone script or sales script with Eonza software.
img:
   sales-script-page: scripts/sales-script-page.png
   sales-script-page-app: scripts/sales-script-page-app.png
   sales-script: scripts/sales-script.png
html:
   sales-script-page: '<img src="%img.sales-script-page%" style="margin: 1em 1em;"/>'
   sales-script-page-app: '<img src="%img.sales-script-page-app%" style="margin: 1em 1em;"/>'
   sales-script: '<img src="%img.sales-script%" style="margin: 1em 1em;"/>'
---
# How to create a sales script

**v1.27.0**  
Eonza program has special features for creating sales scripts or phone scripts. You can create sales scripts **for free** and share them with other people.

## Step 1. Define the content of the script pages

First you need to define which pages your script will contain. For each page, you should come up with a title and its content. Also determine the possible transition options from each page. Each transition option should link to another page.

## Step 2. Create a new script

Create a new script in the Eonza program. In the script settings, specify its name and a short description.

## Step 3. Add pages to the script

Create a [Sales Script Page](/scripts/sales-script-page.html) command for each page. The text can be in HTML or Markdown format. Add your answer choices by specifying the page names. All answer options will be displayed as links. If users clicks on an option, they will be redirected to the corresponding page. If you leave the link text empty, the name or title of the corresponding page will be displayed.

%html.sales-script-page%

## Step 4: Add the Sales Script command

After you added commands for all pages in the previous step, it remains to add the [Sales Script](/scripts/sales-script.html) command. Here you should specify the name of the page the sales script will start from.

%html.sales-script%

Now you can run the ready-made script. If you want to transfer it to another computer, export the script. To do that, press the Menu button and select **Export**. To import it, you should use the **Import** menu item.

[%dwnsample%](/samples/demo-sales-script.yaml)

%scriptresult%

%html.sales-script-page-app%
