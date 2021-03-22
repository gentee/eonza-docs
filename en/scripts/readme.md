---
title: Show Readme text
desc: The command displays HTML, Markdown, or preformatted text.
img:
   readme-1: scripts/readme-1.png
   readme-2: scripts/readme-2.png
html:
   readme-1: '<img src="%img.readme-1%" style="margin: 1em 1em;"/>'
   readme-2: '<img src="%img.readme-2%" style="margin: 1em 1em;"/>'
---
# Readme

The **Readme** command displays HTML, Markdown or preformatted text. This command can also be used to describe script capabilities, documentation, etc.

%html.readme-1%

**Text**  
Specify the text you want the user to see. If the text starts with **&lt;** it will be shown as HTML. If the text starts with one or more characters **#** and a space, then it will be shown as Markdown text. Otherwise, it will be shown as preformatted text.

**Skip**  
Check this box if the text describes the operation and capabilities of the script and should not be displayed when the script runs.

%html.readme-2%
