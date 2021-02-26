---
title: Users tab in the Pro version
desc: Documentation on the Users tab in the Pro version of Eonza.
img:
   users: users.png
   users-role: users-role.png
   users-user: users-user.png
html:
   users: '<img src="%img.users%" style="margin: 1em 1em;"/>'
   users-role: '<img src="%img.users-role%" style="margin: 1em 1em;"/>'
   users-user: '<img src="%img.users-user%" style="margin: 1em 1em;"/>'
---
# Roles and users

The standard version of *Eonza* works only in single-user mode. At the first launch of the program, the **admin** group is created with full rights to all actions and a user named **root** in this group. By default, logging in as this user is not password-protected. However, if you have installed the program on a VPS or a local server, then you must necessarily specify a password to enter the program. You might want to give other people access to run some scripts. The *Pro* version allows you to create roles and users and work with the program in **multi-user mode**.

%html.users%

## Roles

Roles are used to group users by access rights when working with Eonza. By default, there is only one role, *admin*, which gives all the possibilities when working with the program. All created roles do not allow editing and viewing scripts, and hide all the program settings that do not apply to a particular user.

%html.users-role%

**Name**  
Specify the name of the role to be created.

**Allow**  
Specify system names of scripts that can be run by a user with this role. It should be noted that the user will not be able to open, view or modify these scripts in the editor. All other scripts will not be visible to the user at all. Also, you can use regular expressions. They must begin and end with **/**. Regular expressions are compared to the full name, which consists of the folder name and the system script name. For example, you want to give access to all scripts in the *mycompany* folder. In this case, it is enough to specify */mycompany/*. Specify command names or regular expressions separated by spaces or line breaks.

**Tasks:View**  
Specify which completed tasks will be visible to the user in the *Task Manager*. Among the tasks in progress, the user can only see the tasks he/she has started.

* **---** - tasks are not visible to the user.
* **ALL** - all completed tasks are visible to the user.
* **GROUP** - tasks that have been started by users with the same role are visible.
* **USER** - the user sees only own tasks.

**Tasks:Delete**  
Specify which completed tasks the user can delete in *Task Manager*.

* **---** - user cannot delete tasks.
* **ALL** - user can delete all tasks.
* **GROUP** - the user can delete tasks that were started by users with the same role.
* **USER** - the user can delete only his/her own tasks.

**Notifications:View**  
Specify which notifications will be visible to the user.

* **---** - notifications are not visible to the user.
* **ALL** - all notifications are visible to the user.
* **GROUP** - notifications of scripts launched by users with the same role are visible.
* **USER** - user sees notifications only from own tasks.

**Notifications:Delete**  
Specify which notifications the user can delete.

* **---** - user cannot delete notifications.
* **ALL** - user can delete all notifications.
* **GROUP** - user can delete notifications from tasks that were started by users with the same role.
* **USER** - user can only delete notifications from own tasks.

## Users

This list displays all created users.

%html.users-user%

**Name**  
User name. This is the name that will be displayed in Task Manager and Notifications for the tasks that the user has started. On the login page, a user will not need to enter the name, only the password.

**Password**  
The user's password for the login. The user can change his password in the settings. If you change the password and don't give it to the user, he won't be able to enter the program. If you don't want to change the user's password when editing, leave it blank.

**Role**  
User role. If you specify the **admin** role, the user will have all rights when working with the program.
