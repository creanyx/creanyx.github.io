---
layout: post
title: "What's a Licode"
date: 2015-08-31 11:18:00
author: Shakeel Shafique
authorbio : Shakeel is an Open Source Developer
categories: Hack Day Special 
---

Licode is an Open Source WebRTC platform which can be used to create applications which includes video/audio communication. Let’s say you want to have your own secure server deployed which can work as a video conferencing platform, licode can handle such requirements. Using Licode client side and server side API, one can record all connected participant video or audio. To do that on client side you need to execute that line in javascript.

`` room.startRecording(localStream);``

After that a message is send to server using websockets to record video and in return server returns videoid, if video ID is returned that means video recording has been started successfully. Now, server side save that video in “mkv” format with a little poor video quality and “mkv” is too much compressed file. Now problem is HTML5 video player do not support “mkv” video format. I experienced that issue when I was developing an app in licode. After spending 5 hours on google searching solution came into my mind was to convert recorded video to mp4 using ffmpeg right after “stopRecorder” event is called.

Now “stopRecorder” event implementation is in file “licode/erizo_controller/erizoController/erizoController.js”. So open that file and locate that function in that file

``socket.on('stopRecorder', function (options, callback)``

and at the end of that function write these 

``var from = GLOBAL.config.erizoController.recording_path + recordingId + '.mkv';``
``var to = GLOBAL.config.erizoController.recording_path + recordingId + '.webm';``

Where “from” variable has path of video which has been recorded and saved by licode, and “to” variable has name and path of converted file which will be created after conversion. Now we have recorded video path. So next step is to convert it which is 

`` exec("ffmpeg -i "+from+" "+to+" "); ``

Now “exec” is function in node js which is used to execute commands in shell. So, in that we are asking ffmpeg to convert an mkv recorded video to “webm” and “webm” is format which all major browsers video tag supports. If you want to convert video to “mp4” you need to do that

``var from = GLOBAL.config.erizoController.recording_path + recordingId + '.mkv';``
``var to = GLOBAL.config.erizoController.recording_path + recordingId + '.mp4';``

``exec("ffmpeg -i "+from+" "+to+" ");``

Its that simple. Now just pass that path to video tag 
<pre><code> 
<video width="320" height="240" controls>
    <source src="path/of/your/video.webm" type="video/webm"> <!-- “webm” or “mp4” -->
    Your browser does not support the video tag.
</video>
</code><pre>

(Note: For conversion you need to install “ffmpeg” installed on “ubuntu”. To install “ffmpeg” please read and follow that article)
http://linuxg.net/how-to-install-ffmpeg-2-4-2-on-ubuntu-14-04-linux-mint-17-elementary-os-0-3-deepin-2014-and-other-ubuntu-14-04-derivatives/>

