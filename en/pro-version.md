---
title: PRO version of the Eonza program
desc: Questionnaire about the PRO version of the Eonza program.
res:
   dis: What are the disadvantages of the current version?
   scripts: What scripts should be added to the standard library?
   features: What features would you like to see in the free version?
   feedback: What needs to be done to organize a community? What is the best way to organize user feedback?
   pro: What features can be implemented in the Pro version?
   cost: How much can an annual Pro license cost?
   email: Please enter your <b>email address</b> if you want to get 50% discount on the PRO version. This is not a mailing list subscription, the email will be sent only once after the release.
   send: Send
   success: Thank you very much. Your opinion will help us improve the program.
html:
   pro: |-
      <div style="max-width:700px;margin-top: 1em;">
        <div  class="notification is-success" v-show="success" style="display:none;">
        <button class="delete" @click="success = false"></button>%res.success%</div>
        <div  class="notification is-danger" v-show="error" style="display:none;"><button class="delete" @click="error = ''">
        </button>{{error}}</div>
        <div  v-show="form">
            <div class="field"><label class="label">%res.dis%</label>
            <div class="control"><textarea class="textarea" v-model="dis"></textarea></div>
            </div>
            <div class="field"><label class="label">%res.scripts%</label>
            <div class="control"><textarea class="textarea" v-model="scripts"></textarea></div>
            </div>
            <div class="field"><label class="label">%res.features%</label>
            <div class="control"><textarea class="textarea" v-model="features"></textarea></div>
            </div>
            <div class="field"><label class="label">%res.feedback%</label>
            <div class="control"><textarea class="textarea" v-model="feedback"></textarea></div>
            </div>
            <div class="field"><label class="label">%res.pro%</label>
            <div class="control"><textarea class="textarea" v-model="pro"></textarea></div>
            </div>
            <div class="field"><label class="label">%res.cost%</label>
            <div class="control"><input class="input" type="text" v-model="cost"></div>
            </div>
            <div class="field">
            %res.email%
            <div class="control">
            <input class="input" type="email" v-model="email" placeholder="e.g. alexsmith@gmail.com">
            </div>
            </div>
            <div class="field" style="display: flex;margin-top: 1em;">
            <div class="control">
            <button class="button is-primary" @click="send">
            %res.send%
            </button>
            </div>
            </div>
        </div>
      </div>
---
# PRO version

Financial resources are needed to develop a free open-source program, so we plan to develop and release a PRO version. It will have features that will make the work with the program more convenient, but will not affect the main functionality. Let's immediately note the following points:

* All scripts will work in any version.
* Pro version will be sold as a one-year license, which will cover all updates for a year.
* Estimated release time for the Pro version is April-May 2021.
* Updates of the free version will continue to be released 1-2 times a month.

We invite you to answer the questions below to get a perspective and choose the direction of the program's development. You can fill in only those fields that interest you.

%html.pro%
