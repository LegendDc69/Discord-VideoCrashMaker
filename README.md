<div align="center">
  <br />
  <p>
    <a href="https://github.com/AstraaDev"><img src="https://files.readme.io/d14112d-Cloudsmith-Integrations-Banner-GitHub.png" width="1000"></a>
  </p>
</div>

# Discord VideoCrashMaker [![Build Status](https://img.shields.io/badge/covarage-100%25-succes)]() ![Profile views](https://gpvc.arturio.dev/AstraaDev)

> Convert the video of your choice into an identical video except that it can crash any discord when playing (uses FFmpeg method).

# Features
 - FFmpeg need to be install.
 - Possibility to choose the time at which the video should crash.

# How to use
 1. [Install FFmpeg](https://www.youtube.com/watch?v=GI7JGouGPsE) (unless already done).
 2. Launch [videocrashmaker.bat](videocrashmaker.bat).
 3. Enter the path to the video file and enter the time when the video should crash.
 4. Wait...

# How does it work?
First of all, this is not something directly related to Discord. Discord's desktop application is developed with Electron, which uses Chromium for rendering engine. Chromium's video playback is really awful. Actually it's the problem. If you download those old crasher videos and play it on your VLC or FFplay, you will notice that it'll be played just fine. So, why Chromium fails to play the video? If you remember, we just divided our video into two parts. First part was from 0 second to 0.1 second. The second part was the rest. And as you will remember, we changed second part's pixel format to YUV444p. Then we just combine them. When Chromium opens the video, it only checks for the first part. It's YUV420p, which your CPU and GPU can decode. Then Chromium decides to decode the video on your hardware. But after 0.1 second, YUV444p part stars. Chromium doesn't support changing resolution or pixel format while playing the video. So this is the first killer. Second bad thing is, it's really high likely that your hardware doesn't support decoding YUV444p. But Chromium decided to decode the video on your hardware anyways. So Chromium fails to decode the video, which results in freezing the whole Discord desktop application.

# How can I avoid crasher videos?
  1. Open Discord
  2. Go to User Settings, then navigate to Advanced.
  3. You will see an option named "Hardware Acceleration".
  4. Disable it and restart your Discord.
=> Now, all of the videos you watch will be decoded by the software.

# Caution
This script is for educational purposes. I am in no way responsible for any inconvenience.

# Credits
My GitHub: [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg' alt='github' height='30'>](https://github.com/AstraaDev)  My Twitter: [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg' alt='twitter' height='30'>](https://twitter.com/AstraaDev)  My WebSite: [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/icloud.svg' alt='website' height='30'>](http://astraadev.club)  
<br>
[![Astraa's GitHub stats](https://github-readme-stats.vercel.app/api?username=AstraaDev)](https://github.com/AstraaDev/github-readme-stats)

# Donate
Support this project and [others](https://github.com/AstraaDev) by Astraa via [PayPal](https://www.paypal.com/).
<br>
<br>
<a href="https://www.paypal.me/fmrhrt/">
  <img alt="Support via PayPal" src="https://cdn.rawgit.com/twolfson/paypal-github-button/1.0.0/dist/button.svg"/>
</a>
