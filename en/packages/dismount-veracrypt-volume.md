---
title: Dismount VeraCrypt Volume
desc: The command will unmount the VeraCrypt volume
img:
  dismount-veracrypt-volume: packages/dismount-veracrypt-volume.png
html:
  dismount-veracrypt-volume: '<img src="%img.dismount-veracrypt-volume%" style="margin: 1em 1em;"/>'
---
# Dismount VeraCrypt Volume

The **Dismount VeraCrypt Volume** command will unmount the VeraCrypt volume.

%html.dismount-veracrypt-volume%

** Drive Letter/Mount Directory**  

* **Windows**. Specify the drive letter you want to unmount. 
* **Linux**. Specify the directory you want to unmount. 

If this parameter is not specified, then all VeraCrypt volumes will be dismounted.

**sudo Password (for Linux)**  
When running on Linux, you need to provide a sudo password. Do not specify the password explicitly! Ask for the password while the parent script is running or use the secret storage in the Pro version.
