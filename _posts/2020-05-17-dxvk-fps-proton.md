---
layout: post
title: 📝 How to monitor your FPS in Linux (Steam & Lutris)
subtitle: An easy alternative for MSI Afterburner
illustration: https://www.khronos.org/assets/uploads/apis/2020-Vulkan-small-badge.png
categories: [blog]
tags: [tuto, linux, proton]
comments: true
---

# A quick and easy way to display your FPS and more when using Steam Proton on Linux

As you might have seen I've been posting some videos now on my youtube channel. Some are short footages from my Switch (as I don't have a capture device), other are now some footage of my playing game in Linux.

In a past life using Windows I was used to having MSI Afterburner to monitor the performance of my games. You can't run this soft in Linux but there is a easy and quick way to do so.

If you are using Steam's Proton compatibility tool you can put this in the launch options:

`DXVK_HUD=1 %command%`

This will overlay the name of your GPU, versions of the drivers you are using and a FPS counter.

Multiple options are available to you if you want more information, just separate them with commas in your launch command:

- `devinfo`: Displays the name of the GPU and the driver version.
- `fps`: Shows the current frame rate.
- `frametimes`: Shows a frame time graph.
- `submissions`: Shows the number of command buffers submitted per frame.
- `drawcalls`: Shows the number of draw calls and render passes per frame.
- `pipelines`: Shows the total number of graphics and compute pipelines.
- `memory`: Shows the amount of device memory allocated and used.
- `gpuload`: Shows estimated GPU load. May be inaccurate.
- `version`: Shows DXVK version.
- `api`: Shows the D3D feature level used by the application.
- `compiler`: Shows shader compiler activity.
- `samplers`: Shows the current number of sampler pairs used [D3D9 Only].
- **`full`**: enables all the available HUD elements

The `DXVK_HUD=1 %command%` is equivalent here to `DXVK_HUD=deving,fps %command%`. Using Lutris, you can type the same options but this time you have to put that in the environment variable.

As always, it you want to now more, the best source is the github page of the project: [https://github.com/doitsujin/dxvk](https://github.com/doitsujin/dxvk)

If you want to see this in action, have a look at this video I made with the Witcher 3 running in Steam Proton on max settings:

<br>

<center><iframe class="iframev" width="560" height="315" src="https://www.youtube.com/embed/Yyt0AN_9TRE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

 <br>