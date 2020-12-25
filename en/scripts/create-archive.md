---
title: Create ZIP or TAR.GZ archive
desc: The command creates a ZIP or TAR.GZ archive.
img:
   create-archive: scripts/create-archive.png
html:
   create-archive: '<img src="%img.create-archive%" style="margin: 1em 1em;"/>'
---
# Create Archive

The **Create Archive** command creates a zip or tar.gz archive.

%html.create-archive%

**Output File**.  
Specify the path and name of the archive file to be created. Specify an appropriate extension for the file.

**Type**  
Select the *zip* or *tar.gz* type of the archive to be created.

**Path**.  
Specify the directory to be packed into the archive. By default, all files and subdirectories will be compressed.

You can specify patterns for files to be packed and for files and directories to be skipped.

**Recursive search**  
**Wildcard or regular expression**  
**Exclude Wildcard or RegExp**  
These parameters are described in the [Foreach File](foreach-file.html) command.
