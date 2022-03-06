---
layout: post
title: 🎛️ Easily share your WiFi with a QRcode
subtitle: Nothing new but it's still useful
illustration: /images/whitehorn.png
categories: [blog]
tags: [linux,qrcode]
comments: false
youtubeId:
---

### 🎛️ Easily share your WiFi with a QRcode

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/L3L17MUSO)

---

Hey there! A short artcile because this weekend I had to setup a new WiFi network at home and I didn't want to have to speel the long password everytime a familly memeber wanted to connect there phone to the new network. So looking for a quick solution, I had the idea to print a QRcode and put on the router's cabinet door.

This is really simple and you can even customize it a bit to make it looks good.

You can use qrencode to do so, grab your favourite package manager and: 

```bash
#if you are using arch
yay -S qrencode

#if you are using debian
sudo apt get install qrencode 
```

Next, here is a small script that will ask you to input your SSID, your WPA password and a filename for the qrcode saved as a png file: 

```sh
#!/bin/bash

read -p "$(tput setaf 3)$(tput bold)SSID name: $(tput sgr0)" ssid
read -p "$(tput setaf 3)$(tput bold)WPA password: $(tput sgr0)" pswd
read -p "$(tput setaf 3)$(tput bold)file name: $(tput sgr0)" fname

qrencode -s 10 -m 3 -l H -d 200 -o $fname.png "WIFI:S:$ssid;T:WPA;P:$pswd;;"    
display qr-wifi.png
```

Let's have a look at the options we have here: 
- -s specifies the size of dot (pixels)
- -m specifies the margins
- -l specifies the error correction, we set it to Highest because we are going to modify the QRcode later with gimp
- -d specifies the DPI of the generated PNG
- -o specifies the output file

You can create any QRcode you like linking to a website, a youtube video, a file shared on the cloud, just be creative. And with the error correction set to Highest, you can modify the QRcode in GIMP and make something a little bit more colorful. For exemple: 

[![qrcode](/images/whitehorn.png)](/images/whitehorn.png)

Have fun with it!