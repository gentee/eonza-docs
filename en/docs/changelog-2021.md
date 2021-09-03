---
title: Changelog for 2021
desc: Eonza Program Changelog for 2021
---
# Changelog for 2021

<!--## Beta version 1.8.0 
## Developer version-->

## Developer version

* Added the [Remove Lines](/scripts/remove-lines.html) command.
* Added the [Foreach Line](/scripts/foreach-line.html) command.
* Added the [XLSX Template](/scripts/xlsx-template.html) command.
* Added the [ODS Template](/scripts/ods-template.html) command.
* Added the [ODT Template](/scripts/odf-odt-template.html) command.
* Added the [DOCX Template](/scripts/docx-template.html) command.
* Added the [Append To Array](/scripts/append-to-array.html) command.
* Added the [Append To Map](/scripts/append-to-map.html) command.
* Added [predefined constants](/docs/constants.html) - *date*, *time*, *year*, *month*, *day*.
* A comparison condition by the presence of a substring has been added to the **If Statement** and **While Statement** commands.
* Fixed a bug in the **Set Variable** command - the 'Substitute Variable Values' parameter worked incorrectly.

## Version 1.20.0 - 2021/08/09

* Added the [Parse HTML](/scripts/parse-html.html) command.
* Added the [Browser](/docs/browser.html) tab to define scripts in Chrome extension.
* Added [Chrome extension](/docs/chrome-extension.html) to run scripts from the browser.

## Version 1.19.0 - 2021/06/07

* Added the [Read INI Values](/scripts/read-ini-values.html) command.
* Added the [Create File From Template](/scripts/create-file-from-template.html) command.
* Added the [Create Report](/scripts/create-report.html) command.
* Added *Timeout* parameter to the **Exit** command.
* Task Manager
    * Added [settings](/docs/settings.html).
    * Added pagination.
    * Added Refresh button.
    * Added protection of completed tasks from deletion.

## Version 1.18.0 - 2021/04/30

* Added support for TLS connections. Working with a remote server is only possible via **https**. [Installation on VPS hosting](installation-on-vps-hosting.html) does not require Nginx, Apache and other web servers.
* Added the *localport* predefined constant.
* Removed *access* parameter and added *localport, cert, priv* parameters in [config file](config.html).
* Fixed bug with the incorrect result of *Check for Update*.
* Fixed minor bugs in the Task Manager.

## Version 1.17.0 - 2021/04/24

* Added the [Try / Catch](/scripts/try-catch.html) command.
* Added [Pro version](/pro-version.html).
    * [License Pro](/docs/eonza-pro-license.html)
    * [General Settings](/docs/pro-general.html)
    * [Roles and users](/docs/users.html)
    * [Security](/docs/pro-security.html)
    * [Storage](/docs/pro-storage.html)

## Version 1.16.0 - 2021/04/06

* Added [Feedback](/docs/help.html) form.
* Added the Scheduler - [Events](/docs/events.html).
* Added the [Create Event](/scripts/create-event.html) command.
* Added the [Run Script](/scripts/run-script.html) command.
* Added **data** and **eonzaport** predefined constants.
* Added *Starts with* parameter to the **If Statement** command.
* Added *Append Data* parameter to the **Write To File** command.
* Added display of IP address to the Information tab of the running script.

## Version 1.15.0 - 2021/03/23

* Added the Scheduler - [Timers](/docs/timers.html).
* Added the [Markdown To HTML](/scripts/markdown-to-html.html) command.
* Added the [Readme](/scripts/readme.html) command.
* Added *Preview* option for **Multi-line text** in the script parameters.

Fixed bugs

* Wrong display *HTML Text* in the **Form** command.

## Version 1.14.0 - 2021/03/09

* Added the [Set Registry Value](/scripts/set-registry-value.html) command.
* Added the [Get Registry Value](/scripts/get-registry-value.html) command.
* Added the [Delete Registry Value](/scripts/delete-registry-value.html) command.
* Added the [Delete Registry Key](/scripts/delete-registry-key.html) command.
* Added the [Foreach Registry Value](/scripts/foreach-registry-value.html) command.
* Added the [Foreach Registry Subkey](/scripts/foreach-registry-subkey.html) command.
* Added the [Foreach Line in CSV](/scripts/foreach-line-csv.html) command.
* Improved security.

## Version 1.13.0 - 2021/02/19

* Added the [Parse YAML](/scripts/parse-yaml.html) command.
* Added the [Hex Encoding](/scripts/hex-encoding.html) command.
* Added the [Base64 Encoding](/scripts/base64-encoding.html) command.
* Added the [Convert Text](/scripts/convert-text.html) command.
* Added the *Substitute Variable Values* parameter to the [Set Variable](/scripts/set-variable.html) command.
* Added the *Skip if file does not exist* checkbox to the [Delete File](/scripts/delete-file.html) command.
* Refactored password protection.

Fixed bugs

* Notifications were not shown when using a password.

## Version 1.12.0 - 2021/02/04

* Added the [SMTP Server](/scripts/smtp-server.html) command.
* Added the [Send Email](/scripts/send-email.html) command.
* Added the [SQL Connection](/scripts/sql-connection.html) command.
* Added the [SQL Close](/scripts/sql-close.html) command.
* Added the [SQL Exec](/scripts/sql-exec.html) command.
* Added the [SQL Query](/scripts/sql-query.html) command.
* Added the [SQL Row](/scripts/sql-row.html) command.
* Added the [SQL Value](/scripts/sql-value.html) command.
* Fixed some minor bugs.

## Version 1.11.0 - 2021/01/22

* Added the [Copy To Clipboard](/scripts/copy-to-clipboard.html) command.
* Added the [Get Clipboard](/scripts/get-clipboard.html) command.
* Added [Notifications](/docs/notifications.html).
* Added the [Notification](/scripts/notification.html) command.
* Added the [Send Telegram Message](/scripts/send-telegram-message.html) command.
* Added language selection on the first launch.
* Added variable substitution to the **HTTP Request** command.
* Added *Check for Update* button in **Help - About**.
* Added setting for automatic check for updates in **Settings - General**.

## Version 1.10.0 - 2021/01/06

* Added the [Rename Files](/scripts/rename-files.html) command.
* Added the [Move Files](/scripts/move-files.html) command.
* Added the [Download File](/scripts/download-file.html) command.
* Added the [Foreach Line in File](/scripts/foreach-line-file.html) command.
* Added Hash function to **Set Variable** command.
* Added *If File Exists* parameter to the **Move File** and **Rename File** commands.
* Added *Save a copy* to the *If File Exists* parameter in the **Copy File** command.
* Added *Save a copy* button in the **File Confirmation** command.
* Fixed some minor bugs.
