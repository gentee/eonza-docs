---
title: Duplicate File Finder
desc: The script finds duplicate files and saves them to a file.
img:
   duplicate-file-finder: packages/duplicate-file-finder.png
   duplicate-file-report: packages/duplicate-file-finder-report.png
html:
   duplicate-file-finder: '<img src="%img.duplicate-file-finder%" style="margin: 1em 1em;"/>'
   duplicate-file-report: '<img src="%img.duplicate-file-report%" style="margin: 1em 1em;"/>'
---
# Duplicate File Finder

The **Duplicate File Finder** script searches for identical files in the specified directory and all subdirectories. Files are considered the same if they have the same size and **MD5** hash. The command saves information about found files to a text file in YAML, JSON, CSV or HTML format.

%html.duplicate-file-finder%

**Path**  
Specify the directory in which to search for duplicate files. Identical files will be searched in all subdirectories.

**Wildcard or RegExp**  
**Exclude Wildcard or RegExp**  
These parameters are described in command [Foreach File](/scripts/foreach-file.html).

**Output File**  
Specify the name of a file in which information about found files will be saved. If the file extension is *yaml*, *json*, *html*, the file list will be saved in the corresponding format. For example, a fragment of YAML file:

```yaml
- size: 1890
  md5: "ae9d4728d7113094397b29c5001384ae",
  list":
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.66.2/testdata/full.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/full.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/full.ini"
- size: 8943
  md5: "17faebcd8a80fc6ffff1fad0b3bc2473",
  list":
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/multiline.ini"
     - "/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/multiline.ini"
```

If the file has a different extension or there is no extension, then the information will be saved in CSV format. For example:

```txt
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.66.2/testdata/full.ini
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/full.ini
1890,ae9d4728d7113094397b29c5001384ae,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/full.ini
8943,17faebcd8a80fc6ffff1fad0b3bc2473,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.62.0/testdata/multiline.ini
8943,17faebcd8a80fc6ffff1fad0b3bc2473,/home/ak/go/pkg/mod/gopkg.in/ini.v1@v1.64.0/testdata/multiline.ini
```

If **Output File** is not specified, a report on found duplicate files will be created and displayed.

%html.duplicate-file-report%
