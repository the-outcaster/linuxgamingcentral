+++
title = "ChimeraOS 39 Switches to New BPM By Default, Adds New Boot Splash Animation"
date = 2023-02-18T03:18:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos/logo.jpg"
tags = ["news", "software update", "distro update", "chimeraos"]
keywords = ["chimeraos", "chimeraos 39", "new bpm", "nintendo ds", "handygccs", "hogwarts legacy"]
description = "Plus, improved Intel GPU support and plenty of other goodies!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Leave it up to my favorite gaming distro, ChimeraOS, to continue with its trend of being more awesome as the months go by.

First thing's up, the distro now **resorts to the new Big Picture Mode as the default interface** (the devs are sad about [old BPM going away](https://linuxgamingcentral.com/posts/rip-old-bpm/)). But this is good timing, as fortunately the [beta desktop Steam client](https://linuxgamingcentral.com/posts/steam-deck-client-beta-update-2-17-2023/) just got updated with improved NVIDIA GPU support. So hopefully NVIDIA users won't have a sluggish experience navigating through the menus. ChimeraOS 39 also comes with a **new splash animation on boot.**

What's nice is, **system updates are fully integrated in the new BPM**. How the ChimeraOS team figured that out is beyond me, but I tip my hat to them. That probably wasn't an easy task.

Other features are as follows:
- Nintendo DS support was added
- the install media has been updated with new system repair/recovery functionality
- improved Intel GPU support
- stability improvements to *Hogwarts Legacy* and "possibly other games"

{{< rawhtml >}} 

<video width=50% controls autoplay loop>
    <source src="/videos/chimeraos/splash.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

*Animation design is brought to you by Mark Tolle*

Package updates:
- kernel: [6.1](https://linuxgamingcentral.com/posts/kernel-6.1-released/).11
- Mesa: [22.3.4](https://docs.mesa3d.org/relnotes/22.3.4.html)
- NVIDIA driver: [525.89.02](https://www.nvidia.com/Download/driverResults.aspx/199656/en-us/) (adds a fix for banding/flickering of color gradients on DisplayPort monitors)

Fixes:
- custom launch options/Steam Input settings should now be properly applied
- improved Flatpak desktop integration
- certain Intel/NVIDIA combos should no longer have a boot failure
- overheating issues on some handhelds (particularly with Ryzen processors) has been resolved by having their "T-junction" temperature set to 95 degrees C automatically

Other changes:
- non-Steam shortcuts that weren't created with the Chimera web app should be preserved
- "improved stuttering" for gyro controls and swapped default button mappings for QAM and Guide buttons on OneXPlayer and AOKZOE devices via [HandyGCCS](https://github.com/ShadowBlip/HandyGCCS) (Handheld Game Console Controller Support for Linux)
- removable media gets checked for compatibility when formatting
- the split_lock_detect kernel parameter is now set to off by default

Pretty exciting release! You should really [give it a try](https://chimeraos.org/download). Patch notes available on [GitHub](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-39-2023-02-17).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
