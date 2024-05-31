+++
title = "Wine 8.0 RC2 Fixes 50 Bugs, Including Unreal Tournament 99, Warframe, Resident Evil 7, and More"
date = 2022-12-22T09:16:48-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.0-rc2.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "resident evil 7", "unreal tournament 99", "warframe", "silent hill 2", "chicken tournament", "serious sam 2", "kholat", "world of warcraft", "kane & lynch", "elder scrolls online"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.0 has reached the release candidate stages. [RC1](https://www.winehq.org/announce/8.0-rc1) upgraded VKD3D to 1.6, provided an improved joystick control panel, and fixed 52 bugs. Now RC2 has arrived, and with it are 50 bug fixes. Note that from here on out Wine 8.0 is in a feature freeze; only bugs will get fixed from here on out.

There's quite a few gaming-related fixes in RC2:
- there should no longer be a crash when bringing up the Steam overlay with a PE build of VKD3D with D3D12 support
- gamepad buttons should now work properly and no longer be delayed
- *Unreal Tournament 99* mouse clicks in main menu should now continue to work after first click
- *Warframe* should no longer crash when loading before menu with WineD3D
- *Kholat* (GOG version) should now run
- *Silent Hill 2* should no longer get the `-installshield` extraction error while installing
- performance degradation fixes for *World of Warcraft* and *Kane & Lynch: Dead Men* demo
- construction set extender mod for *ESO* should no longer crash
- *Resident Evil 7* should now properly render in DX11 mode
- *Chicken Tournament* should no longer crash on start
- *Serious Sam 2* should no longer crash with OpenGL renderer

Some other fixes have made it in as well; see the full patch notes on [WineHQ](https://www.winehq.org/announce/8.0-rc2).

*Cover image credit: Capcom*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
