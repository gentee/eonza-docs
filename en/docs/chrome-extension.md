---
title: Eonza Chrome Extension
desc: How to install and configure the Eonza extension for Chrome browser.
img:
   chrome-ext-install: chrome-ext-install.png
   chrome-ext: chrome-ext.png
   chrome-ext-start: chrome-ext-start.png
   chrome-ext-settings: chrome-ext-settings.png
   chrome-ext-run: chrome-ext-run.png
html:
   chrome-ext-install: '<img src="%img.chrome-ext-install%" style="margin: 1em 1em;"/>'
   chrome-ext: '<img src="%img.chrome-ext%" style="margin: 1em 1em;"/>'
   chrome-ext-start: '<img src="%img.chrome-ext-start%" style="margin: 1em 1em;"/>'
   chrome-ext-settings: '<img src="%img.chrome-ext-settings%" style="margin: 1em 1em;"/>'
   chrome-ext-run: '<img src="%img.chrome-ext-run%" style="margin: 1em 1em;"/>'
---
# Chrome Extension

You can install and use the Eonza extension for Chrome browser. This extension allows you to run scripts that have been defined in the [Browser tab](browser.html). When you run the script, the URL address and the title of the current page in the browser are passed to it. Also, the content of the HTML page can be passed to the script. The extension will work in any browser that supports Chrome extensions. Let's see how to install and configure this browser extension.

## Installing the extension

You can download and build the extension yourself from the sources located at [repository on github.com](https://github.com/gentee/eonza-chrome). The easiest way is to [**download ready-made archive**](https://github.com/gentee/eonza-chrome/releases/download/v1.0.0/eonza-chrome.zip) and unpack it into any directory.

After the extension files have been unpacked, launch your browser and open the page with extensions. This can be done in the settings section or by specifying *chrome://extensions/* in the address bar. Turn on the **Developer mode** and click on the **Load unpacked** button. Specify the directory with the unpacked files in the directory selection window.

%html.chrome-ext-install%

After the extension has been installed, click on the extension icon and then on the *Pin* button to make the extension icon appear permanently in the address bar.

%html.chrome-ext%

## Configuring the extension

After the extension is installed, click on its icon and a window with the *Settings* and *Help* buttons should appear.

%html.chrome-ext-start%

Click on the *Settings* button to specify the address of the Eonza application.

%html.chrome-ext-settings%

Now you need to add scripts to [Browser tab](browser.html) in Eonza application. For example, you can add *url.title* (Copy URL & Title) script, which will copy URL and title of the current page in the browser to the clipboard.
If all the settings are correct and the Eonza program is running, you should see a list of scripts in the extension. Note that if Eonza is password-protected, you should open it in the browser in a separate tab. In this case, authentication will occur automatically.

%html.chrome-ext-run%

Two buttons are shown for each script. If you click on the big button with the name of the script, it will be launched and opened in the browser. If you click the right arrow button, the script will run in hidden mode. When launching, the script passes JSON string with URL and title of the current page to the *#.data#* constant. Also, the HTML content of the page can be passed for parsing.
