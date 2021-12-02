---
title: Mount VeraCrypt Volume
desc: The command mounts a VeraCrypt volume.
img:
  mount-veracrypt-volume: packages/mount-veracrypt-volume.png
html:
  mount-veracrypt-volume: '<img src="%img.mount-veracrypt-volume%" style="margin: 1em 1em;"/>'
---
# Mount VeraCrypt Volume

The **Mount VeraCrypt Volume** command mounts the specified encrypted file using the VeraCrypt program. For the script to work, the path to the VeraCrypt application file must be specified in the package settings.

%html.mount-veracrypt-volume%

**VeraCrypt Volume**  
Specify the full path to the encrypted VeraCrypt file that you want to mount.

**Password**  
Specify the password that was used to encrypt the mounted volume. Do not specify the password explicitly. Ask for the password while the parent script is running or use the secret storage in the Pro version.

**Drive Letter/Mount directory**  

* **Windows**. Specify the drive letter where the VeraCrypt volume will be mounted. If not specified, the volume will be mounted on the nearest unused drive letter.
* **Linux**. Specify the directory where the VeraCrypt volume will be mounted. If not specified, the volume will be mounted in the directory */mnt*.

**Keyfile**  
Specify the key file, if it was used for data encryption.

**sudo Password (for Linux)**  
When running on Linux, you need to provide a sudo password. Do not specify the password explicitly!

## Optional parameters

You can specify optional parameters to mount the volume.

**pim**  
PIM identifier.

**slot**  
When used on Linux, you can specify the slot number where the volume will be mounted.
