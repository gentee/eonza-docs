---
title: Settings tab in the Pro version
desc: Documentation for the Settings tab in the Pro version of Eonza.
img:
   pro-security: pro-security.png
   pro-security-users: pro-security-users.png
html:
   pro-security: '<img src="%img.pro-security%" style="margin: 1em 1em;"/>'
   pro-security-users: '<img src="%img.pro-security-users%" style="margin: 1em 1em;"/>'
---
# Settings

**Autofill Forms**  
Check this box if you want to [save entered data](autofill-forms.html) in forms. In this case, the saved values will be substituted in the form fields on the next run. It is also possible to save several variants for filling out the form.

## Security

The Pro version provides additional features for safe work in the Eonza program.

%html.pro-security%

**Two-factor Authentication**  
If you installed the program on a VPS / VDS hosting or a remote server, be sure to enable [two-factor authentication](two-factor-authentication.html). In this case, after entering the password, the user will have to specify a one-time numeric code from a special program in the mobile phone. Two-step authentication helps prevent unauthorized access to the program if the password is leaked. If the user loses access to the cell phone, click the two-factor authentication reset button in the user list.

%html.pro-security-users%

**Logout All Users**  
Click this button if you want to log out all users. For example, it is recommended to do this after updating the program. If you enable two-factor authentication, then the program automatically log out all users.