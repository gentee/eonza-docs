---
title: Terminate the script with an error
desc: The command terminates the script with an error.
img:
   error-1: scripts/error-1.png
   error-2: scripts/error-2.png
html:
   error-1: '<img src="%img.error-1%" style="margin: 1em 1em;"/>'
   error-2: '<img src="%img.error-2%" style="margin: 1em 1em;"/>'
---
# Error

The **Error** command terminates the script with the specified error. Information about the error is written to the log file.

%html.error-1%

**Error Message**  
Enter the error text.

**Error Code**  
You can specify a numeric code that the program will return when terminating the script. The default value is **100**.

If an error occurs, the script window will look like this.

%html.error-2%
