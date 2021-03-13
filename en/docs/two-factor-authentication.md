---
title: Two-factor authentication in Pro version
desc: Two-factor authentication in the Pro version of the Eonza program.
img:
   twofa: twofa.png
html:
   twofa: '<img src="%img.twofa%" style="margin: 1em 1em;"/>'
---
# Two-factor Authentication

Two-factor authentication protects the Eonza program from unauthorized access in case of a password leak. This is important if you use Eonza on a VPS hosting or remote server. If two-factor authentication is enabled, the user has to enter a password and a one-time numeric code which is constantly generated on his cell phone.

**Step 1: Install Google Authenticator**  
You will need to install **Google Authenticator** (Andorid, iOS) on your cell phone in order to receive your one-time passwords. You can use **Microsoft Authenticator** (Android, iOS) or **FreeOTP** (Android, iOS) instead of Google Authenticator.

**Step 2: Scan the QR code**  
The first time, after entering your password, you will see a QR code. Scan it with Google Authenticator to have the app create a new account. After that, Google Authenticator will generate a new numeric code every 30 seconds.

%html.twofa%

**Step 3: Enter your current numeric code**  
Enter your current Google Authenticator numeric code into the one-time password field, and click the *Login* button.

Two-factor authentication is available in the Pro version only.
