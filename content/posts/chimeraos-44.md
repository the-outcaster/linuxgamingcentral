+++
title = "ChimeraOS 44 Nerfs NVIDIA Support, Adds Swap File For Improved Performance"
date = 2023-09-28T15:34:06Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/distro_reviews/chimeraos/cover.jpg"
tags = ["news", "software update", "distro update", "chimeraos"]
keywords = ["chimeraos", "chimeraos 44", "chimeraos loses nvidia support", "asus rog ally", "nvk"]
description = "Plus: DSDT audio override no longer needed for the ROG Ally."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
ChimeraOS 44 released just a few days ago. While there's nothing too exciting going on with this release, the "groundwork" they "have laid out in the previous releases has been bearing fruit so you can expect more consistent releases in the future."

Software components have been upgraded as follows:
- Kernel: [6.5.3](https://9to5linux.com/linux-kernel-6-5-officially-released-this-is-whats-new)
- [OpenGamepadUI](https://linuxgamingcentral.com/posts/open-gamepadui/): 0.21.7. This update allows performance profiles, improved gamepad support for the ROG Ally and GPD Win 4, Power Tools support for the AMD 7000 series, and more
- Mesa: [23.1.7](https://docs.mesa3d.org/relnotes/23.1.7.html)

There are several fixes and improvements, ranging from DSDT override no longer needed for ROG Ally audio support, improved compatibility with handhelds that have AT keyboards, **a 1 GB swap file now set in place "to boost a lot of games,"** fixed headphone output on Aya Neo devices, save files for PSP games now fixed, an option in the Chimera app to initialize an existing partition as a Steam library, and *tons* of other additions.

One nice advantage to this update is **users will no longer have to manually adjust the resolution on a per-game basis.** This is because Gamescope-plus creates a native display resolution xWayland session. That was one of the complaints that I had with my [review of the distro](https://linuxgamingcentral.com/posts/chimeraos-review/) a while back, and I'm glad to see it has been addressed. HandyGCCS also gets some QoL improvements, including "greatly improved" latency, suspend looping getting fixed, and full controller support for a few more handhelds.

Since the Steam client works differently now in terms of checking for OS updates, if you're using ChimeraOS 43 or earlier, **you'll need to upgrade the OS by checking for Steam client updates.** The Chimera web-ui port has been changed from 80 to 8844.

One major change with this update is **NVIDIA is no longer supported**:
> In the last few releases we have discovered multiple examples with Nvidia drivers causing major issues on systems without Nvidia components. After attempting multiple avenues to resolve these issues unsuccessfully, the poor state of Wayland and Gamescope support for Nvidia in general, and with Nvidia [having more driver issues coming soon](https://www.phoronix.com/news/Linux-6.6-Illicit-NVIDIA-Change), we have opted to remove Nvidia support entirely at this time to provide a better experience for users that have hardware with full support.

The patch notes do mention that once [NVK](https://linuxgamingcentral.com/tags/nvk) becomes more mature, they will "revisit Nvidia support." In the meantime, NVIDIA users are recommended to stick with version 42.

See the full patch notes on [GitHub](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-44-2023-09-25).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
