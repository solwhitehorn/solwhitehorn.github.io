---
layout: post
title: 🗞️ The News this week - May 11 to 15
subtitle: A lot happened this week 
illustration: /images/newspaper.png
categories: [blog]
tags: [news]
comments: true
---

### 

<br>

---

* Friday, May 15 2020

Let's talk about **Doom Eternal** and some strange practice that was just discovered. Bethesda made the choice to implement Irdeto's new tool called **Denuvo Anti-Cheat** (DAC) in the last major update made to Doom Eternal. This is different from Denuvo Anti-Tamper, the DRM tool supposed to guaranty anti-piracy of game softwares, that proved to be ineffective in many cases already.

DAC is advertised as being a "*technology solution (to) protect eSports and online games from cheating. Developed by security experts, Denuvo Anti-Cheat has no negative impact on in-game performance*". Further reading of the [blog article](https://blog.irdeto.com/2020/05/14/denuvo-anti-cheat-goes-live-a-message-to-doom-eternal-fans-and-gamers/) posted by Irdeto informs us in *all transparency* that Anti-Cheat "*installs a kernel mode driverd into the Program Files folder*" that starts automatically when the game starts. They also specify that DAC "*does not take screenshots, scan file system or stream shellcode from the internet. It collects information on how the OS interacts with the game and send the information to **Amazon-hosted servers** for cheat detection*".



[Arstechnica](https://arstechnica.com/gaming/2020/05/doom-eternal-anti-cheat-kernel-driver-is-safer-than-others-denuvo-says/) asked Michail Greshishchev (DAC product owner) about the alleged security concerns on which he responded:

>the company's driver has received "certification from renown[ed] kernel security researchers, completed regular whitebox and blackbox audits, and was penetration-tested by independent cheat developers." 



He also added that:

>"Unlike existing anti-cheats, Denuvo Anti-Cheat does not stream shell code from the Web," Greshishchev told Ars. "This means that, if compromised, attackers can't send down arbitrary malware to gamers' machines.

> "These same gaming machines already have a sea of subpar (security-wise) administrative services with active Internet connections," he continued. "Drivers from mouse and keyboard vendors, lighting and overclocking services, etc. If attackers really wanted to compromise gamers' machines, they would go through them—not through the world's strongest anti-tamper software."



Cool, so it's totally safe to let DAC temper with your kernel and by the way, our system are already vulnerable enough from third party driver so why not add another closed source data gathering code on top of it. That is wrong on so many level and by the way, device drivers don't operate on the same ring level as the Kernel. 

On top of that, I don't think that Denuvo as proved to completely safe from tempering. Should we remember the number of game that shipped with Denuvo Anti-Temper that were cracked, sometimes just a few days after release. 

Riot Game's **Valorant** is using a similar kernel level 0 access anti-cheat called **Vanguard Anti-Cheat** system that already raised many concerns in the community, especially as the program was loaded on start-up. 

No software should be allowed to have kernel level 0 access to your system. This is the equivalent of voluntarily installing a rootkit on your system and giving a third party the highest administrator privileges they can have on your system. Or to put it simply, giving a stranger the key to your house and your mom's number.



<br>

---

* Thursday, May 14 2020

A lot happened on this Thursday. First a new Paper Mario "**Origami King**" was announced out of nowhere with a trailer from Nintendo. 

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/FX6DTLcWUdY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

It seems that it's the kind of communication that Nintendo will use for the coming months as the COVID-19 situation is forcing a lot of compagnies to re-think their presence on various events. Words are that Nintendo will release more trailers of incoming game for what was supposed to be E3-2020 but there will no be any new Nintendo direct in the near future.

<center><blockquote class="twitter-tweet"><p lang="en" dir="ltr">Yes. No Direct, but it obviously still has games to announce. <a href="https://t.co/zBPNUJlBhQ">https://t.co/zBPNUJlBhQ</a></p>&mdash; Jeff Grubb (@JeffGrubb) <a href="https://twitter.com/JeffGrubb/status/1260933475755909120?ref_src=twsrc%5Etfw">May 14, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center> 

<br> 

The other trailer that a lot of people were waiting for was Sony's State of Play, featuring Sucker Punch Studios new IP **Ghost of Tsushima**. To be honest I was not as impressed as I thought I would be. Gameplay seems fun but not so dynamic at what was teased previously. The pace of the game is a lot slower than your typical sword action adventure. Also my first impression of the world design was not the best. I found it to be "bland" if I can use that term, something is lacking but I can't put my finger on what exactly. Anyway, enjoy the trailers if you didn't saw them already:

<center><iframe class ="iframev" width="560" height="315" src="https://www.youtube.com/embed/Ur0pQblaZcE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<br>

---

* Wednesday, May 13 2020

The big news today is the release of the Unreal Engine 5 showing a tech demo running on the PS5:

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/qC5KtatMcUw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

I was going to write a long page about what I think about this demo but I decided that it would be part of an article.

<br>

On other news, thanks to J. Vogt-Roberts, we are gifted some new codec com between the legendaries Solid Snake, Col. Campbell and Otacon:

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/e7aUWvsQ6W0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<center><blockquote class="twitter-tweet"><p lang="en" dir="ltr">I wish I could share more frequent updates on the film adaptation of <a href="https://twitter.com/HIDEO_KOJIMA_EN?ref_src=twsrc%5Etfw">@HIDEO_KOJIMA_EN</a>’s seminal METAL GEAR SOLID...<br><br>But❗️I can share this codec from the legends <a href="https://twitter.com/DavidBHayter?ref_src=twsrc%5Etfw">@DavidBHayter</a>, <a href="https://twitter.com/4pauleiding?ref_src=twsrc%5Etfw">@4pauleiding</a> &amp; <a href="https://twitter.com/christophran?ref_src=twsrc%5Etfw">@christophran</a> as we celebrate MGS and try to make the world whole again.<a href="https://twitter.com/hashtag/MGSQUARANTINE?src=hash&amp;ref_src=twsrc%5Etfw">#MGSQUARANTINE</a> <a href="https://t.co/6AE9qLL74v">pic.twitter.com/6AE9qLL74v</a></p>&mdash; Jordan Vogt-Roberts (@VogtRoberts) <a href="https://twitter.com/VogtRoberts/status/1260293444691390465?ref_src=twsrc%5Etfw">May 12, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

Jordan is going at it during all the week so I suggest you visit is twitter to see the next surprises he has for us.

<br>




<br>

---

* Tuesday, May 12 2020

Your dream of becoming a space trucker has never been so close! SpaceX, Elon Musk's aerospace manufacturer and space transportation company just released a new space simulator. 

Try yourself at docking the Crew Dragon with the ISS. The Crew Dragon is a reusable spacecraft capable of carrying 7 passengers to and from Earth orbit (and beyond as they advertise). The aim here is to dock yourself with the ISS while controlling the pitch, yawn, role and thrust of the capsule. It can be a little bit tricky if you are not accustomed to space simulation games (you should try Kerbal Space Program). 

Just a note, if you want to embark in this docking scenario, you must have all values nominal (in green and < 0.2) when approaching the station.

Have fun, space cowboy:

<center><blockquote class="twitter-tweet"><p lang="en" dir="ltr">Simulator of Crew Dragon docking with <a href="https://twitter.com/Space_Station?ref_src=twsrc%5Etfw">@space_station</a> → <a href="https://t.co/vVqJfnbuNC">https://t.co/vVqJfnbuNC</a> <a href="https://t.co/ZH3bkT0DhM">pic.twitter.com/ZH3bkT0DhM</a></p>&mdash; SpaceX (@SpaceX) <a href="https://twitter.com/SpaceX/status/1260269423090208768?ref_src=twsrc%5Etfw">May 12, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br>

---

* Monday, May 11 2020

This week starts with some new footage for the Definitive Edition of Xenoblade Chronicles on the Nintendo Switch. This time the footage features a short example of the combat system. The combat is based on a mix of real-time action with turn based strategy. 

Enough talk, enjoy:

<center><blockquote class="twitter-tweet"><p lang="en" dir="ltr"><a href="https://twitter.com/hashtag/XenobladeChronicles?src=hash&amp;ref_src=twsrc%5Etfw">#XenobladeChronicles</a>: Definitive Edition’s combat mixes real-time action with turn-based strategy. Get in range of an enemy to auto-attack and unleash powerful Arts. Your party can fend for themselves, but you can also issue commands to them! <a href="https://t.co/bl7t2nGrta">pic.twitter.com/bl7t2nGrta</a></p>&mdash; Nintendo of Europe (@NintendoEurope) <a href="https://twitter.com/NintendoEurope/status/1259815941627666435?ref_src=twsrc%5Etfw">May 11, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br>

---



