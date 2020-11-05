---
title: Eonza Automation Software | Official site
desc: Eonza is free, open source, cross-platform automation software.
img:
   eonza-1: eonza-1.png
   eonza-2: eonza-2.png
res:
   contacts: Contacts
   features-md: |-
      ## Key features

      * Creating scripts does not require knowledge of programming languages.
      * There is a constantly updated library of built-in scripts.
      * **The program can be installed on a remote server or VPS/VDS hosting and managed from a browser**.
      * Protection by password and using a "white list" of IP-addresses.
      * Quick search for scripts.
      * You can launch scripts from the console.
      * Saving logs and console output for each completed task.
      * Export/import of scripts to/from a text YAML file.
      * It is possible to suspend, resume and terminate script execution.
html:
   home: |-
      <div style="margin: 1em 0em;" class="columns">
      <div class="column is-two-thirds">
      %res.features-md%
      <div style="margin-top: 1rem;">
      <a class="button is-medium" title="%onlinedemo%" style="text-decoration:none;margin-bottom:1rem;color: #fff;
       background-color: #3273dc;margin-right: 1rem;" href="https://playground.eonza.org" @click="trackplay('home')" target="_play">
      <span class="icon">
      <i class="fas fa-caret-square-right"></i>
      </span>
      <span>%playground%</span>
      </a>

      <a class="button is-medium" style="text-decoration:none;margin-bottom:1rem;color: #fff;
       background-color: #3273dc;margin-right: 1rem;" href="downloads.html">
      <span class="icon">
      <i class="fas fa-download"></i>
      </span>
      <span>%downloads%</span>
      </a>

      <a class="button is-medium" style="text-decoration:none;margin-bottom:1rem;" 
      target="_blank" href="https://github.com/gentee/eonza">
      <span class="icon">
      <i class="fab fa-github"></i>
      </span>
      <span>GitHub</span>
      </a>
      </div>
      <h2>%res.contacts%</h2>
      <ul>
      <li><a href="https://github.com/gentee/eonza/issues">GitHub issues</a></li>
      <li><a href="mailto:eonza.dev@gmail.com?Subject=Eonza">eonza.dev@gmail.com</a></li>
      </ul>
      </div>
      <div  class="column" style="padding-left: 1em;max-width: 350px;">
      <a href="%img.eonza-1%"><img src="%img.eonza-1%" style="margin: 1em 1em;width: 300px;"/></a>
      <a href="%img.eonza-2%"><img src="%img.eonza-2%" style="margin: 1em 1em;width: 300px;"/></a>
      </div>
      </div>
---
# Software for script management

Free, open source cross-platform program for working with scripts and automating actions on the computer.

* **It does not require installation. Save the program to any directory and run it.**
* **Free, cross-platform, open source.**
* **Software does not require any additional programs or packages.**
* **Graphical interface is implemented in HTML+JavaScript and opens in the browser.**

%html.home%
