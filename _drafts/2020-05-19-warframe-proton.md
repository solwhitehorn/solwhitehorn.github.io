---
layout: post
title: How to play Warfarme in Linux with Steam Proton
subtitle: Yes, you can be a Space Ninja in Linux too
illustration: /images/newspaper.png
categories: [blog]
tags: [tuto, linux, proton, steam, gaming]
comments: true
---

### Here is how to play Warframe in Linux with Steam Proton

<br>

---

Lately I've been craving so fast-paced action game and Warframe is one of the best free games that I know of. I haven't play the game since a couple of years and at the time I was still using windows. 

Before playing any games on Steam that are not natively ported to Linux, I check it under [protondb.com](www.protondb.com). For Warframe, the report are kind of a mixed bag but the overall rating is *gold* meaning that you should be able to run quite easily. 

There is two way to install and play the game with impressive performance:

#### First option:

* install it normally. However, before launching the game, specify in the properties that you want to use proton 4.8 

**insert screenshot**

* Let the launcher do its update. It will probably crash if you try to play it. Once the update is done, close the launcher, and this time, you want to use the latest version of proton and add this launch command: 

  `WINEDLLOVERRIDES="xaudio2_7=n,b" %command%`

* The launcher should start fine. It will ask if you want to pre-charge some game files, let it do so, it will however take some time. Be patient.

After that everything should run smoothly.

  

#### Second option:

* You can also use Proton Glorious Eggroll, a custom version of proton that currently fixes a lot of problem with certain games (i.e. Resident Evil 2 remake; Monster Hunter World, FFXIV, etc...).

* Follow the instruction on the github page for installation: [https://github.com/GloriousEggroll/proton-ge-custom](https://github.com/GloriousEggroll/proton-ge-custom)

* Then as before, install the game and run it a first time using proton 4.8, let the launcher make the updates. Don't specify any launch commands, they are not necessary this time.

* Close the game, specify the proton version to use, this time select proton GE and let the launcher to its thing.  



On my setup, I had to deactivate Vsync and fix the framerate to 60 FPS. It seems that people are running the game fine whiteout these changes so you should try in regard to your performance, especially if you encounter micro-stuttering.

As always, enjoy and here is a example on how it runs with my rig under Ubuntu 19.10:

**instert youtube video**





<br>

---



