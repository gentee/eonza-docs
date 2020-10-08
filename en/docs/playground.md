---
title: Online demo version
desc: Online demo version of Eonza.
img:
   playground: playground.png
   playground-error: playground-error.png
html:
   playground: '<img src="%img.playground%" style="margin: 1em 1em;"/>'
   playground-error: '<img src="%img.playground-error%" style="margin: 1em 1em;"/>'
---
# Playground

If you want to try Eonza, you don't need to download it. Go to the site [https://playground.eonza.org](https://playground.eonza.org) and it will open a working version of the Eonza program, which is installed on the remote server. There are several nodes that are periodically initialized and, as a rule, one user occupies one node. Keep in mind that you are working in a demo version that may be available to other users, so do not create complex scripts that would not want to lose, and do not place sensitive information there.

## Limitations of the online demo version

Since the demo version runs on real hosting and the program has great computer control capabilities, there are a number of limitations for each node. They protect the server from accidental or intentional dangerous actions.

* **Processes**. Disabled launches of any processes, including opening files in the corresponding applications. That is, for example, the script [Run application](/scripts/run.html) will not work.

* **File system**. Files can be written and read only in the current directory, which is created when the script is run. In addition, there are restrictions on:
   * total number of files (not more than 100).
   * total size of files (not more than 10 MB).
   * maximum file size (not more than 5 MB).

* **Network**. Disabled [HTTP request](/scripts/httprequest.html) script. Calling other scripts to retrieve data from the Internet virtually adds a file with the appropriate size to the directory for writing. Thus, these scripts are also restricted by the file system. For example, you will not be able to download a file over 5MB or send more than 100 requests to sites.

* **Scripts**. The number of simultaneously running scripts cannot exceed 2.

* **Settings**. Disabled the ability to set login password.

If an error occurs during the script operation due to sandbox limitations, the script will stop working and output an error that starts with text **[Playground]**.

%html.playground%
%html.playground-error%
