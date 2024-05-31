+++
title = "PCSX2 (PS2 Emulator) Gets New UI + Support for DS4/DualSense Controllers"
date = 2022-05-23T11:51:29-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/pcsx2/cover.jpeg"
tags = ["emulation", "news"]
keywords = ["pcsx2", "ps2", "playstation 2"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The PlayStation 2 emulator [PCSX2](https://pcsx2.net/) gets a much-needed UI overhaul. The `wxWidgets` library that the developers were using before has now been replaced with `Qt`. Now it looks much cleaner. If you've used the Dolphin emulator, you'll notice the interface looks quite familiar:

![pcsx2 new ui](/images/pcsx2/ui.png)
*Image credit: @Dreamboum*

The controller setting interface has also been updated with this new UI library. Settings can now be set on a per-game basis, there's an auto-updater, and there's "native" support for the DualShock 4 and DualSense gamepads.

You can try these new features out by downloading the latest [nightly build](https://pcsx2.net/downloads/#nightly-anchor) and running the emulator through Wine. Unfortunately the Linux and Mac versions are still using the `wxWidgets` UI, and I don't know when or even if these versions will get the `Qt` makeover.

*Cover image credit: @Dreamboum*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
