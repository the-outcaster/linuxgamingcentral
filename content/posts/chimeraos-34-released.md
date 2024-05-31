+++
title = "ChimeraOS 34 Released, Improves Handheld Gamepad Support and Adds Plenty of Bug Fixes"
date = 2022-08-09T10:55:56-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos_32/cover.svg"
tags = ["news", "software update", "distro update", "chimeraos"]
keywords = ["chimeraos", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[ChimeraOS](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/) -- one of my favorite gaming-oriented distributions -- just got a big update today. Proton has been re-enabled for Windows-based games (for some reason it wasn't before), several bug fixes have been addressed for the Steam Deck UI, Proton, and Bluetooth, a UI has been added for formatting external hard drives, "ChimeraOS Verified and Playable" games have been added to the Deck UI, and plenty of other improvements! In addition, the typical set of software packages have been updated:
- kernel [5.18](https://linuxgamingcentral.com/posts/news-kernel-5.18/).14
- Mesa [22.1.4](https://docs.mesa3d.org/relnotes/22.1.4.html)
- NVIDIA driver [515.57](https://www.nvidia.com/download/driverResults.aspx/190432/en-us/)
- Chimera [0.14.11](https://github.com/ChimeraOS/chimera/releases/tag/0.14.11) (a web interface for adding ROMs or Flatpaks to your system)
- SteamOS Compositor Plus [1.10.1](https://github.com/ChimeraOS/steamos-compositor-plus/releases/tag/1.10.1)
- RetroArch [1.10.3](https://retroarchofficial.itch.io/retroarch/devlog/370428/retroarch-1103-release)

Since the Big Picture Mode session is now using the Deck client, this should mean that switching between interfaces will be smoother and not require Steam client updates. Steam Input is now activated globally.

I have personally tested this distro on the Deck and can confirm I can get into the Steam Deck UI by opening up a terminal with CTRL + ALT + F3 and running `chimera-session gamepadui`. The framerate limiter works, but lowering the refresh rate causes the screen to tear. Unfortunately audio won't work on the Deck until this [patch](https://git.kernel.org/pub/scm/linux/kernel/git/next/linux-next.git/commit/?id=b340128432a2b8849cc34f9653d7c43c83102bbd) gets merged into the kernel, which we should hopefully see in 5.20/6.0. For the time being though you can use Bluetooth audio.

![chimeraos on Deck](/images/steam_deck/photos/chimeraos/34.jpg)

For more info, see the patch notes on [Steam](https://steamcommunity.com/groups/chimeraos/announcements/detail/3377155691541233300).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
