---
layout: post
title: 📝 How to connect a Switch Pro Controller to Linux
subtitle: Quick configuration for Ubuntu/Arch
illustration: https://cdn.vox-cdn.com/thumbor/YFJJoAdBa9n2YA8za8GoBFgCMj8=/0x0:2040x1360/1200x800/filters:focal(857x517:1183x843)/cdn.vox-cdn.com/uploads/chorus_image/image/53373313/jbareham_170221_1475_0010.0.0.jpg
categories: [blog]
tags: [tuto, linux, gaming, nintendo switch]
comments: true
---

### Troubleshooting when your controller is not recognized in Ubuntu & Steam

Something that happened to me today is that my Nintendo Switch Pro controller was not recognized in Steam. Both Steam Big Picture and Steam itself were not able to detect it. 

I am currently using Ubuntu 19.10 with the 5.3.0-51-generic kernel, which should be able to detect this kind of controller. I was able to connect via BT but the controller was still not recognized in Steam. 

The solution come from a [reddit post](https://www.reddit.com/r/linux_gaming/comments/airri2/switch_wired_pro_controller_on_steam_arch_linux/) with the same issue but on ArchLinux.

Here is the solution:

- Check that Steam has controller rules, they should be located there:

  ```bash
  $ /lib/udev/rules.d/99-steam-controller-perm.rules
  ```

  

- If not, you have to install the following package:

  ```bash
  $ sudo apt install steam-devices
  ```

  

- Then, use lsubs to find this values: _bus_ and _device_ for the controller, mine is the second line:

  ```bash
  $ lsusb
  Bus 001 Device 015: ID 057e:2009 Nintendo Co., Ltd Pro Controller`
  ```

  

- Find the _idVendor_ and _idProduct_ using this command where xxx is the bus and yyy the device, so for me it should be 001 and 015:

  ```bash
  $ udevadm info -a -p $(udevadm info -q path -n /dev/bus/usb/xxx/yyy)
  ```

  We are looking for this two values: ATTR**S**{idVendor} and ATTR**S**{idProduct}



- You then edit the controller rules in /lib/udev/rules.d/99-steam-controller-perm.rules and add these lines (of course, replace the XXXX with your values):

  ```bash
  #NS PRO Controller USB
  KERNEL=="hidraw*", ATTRS{idVendor}=="XXXX", ATTRS{idProduct}=="XXXX", MODE="0666", TAG+="uaccess"
  ```

  

- Now the last thing to do is to reload the rules:

  ```bash
  $ sudo udevadm control --reload-rules
  ```
  
  


Now in Steam Big Picture you just have to activate the support for the Pro Controller and the home button should then light in blue.

![](https://cdn.vox-cdn.com/thumbor/YFJJoAdBa9n2YA8za8GoBFgCMj8=/0x0:2040x1360/1200x800/filters:focal(857x517:1183x843)/cdn.vox-cdn.com/uploads/chorus_image/image/53373313/jbareham_170221_1475_0010.0.0.jpg)
