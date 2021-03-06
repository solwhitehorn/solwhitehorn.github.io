---
layout: page
title: The Nintendo Switch - A port machine
subtitle: Why it is the best porting system
illustration: /images/20200507-switch/logo.png
categories: [articles]
tags: [gaming, nintendo switch]
comments: true
---


### Why the Nintendo Switch might be the best porting system

The Nintendo Switch was released just a little bit than 3 years ago on March 2017. At the end of March 2020, Nintendo has already sold more than 55 million of units worldwide[¹](https://www.nintendo.co.jp/ir/en/finance/hard_soft/index.html). Lately, the COVID-19 situation boosted the sales as a lot of people under lockdown were looking for new sources of entertainment[²](https://www.theverge.com/2020/4/21/21229666/nintendo-switch-march-npd-sales-playstation-4-xbox-one-animal-crossing)

The success recipe of this platform is simple: the handheld and dock modes give versatility on how and where you can play; great first party games from well know franchise serving as a system seller (*The Legend of Zelda: Breath of the Wild*, *Splatoon 2*, *Super Smash Bros Ultimate*, *Mario Odyssey*, etc...) but also a lot of great interdependent game that were already successful on the PC (*Stardew Valley*, *Shovel Knight*, *Hollow Knight* or *Cuphead*) and the addition of a cheaper *"Lite"* model in Sept. 2019.

However I would like to focus on a specific category of game released on the Switch. At its release in 2017 one of the major critic was its lacks of new IPs and games[³](https://www.businessinsider.fr/us/nintendo-switch-third-party-games-support-2017-2). or that only ports of Wii U games were announced (e.g. *BOTW*; *Mario Kart 8 Deluxe*). Instead of following this argument, I would argue on the contrary that the Switch makes the perfect porting system for last gen system and even older titles. To make my point we will first discuss what are the requirements for porting a game to a system. Then let's have a look at some port that were well executed as well as poorly ported ones. And meanwhile, why don't we imagine what the Switch as yet to offer on the nostalgia road.

## 1. Porting a game

When speaking about game porting, most of us are thinking about console games ported to the PC world aka "*Console Port*". However in the recent years, porting games from other platforms to a different/newer console is more and more prevalent. 

Do you remember how we were able to play first generation title from the Game Boy on the Game Boy Color and then with the Game Boy Advance. In this case it's not a port of the game, its ensuring "*retrocompatibility*" or "*backward compatibility*", meaning that the newer system is able to run software from older generations. Sony's PS2 did the same with PS1 games and Microsoft added the same principle to the Xbox One. In some of this cases, the newer system emulates the older one to run the software, therefore there is no need to adapt the existing game code. This is something that was very popular in the 90s and early 2000s where the newer system would advertise it's backward compatibility, therefore artificially increasing its game catalog at release. 

So what about porting? Porting is the process a game undergoes during development in which a finalized version on one platform is converted for usage on another[⁴](https://www.giantbomb.com/porting/3015-988/). This is a necessary step when you need to run a game software which code is not designed to run on the system it is being ported to.

A requisite that you can't do without is the source code. This is the code that you are going to translate into the new system with the goal to have it run like it was intended. Through time however, it is not rare that the source code has been lost. One of the latest example is how Square lost the source code to Final Fantasy VIII, therefore a port was impossible and they have to opt for a remake. Or take this one, Blizzard losing the source code and the assets of the original Starcraft[⁵](https://arstechnica.com/gaming/2017/06/hands-on-with-starcraft-remastered-ahead-of-its-august-14-launch-for-15/).

Speaking of the assets, they are the other ingredient that you need. They are the textures, polygon models, text and dialogues, sound effects and musics, etc... But if they are missing or incomplete, it is far easier to create them from scratch in comparison to the source code. 

Other things you need; the SDK related to the system you are porting to and a good knowledge of its hardware architecture in order to have an idea on how the code is going to interact with it.

Now that we know what a port is, let's have a look at some games that were ported to the Nintendo Switch, how they did so and what are the results.

<br>

## 2. Ports on the Switch

As we said earlier, the Switch is known to host a lot of ports from other system. However we have to differentiate the port from *retrogames* (I include the 5th generation with the PS1, N64 and Sega Saturn) and ports from the few last generations of systems (let's say at least from the 6th generation with the PS2, Xbox and Gamecube to current systems). 

There is not much to say about retrogames as I don't necessary think that they are challenging to port nowadays (at least to the Switch). First, most of the times they already have been ported to different systems multiple times. Secondly, most of them are run through emulators rather than being ported directly to the new architecture. As mentioned before, the worst that can happen is if the source code is lost. Then it's a whole different story.

Then there is third party ports, that's when a subcontractor is in charge of porting the game to the targeted system. In the case of the Switch, there is a lot to say about these ports. Some are really interesting technically while other are a thing straight out of a nightmare. When possible I will compare the minimum requirement for the game if it has been released on PC. If not, it will be compared to the performance of their console version (i.e. PS4 or Xbox One S).  



Good ports

* DOOM - ported by Panic Button

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/6lRpoGucGA0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

Doom 2016 was considered as one of this *impossible* game to port on the Switch. We are talking about a fast paced, action oriented new gen FPS. A quick look at the minimum specs for PC vs the Switch's hardware will let you see why it was a challenge to port:

|                | PC Minimum Specs |     Switch specs      |
| -------------- | :--------------: | :-------------------: |
| **CPU**        | i52400 - 3.4 GHz | ARM Cortex - 1020 MHz |
| **GPU**        |   GTX670 - 2GB   |    Tegra - 768 MHz    |
| **RAM**        |       8 GB       |       4 GB DD4        |
| **Disk Space** |      55 GB       |         32 GB         |

There is no need to comment further. The Switch is largely under the minimal specs required for the PC version of the game. So how did they manage to port it?

The first thing to mention is that Panic Button manage to port the totality of the original levels with every stages being in its complete form. In the same manner, all enemies, weapons and features from the PC release are on the Switch version which is a very good thing. However a large number of compromises had to be done, especially in the graphic department.

The image quality is obviously lower than the PC counterpart, with a resolution scaled down to around 720p (since patch 1.2). But this resolution is not fixed and Panic Button implemented adaptive resolution meaning that it can go further down in order to maintain a constant framerate. Talking about framerate, the target is 30 FPS but it can drop to 20 when a lot of enemies are on screen. A funny consequence from this is that lower difficulties with fewer enemies exhibits better framerates while higher difficulties are penalized by important drops when the action gets heavy. Among other things we can mention: the FOV is locked at 90; DOF and alpha effects are rendered at 25% of the initial resolution (so around 360p); lighting and reflections effects are reduced or removed; ambient occlusion effects are reduced and color gradients are sometimes removed. 

One of the major downfall of this port is the framepacing, i.e. that frame are persisting on screen for a variable amount of time. Digital Foundry did an excellent job at documenting this effect on the docked version of the game. An other thing they put in evidence is that the video settings are globally below the PC lowest setting. Not a surprise considering how demanding this game is. 

Overall, even with all of these compromise, Doom 2016 on the Switch is still a impressive port as Panic Button managed to keep what's make the essence of the game: fast paced, gory, intense, demon hunting. The loading time are even quite similar to the one the base PS4 according to Digital Foundry. And to top that, the portable mode is as good as the docked mode which is the most interesting feature of this port, being able to slay demons on the go.



*take screenshot from digital foundry videos



* The Witcher 3 - ported by 

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/Ql2BJiDg7hY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>



* Divinity Original Sins 2 - ported by 

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/Cf_eCJl5-ts" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>



* FF XII - TZA - ported by 

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/uz5qP0R0Wgo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

---

Bad ports



* Bloodstained: Ritual of the Night

video



* Rime
* ARK
* WWE 2K18
* PayDay 2





* Skyrim

toaster video



## 3. Porting ahead























sources:

https://www.giantbomb.com/porting/3015-988/

https://room8studio.com/news/games/abzu-on-nintendo-switch-how-to-successfully-port-a-game/

https://room8studio.com/news/games/top-5-game-porting-tips-for-the-nintendo-switch/

https://gamasutra.com/view/news/222363/What_exactly_goes_into_porting_a_video_game_BlitWorks_explains.php