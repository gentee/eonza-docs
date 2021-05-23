---
title: Create a report
desc: This command creates and displays an HTML, Markdown or text report.
img:
   create-report: scripts/create-report.png
   result-report: scripts/result-report.png
html:
   create-report: '<img src="%img.create-report%" style="margin: 1em 1em;"/>'
   result-report: '<img src="%img.result-report%" style="margin: 1em 1em;"/>'
---
# Create Report

The **Create Report** command displays an HTML, Markdown or text report. You can create multiple reports while the script is running. You can view the report both while the script is running and after it ends. In addition, you can save the report to a file.

%html.create-report%

**Title**  
Report title.

**Text**.  
The text of the report you want to show to the user. If the text starts with **&lt;** then it will be shown as HTML. If the text begins with one or more characters **#** and a space, it will be displayed as Markdown text. In other cases, it will be shown as preformatted text.

%html.result-report%
