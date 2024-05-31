+++
title = "Steam Deck Client Update Allows You to See Shader Cache Size, Adds Low Latency Option for Streaming"
date = 2023-10-26T06:01:38Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/stable/10-25-2023/shader_cache_size.jpg"
tags = ["news", "software update", "steam deck", "steam deck client update", "stable"]
keywords = ["steam deck client update", "steam deck", "powera nintendo switch nano", "google stadia controller", "steam input gyro"]
description = "Plus support for the PowerA Switch Nano gamepad."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
It's been nearly six weeks since the last stable Steam Deck client update. A fresh update arrived for all users a few hours ago. Let's go over the changes, fixes, and features. (Note: these screenshots were taken from the "Preview" branch and as such may look slightly different if you're on the "Stable" branch.)

First, **users can now see how much shader cache each installed game takes up** from the Storage tab in Settings:

![Shader cache size in Storage tab](/images/steam_deck/client_updates/stable/10-25-2023/shader_cache_size.jpg)

A new option has been added for Remote Play -- **"Low Latency Networking".** Toggling this on, as the name implies, will reduce latency while streaming, at the expense of bandwidth. Keep in mind you will need to toggle "Enable Advanced Client Options" in the Remote Play tab in order to see this option.

![Low latency networking option in Remote Play](/images/steam_deck/client_updates/stable/10-25-2023/low_latency_networking.jpg)

Steam Input got a *ton* of features and fixes with this update, particularly in the gyro department. Controllers can now be renamed again:

![Rename controller option restored](/images/steam_deck/client_updates/stable/10-25-2023/renaming_controller.jpg)

A new experimental gyro mode has been added -- **"Gyro to Mouse".** This is a renovation of the gyro "As Mouse" mode. More details about this are available in the official patch notes.

![Gyro to Mouse gyro options](/images/steam_deck/client_updates/stable/10-25-2023/3dof_to_2d.jpg)

Along with this comes another experimental gyro mode -- **"Gyro to Joystick (Camera)".** This re-uses concepts from the gyro to mouse system, but outputs to joystick instead of mouse. This will eventually replace Gyro -> "As Joystick".

There's yet another gyro mode -- **"Gyro to Joystick (Deflection)".** "This is most appropriate for simulating steering and flight yokes" and will eventually replace Gyro "Joystick". Both this mode and the "Gyro to Joystick (Camera)" get a "Joystick Power Curve" slider to "counteract the response curve that many games employ for better precision."

![Joystick power curve slider](/images/steam_deck/client_updates/stable/10-25-2023/joystick_power_curve.jpg)

A **"World Space" experimental gyro conversion mode** has been added, which "feels similar to using a laser pointer."

The Steam Input UI gets 'minor tidying,' support for the PowerA Switch Nano Wired controller has been added, and the Stadia controller can now have the capture button binded.

Finally, there are plenty -- and I mean *plenty* -- of fixes for Remote Play, Steam Input, Desktop Mode, and Steam Community. The word "fix" shows up 40 times in the patch notes, ranging from DLC art displaying in the wrong language, the Discovery Queue background color, audio crackling while streaming, the Razer Wolverine V2 Pro DualSense gyro, the "Player Space" gyro conversion mode, DS4 autocalibration, resize grip showing sometimes when windows are maximized, and the friend profile message button.

See the full patch notes on [Steam](https://store.steampowered.com/news/app/1675200/view/3714966246894291121).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
