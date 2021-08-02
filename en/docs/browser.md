---
title:  Browser tab
desc: Documentation for the Browser tab of the Eonza program.
img:
   browser: browser.png
   browser-edit: browser-edit.png
html:
   browser: '<img src="%img.browser%" style="margin: 1em 1em;"/>'
   browser-edit: '<img src="%img.browser-edit%" style="margin: 1em 1em;"/>'
---
# Browser

**v1.20.0**  
There is a [Chrome extension](chrome-extension.html), which can be used to run Eonza scripts. Here you can specify the scripts that will be available to run in the Chrome extension. If you are using Pro version and you have several users, they can also use the browser extension, but they will see only those scripts
to which they have access.

%html.browser%

## List of scripts

Specify the list of sites and scripts that will be available to run from the browser.

### URLs

In this field you should specify a list of site addresses. You can specify one site per line or separate them with spaces.
If this field is empty, the corresponding scripts will be shown for all sites in the browser. If the site address starts with *http*, then the beginning of the addresses is compared. For example, you specified *https: //mysite.com/*, then these scripts will be available in the browser on the pages *https://mysite.com/mypage.html, https://mysite.com/docs*, but will be absent on the pages *http: //mysite.com/, https://www.mysite.com*. If the url address does not begin with *http*, then
scripts will be available for all sites that contain the specified substring. For example, you specified *bank*. In this case,
scripts in the extension will be available at *mybank.com, banki.ru, mysite.com/banks.html* sites.

## Scripts

Specify one or more comma separated scripts that will be available from the browser extension on the corresponding sites. By default, a JSON string with the following fields is passed to the *#.data#* constant when the script is called.

* **url** - current URL in the browser;
* **title** - title of the current page in the browser;
* **html** - sources of the current HTML page. The page content is transmitted only if the *Get HTML Content* checkbox is checked.

%html.browser-edit%

### Get HTML Content

Select this checkbox if you want to fetch the HTML content of the page when the script runs. In this case, you will not need to additionally request the HTML page for parsing.
