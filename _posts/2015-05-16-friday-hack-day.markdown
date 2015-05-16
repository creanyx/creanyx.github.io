---
layout: post
title:  "Hack days at Creanyx are Fridays!"
date:   2015-05-16 10:18:00
categories: Hacking Twilio Node.js
---

At Creanyx we are oganizing Hackdays on Fridays. We will spend half of the day wokring on awesome new ideas as well as contributing to open source community.

This Friday we worked to solve a paticular problem that I faced once I went for Hiking. Here in Islamabad where we go for hike, we have a bad reception for 3G and a common problem to get in connection with new hiking group members is the need to share contact numbers.

Here is the scenario: I went for hiking and I meet 5-6 new hiking members and we want to share contact numbers with each other, one solution is that I visit each member and collect the number and every other member has to do same. This can be good for small numbers but it can go wild if members are greater in number.

There is an obvious solution that we can get in contact with each other and that is to use an online group like facebook group, but lets suppose no one is on facebook :P (obviously that is an assumtion) so for that case we all need to share each other's contact number with each other.

We solved this using Twilio and here is the breakdown of how it works:

* One of the group member sends a request to a twilio number with a paticulat text saying "list".
* Twilio number sends back a randomly generated identifier with text saying "Ask your group to send me <id> in message body with in 5mins."
* Every member sends that id to the twilio number and that's all.
* After 5 minutes each member who opted in will recieve a text message which includes the numbers of each member. 

Here is the screen shot in action.

That was fun working out. We have also introduced a space at Creanyx calling it RELAX.JS which basically says relax and write Javascript.

You can find out the source code of our hack at [Github](https://github.com/creanyx/groupSMS).

