---
layout: post
title:  "Play Lingo in JavaScript"
date:   2015-05-16 10:18:00
categories: Game Javascript Node.js
---

Last friday at creanyx we started our official hackdays and we created a fix for contact sharing [Source](https://github.com/creanyx/groupSMS)

This friday we came up with an idea for creating a TV show game by the name of [Lingo](http://en.wikipedia.org/wiki/Lingo_(U.S._game_show)) in JavaScript. So we fired our jetpacks and did a hack session. I was working on the front end mechanics while Ahmad was working on the back end mechanics of the game.

The rules of the games are very simple.

* You have to judge a five letter word with a 5 chances in hand.
* Only first letter is given to you as a starting point.
* As an example if the word is "water" you will be given with w to start with.
* You make a guess and add the following letters, let's say you type in "wound".
* On pressing Enter the system will process your input.
* As "wound" only matches "water" with a single letter which is "w" the system will show all the letters except "w" in red.
* If you have entered "waste" then the system have shown you "wa" in green.
* If your letter is present in the final word but is not on the right location then it will be shown in blue background. This is giving you a hint that the letter is present and you can think of any other which contains the letter on a different position.
* Once you judge the correct the right word you will see a congratulations message.
* Or you can play again by pressing the playagain button.

Here is the screen shot in action.

![screenshot](https://raw.githubusercontent.com/creanyx/images/master/Screen%20Shot%202015-05-29%20at%2010.39.jpg "Screenshot")

Ali joined us in this hack and was supporting us morally. 

![relaxjs](https://raw.githubusercontent.com/creanyx/images/master/IMG_1264.jpg "Relax.JS")

You can find out the source code of our hack at [Github](https://github.com/creanyx/groupSMS).
