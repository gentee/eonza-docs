---
title: Delete Windows Registry values
desc: This command removes one or more Windows registry values.
img:
   delete-registry-value: scripts/delete-registry-value.png
html:
   delete-registry-value: '<img src="%img.delete-registry-value%" style="margin: 1em 1em;"/>'
---
# Delete Registry Value

The **Delete Registry Value** command deletes the Windows Registry values ​​in the specified subkey.

%html.delete-registry-value%

**Root Key**  
Specify the Registry root key.

**Subkey**  
Specify the name of the Registry key in which you want to delete the value.

``` txt
Software\My Application\Data
```

## Values for deleting
You can specify one or more values that you want to delete.

**Value Name**  
The name of the value to be deleted. If an empty string is specified, the default value will be deleted.

**Access**  
Access for keys of 32-bit or 64-bit applications.

* *---* - default access.
* *WOW64_32KEY* - access to the Registry keys for 32-bit applications.
* *WOW64_64KEY* - access to the Registry keys for 64-bit applications.
