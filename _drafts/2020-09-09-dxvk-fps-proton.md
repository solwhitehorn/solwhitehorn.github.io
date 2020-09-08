---
layout: post
title: 📝 A great solution for displaying your FPS in Linux (Steam & Lutris)
subtitle: MangoHud all day, everyday
illustration:https://github.com/flightlessmango/MangoHud/blob/master/assets/overlay_example.gif
categories: [blog]
tags: [tuto, linux, proton]
comments: true
---

# MangoHud is the best way to monitor FPS on Linux

Throw back to an article I wrote back in May about how to display your FPS with Proton on Steam. Since then I discovered an even better tool called MangoHud.

MangoHud is a Vulcan and OpenGL overlay used for monitoring FPS, temperatures, CPU/GPU load, VRAM, RAM and more.

Its installation is easy and I point you to the GitHub page for more information on that. 
Using it is also really easy:

- to enable the HUD for Vulkan and OpenGL run: `mangohud /path/to/app`
- For Lutris, got to the system options and add this command prefix: `mangohud`
- for Steam you can add this launch option: `mangohud %command%`

The command options that you can use with steam are numerous:

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