---
title: Eonza Automation Software | Official site
desc: Eonza is free, open source, cross-platform automation software.
img:
   eonza-1: eonza-1.png
   eonza-2: eonza-2.png
res:
   alpha: Alpha
   beta: Beta
   contacts: Contacts
   emailnotice: Eonza is still under development. You can leave your email and I (the developer) will send you a personal message when the desired version is released. 
   letme: Let me know when the marked version is released
   name: Name
   nosubs: This is not a mailing list subscription, it will only be a one-time email.
   release: Release
   send: Send
   success: Thank you very much. Your application has been received.
html:
   home: |-
      <div style="margin: 1em 0em;" class="columns">
      <div class="column is-two-thirds">
      <a class="button is-medium" style="text-decoration:none;" 
      target="_blank" href="https://github.com/gentee/eonza">
      <span class="icon">
      <i class="fab fa-github"></i>
      </span>
      <span>Eonza on GitHub</span>
      </a>
      <a button class="button is-medium" style="text-decoration:none;" 
      target="_blank" href="https://github.com/gentee/eonza-assets">
      <span class="icon">
      <i class="fab fa-github"></i>
      </span>
      <span>Eonza Client on GitHub</span>
      </a>
      <div style="max-width:500px;margin-top: 1em;">
      <div  class="notification is-success" v-show="success" style="display:none;">
      <button class="delete" @click="success = false"></button>%res.success%</div>
      <div  class="notification is-danger" v-show="error" style="display:none;"><button class="delete" @click="error = ''">
      </button>{{error}}</div>
      <div  v-show="form">
      <p style="margin-bottom: 1em;">%res.emailnotice%</p>
      <div class="field">
      <label class="label">%res.name%</label>
      <div class="control">
      <input class="input" type="text" placeholder="e.g Alex Smith" v-model="name"
      :class="{'is-danger': isemptyname}">
      </div>
      </div>
      <div class="field">
      <label class="label">Email</label>
      <div class="control">
      <input class="input" type="email" v-model="email" placeholder="e.g. alexsmith@gmail.com" 
      :class="{'is-danger': isemptyemail}">
      </div>
      </div>
      <div>%res.letme%</div>
      <div class="field">
      <div class="control">
      <label class="radio">
      <input type="radio" v-model="ver" name="ver" value="beta">
      %res.beta%
      </label>
      <label class="radio">
      <input type="radio" v-model="ver" name="ver" value="release">
      %res.release%
      </label>
      </div>
      </div>
      <div class="field" style="display: flex;margin-top: 1em;">
      <div class="control">
      <button class="button is-primary" @click="send">
      %res.send%
      </button>
      </div>
      <div style="padding: 0em 1em">
      %res.nosubs%
      </div>
      </div>
      </div>
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

Status: **Alpha version**. Beta version is expected in the middle of August 2020.

* It does not require installation. Save the program to any directory and run it.
* Free, cross-platform, open source.
* Software does not require any additional programs or packages.
* The current version works through a browser.

%html.home%
