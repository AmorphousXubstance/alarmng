# Alarm!NG
Alarm!NG (Pronounced alarming) is a light, fast &amp; simple python &amp; curses based TUI alarm clock implemented on systemd.timer (requires systemd). It is built on the principle of simplicity and reliability. While still in its beta stage with a lot of possible bugs and missed chances at optimization, Alarm!NG currently aims to provide all the features required to help users who use crontabs or basic timer functionality to have a dedicated lightweight application (~66kb without the alarm track) to set alarms. It is meant to have the same performance with more intuitive features without the same overhead of precision and requirements while programming the conventional alarm shell script.
<img width="1366" height="690" alt="splashscreen" src="https://github.com/user-attachments/assets/7ae9b283-43be-4bb7-b162-be9ba0377cd0" />
</br>While crontabs and shell scripts for alarms are agreeably great learning experiences all things considered, sometimes they are unreliable and hard to debug when hopping systems. Alarm!NG has been made for one to have the ability to move their alarms from system to system and back it up as desired.
<img width="1366" height="690" alt="ui" src="https://github.com/user-attachments/assets/9fb8e217-0cc4-4a07-acf1-207721c766fe" />
</br>However, the crontab experience has not been extinguished completely for those who enjoy manual entry into set data structures. This is the reason why Alarm!NG uses a .txt plaintext file to store alarms with specific delimiters (which may be changed in the future to accomodate more character flexibility). As clearly specified in the man page as well, Alarm!NG's engine has the ability to operate headlessly by just appending your desired alarm in the specified structure.
<img width="1366" height="694" alt="image" src="https://github.com/user-attachments/assets/d5b70102-ab34-4761-aead-85dd37c10378" />

## Dependencies
Since Alarm!NG was made to step away from shell scripts (which usually use a remarkable piece of software known as [MPD]), it refrains from using any supporting daemons and keeps the dependencies as light as possible. It uses pw-play to play the audio and very soon support for pulseaudio & alsa will be added as well (the way the engine functions, these can be used interchangeably; if required, one may change the 'pw-play' to their preference).
### Current Dependencies:
* <b>python</b>
> Libraries - configparser, curses, os, signal, subprocess, time (almost always comes with any installation of python/linux)
* <b>pipewire</b>
> pw-cat suite, pw-play specifically
* <b>systemd</b>
> Service and Timer units specifically

## What Next?
Alarm!NG will be further developed to include things such as simple timers, pomodoro timers, etc. Since the superposition of time and audio has already been explored in this project, any possible permutation and intersection of these two might be added in the future.

## Why?
Originally made for myself, I decided to release Alarm!NG in case anyone else requires the same functionality as me. It also comes with an original alarm track which can be replaced at any time with your own track from the TUI or using the config file.
</br>However, I do believe people usually learn from every project. For me, this happened to be learning how to license software and more specifically media that comes with software. In this case, the very simple wav file here is CC-BY-4.0. Unlike software where you include your copyright with the license text usually as a comment in your executable and a copy of plaintext license, you must write licenses for media files into the metadata.

[MPD]: https://www.musicpd.org/
