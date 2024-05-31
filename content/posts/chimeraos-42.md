+++
title = "ChimeraOS 42 Adds Support for Aya Neo 2, OpenGamepadUI"
date = 2023-05-11T14:41:30Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos/logo.jpg"
tags = ["news", "software update", "distro update", "chimeraos"]
keywords = ["chimeraos", "chimeraos 42", "aya neo 2"]
description = "Plus GPD Win 4 controller support and several bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The fantastic console-oriented distro ChimeraOS has been updated to version 42. The developers have worked very hard on this release, ensuring any last-minute crashes were fixed. This update removes old BPM, upgrades GNOME to version 44, adds experimental support for [OpenGamepadUI](https://linuxgamingcentral.com/posts/open-gamepadui/), better support for Aya Neo devices (the Aya Neo 2 in particular), a way to manage multi-GPU systems via the CLI, Chimera app improvements, and more than half-a-dozen bug fixes.

Software updates are as follows:
- kernel: [6.1.27](https://lwn.net/Articles/930597/)
- Mesa: [23.0.2](https://docs.mesa3d.org/relnotes/23.0.2.html)
- NVIDIA driver: [530.41.03](https://www.nvidia.com/download/driverResults.aspx/200481/en-us/)
- GNOME: [44](https://release.gnome.org/44/)

Features:
- two experimental sessions for [OpenGamepadUI](https://linuxgamingcentral.com/posts/open-gamepadui/)
- LEDs on various Aya Neo devices can now be controlled via the [AYALED service](https://github.com/ChimeraOS/chimeraos/wiki/Device-Specific-Configurations)
- exposed fan control support for Aya Neo 2/Geek
- pikaur AUR helper added "for simpler troubleshooting and development usage"
- CLI utility to manage multi-GPU systems has been [added](https://github.com/ChimeraOS/chimeraos/wiki/General-Configuration#multi-gpu-management-utility-egpu-and-igpu--dedicated-gpu-configurations)

Improvements:
- "usability and aesthetics" of the disk management utility in the Chimera app
- controller support for GPD Win 4
- Chimera app can be launched with the LC button on the Aya Neo 2
- Chimera app: built-in TDP controls for Aya Neo 2
- Chimera app can be launched from the desktop
- Chimera app shows app and game titles from Flathub, GOG, and EGS "for easy searchability"

Fixes:
- secondary drives are automatically mounted
- boot splash screen
- bootloader generator "that failed to pickup additional kernel options"
- devices suspending immediately after waking
- duplicate key presses on Aya Neo 2/Aya Neo Geek
- button mapping in RetroArch emulators "for devices managed by HandyGCCS"
- MangoHUD displaying in the center of the screen for "left-rotated" displays
- MangoHUD not displaying the overlay correctly "with systems with multiple CPU cores/threads"

Other:
- old BPM has been removed, as well as steamos-compositor-plus
- updated "device quirks script" for [AOKZOE A1](https://github.com/ChimeraOS/chimeraos/wiki/Device-Specific-Configurations#aokzoe-a1)
- brightness control switched to polkit

Please be aware that **if your system is using legacy/BIOS boot or a MPR partition type, you will need to re-install your system.** Upgrading ChimeraOS from an older version should still be possible, but upgrading as soon as possible is recommended "to avoid getting into an unbootable state."

See the [patch notes](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-42-2023-05-11) for more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
