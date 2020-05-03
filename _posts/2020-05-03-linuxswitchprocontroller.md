---
layout: post
title: How to connect a Switch Pro Controller to Linux
categories: [blog]
tags: [blog, linux, gaming]
---

_Troubleshooting when your controller is not recognized in Ubuntu & Steam_



Something that I came around today is that my Nintendo Switch Pro controller was not recognized in Steam. Both Steam BigPicture and Steam itself were not able to detect it. 

I am currently using Ubuntu 19.10 with the 5.3.0-51-generic kernel, which should be able to detect this kind of controller. I was able to connect via BT but the controller was still no recognized in Steam. 

The solution come from a [reddit post](https://www.reddit.com/r/linux_gaming/comments/airri2/switch_wired_pro_controller_on_steam_arch_linux/) with the same issue but on ArchLinux.

Here is the solution:

- Check that Steam has controller rules, they should be located there:
`/lib/udev/rules.d/99-steam-controller-perm.rules`

- If not, you have to install the following package:

  `$ sudo apt install steam-devices`

- Then, use lsubs to find this values: _bus_ and _device_ for the controller, mine is the second line:

  `$ lsusb`

  `$ Bus 001 Device 015: ID 057e:2009 Nintendo Co., Ltd Pro Controller`

- Find the _idVendor_ and _idProduct_ using this command where xxx is the bud and yyy the device, so for me it should be 001 and 015:

  `$ udevadm info -a -p $(udevadm info -q path -n /dev/bus/usb/xxx/yyy)`

- You then edit the controller rules in /lib/udev/ and add this line:

  `# NS PRO Controller USB`

  `KERNEL=="hidraw*", ATTRS{idVendor}=="0e6f", ATTRS{idProduct}=="0181", MODE="0666", TAG+="uaccess"`

- Now the last thing to do is to reload the rules:

  `$ sudo udevadm control --reload-rules`


Now in Steam BigPicture you just have to activate the support for the Pro Controller and the home button should then light in blue. A interesting feature that I don't know why Nintendo has not implemented when the controller is connected to the Switch?


