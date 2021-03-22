---
title: Working with timers in the Eonza program
desc: Documentation for working with timers in the Eonza program.
img:
   timers: timers.png
   timer-cron: timer-cron.png
html:
   timers: '<img src="%img.timers%" style="margin: 1em 1em;"/>'
   timer-cron: '<img src="%img.timer-cron%" style="margin: 1em 1em;"/>'
---
# Timers

Timers allow you to set automatic launching of scripts at regular intervals. The minimum interval between timer activations is one minute. If you want to perform some actions more often, then you need to create a script with an infinite loop and [pauses](/scripts/sleep.html) in the required number of seconds. The timers only work when the Eonza program is running.

%html.timers%

The list of created timers is sorted by the nearest start time. Each timer in the table has a name, starting frequency in **Cron** format and the name of the script to be launched.

## Timer parameters

%html.timer-cron%

* **Name**  
Timer name.

* **Script**  
The system name of the script. The script should not have parameters, otherwise, it will wait for the input of parameters at startup.

* **Disabled**  
Check this box if you want to stop the timer.

In the fields below, you can specify specific values or ranges of values ​to trigger the timer. The values are separated by commas. In the right column, you can specify the corresponding intervals.

* **Minute/Every [?] minutes** - possible values 0-59.
* **Hour/Every [?] hours** - possible values 0-23.
* **Day/Every [?] days** - possible values 1-31.
* **Month/Every [?] month** - possible values 1-12.
* **Week/Every [?] weeks** - possible values 0-6. The week starts on Sunday.

For example, let the following parameters be specified

``` txt
Minute: 0 / Every 15 minutes
Hour: 9-17,21-23
Day: 1 / Every 2 days
```

This means that the timer will run the script on odd days every 15 minutes (0, 15, 30, 45) from 9 am to 5 pm and from 9 pm to 11 pm inclusive.
