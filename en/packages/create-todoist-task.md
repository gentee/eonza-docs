---
title: Create Todoist Task
desc: The command creates a task in the Todoist service
img:
   create-todoist-task: packages/create-todoist-task.png
html:
   create-todoist-task: '<img src="%img.create-todoist-task%" style="margin: 1em 1em;"/>'
---
# Create Todoist Task

**v1.23**  
The **Create Todoist Task** command creates the specified task in the Todoist service. For the script to work, the API token must be specified in the package settings.

%html.create-todoist-task%

**Content**  
The name of the task to be added. It will appear in your Todoist tasks list.

**Due Date**  
Specify the due date of the task. You can specify a specific date in *YYYYY-MM-DD* format or using [descriptions](https://todoist.com/help/articles/due-dates-and-times) that Todoist supports. For example, *tomorrow at 12:00*.

## Optional parameters

You can specify optional parameters for the task you create.

**desc**  
Additional description of the task.

**project**  
Identifier of the project to which you want to add the task.

**section**  
Identifier of the section where the task should be added.

**priority**.  
The priority of the task.
