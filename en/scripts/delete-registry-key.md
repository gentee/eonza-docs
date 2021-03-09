---
title: Remove Windows Registry Key
desc: The command deletes the Windows registry key with all its subkeys.
img:
   delete-registry-key: scripts/delete-registry-key.png
html:
   delete-registry-key: '<img src="%img.delete-registry-key%" style="margin: 1em 1em;"/>'
---
# Delete Registry Key

The **Delete Registry Key** command deletes the specified Windows Registry key with all subkeys.

%html.delete-registry-key%

**Root Key**  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry key to be deleted. The specified key will be deleted with all subkeys.

``` txt
Software\My Application\Data
```

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
