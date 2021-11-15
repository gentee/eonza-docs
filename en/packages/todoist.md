---
title: Package for working with the Todoist service
desc: Package for work with Todoist scheduling service.
img:
   todoist: packages/todoist.png
   todoist-token: packages/todoist-token.png
html:
   todoist: '<img src="%img.todoist%" style="margin: 1em 1em;"/>'
   todoist-token: '<img src="%img.todoist-token%" style="margin: 1em 1em;"/>'
---
# Todoist

The **Todoist** package  contains scripts to work with [Todoist](https://todoist.com/) scheduling service. All scripts use the Todoist server's REST API to manage tasks. For all scripts of the package to work it is necessary to specify API Token in the package settings.

%html.todoist%

## Settings

**API URL**  
Specify the URL to which REST API requests will be sent. By default, it is *https://api.todoist.com/rest/v1/*.

**Token**  
Since the Todoist service requires authentication to access your tasks, you must provide an account token. It can be found in the Settings menu of your account, in the Integrations section. Do not show or pass this API token to anyone. For safe operation, it is recommended to use the Eonza Pro version and store the token in the  encrypted storage, and here you should only specify the name of the corresponding value.

%html.todoist-token%

## Scripts

%func.children%
