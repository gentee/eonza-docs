---
title: Script for exporting Todoist tasks
desc: The script exports Todoist tasks and projects.
img:
   export-todoist: packages/export-todoist.png
html:
   export-todoist: '<img src="%img.export-todoist%" style="margin: 1em 1em;"/>'
---
# Export Todoist

**v1.23**  
The free Todoist account does not have the ability to export existing projects and tasks. How to back up Todoist content in this case? The **Export Todoist** script gets your projects, sections, tasks, comments and labels in JSON format and packs them into a zip file. For the script to work, the API token must be specified in the package settings.

%html.export-todoist%

**Path**  
Specify the directory where the zip file will be saved.

**Archive name (.zip)**  
Define name of the .zip file to be created.

The archive with a backup copy of your data will contain the following files:

* comments.json - comments;
* labels.json - labels;
* projects.json - projects;
* sections.json - sections;
* tasks.json - tasks.

