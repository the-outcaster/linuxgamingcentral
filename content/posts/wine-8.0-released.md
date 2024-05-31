+++
title = "Wine 8.0 Released, Brings Improved Performance to Direct3D and Improved Controller Hotplugging Support"
date = 2023-01-24T16:13:13Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/dualsense/ds4_and_ds.webp"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "wine 8.0", "wine 8.0 stable", "direct3d", "direct2d", "wow64", "pe"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.0 has now been declared as stable. In it were five release candidates which "represents a year of development effort" and over 8,600 changes. The main achievement of this release, as brought out in the patch notes, "is the completion of the **conversion to PE** format." The PE conversion itself took four years worth of work! But it's important to have as this, as this is a "milestone on the road to supporting various features" such as copy protection and x86 application support on ARM.

There's also **"WoW64 thunks."** Eventually this will make it "fully possible to run 32-bit Windows applications without any 32-bit Unix library."

In the **gaming** department we've got a couple of nice features:
- "greatly improved" controller hotplugging support
- "better implemented" driving wheel detection and reporting, with improved force feedback
- redesigned joystick control panel with new graphics and dedicated view for XInput pads
- DualShock/DualSense hidraw support
- new programming interface for gamepads/driving wheels
- "major performance improvements" for Direct3D due to "optimizations related to streaming map acceleration"
- recognition for more graphics cards

Some other changes:
- light theme enabled by default "for a more modern look"
- print processor architecture implemented "to avoid direct PE<->Unix calls in the printer driver"
- "effects" support for Direct2D, including "description parsing and a number of core objects"
- support for Vulkan driver 1.3.237
- multiple viewport and scissor rectangle support for the Vulkan renderer
- Vulkan renderer limits max D3D feature level based on available Vulkan features
- MPEG-1 layers 1-3 implemented on top of GStreamer
- ASF reader filter support
- "content type resolution" improved in media foundation player
- better support for the enhanced video renderer, with DirectShow filter support
- reduced disk space and address space usage with the implementation of the ApiSetSchema database
- Mono updated to [7.4.0](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.0)
- updates to various bundled libraries, including Faudio, Zlib, and more
- RSA encryption/signing

See the rest of the patch notes on [WineHQ](https://www.winehq.org/announce/8.0). Congrats to the Wine team, CodeWeavers, Valve, and whoever else contributed to this huge release!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
