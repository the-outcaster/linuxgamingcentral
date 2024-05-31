+++
title = "ChimeraOS 32 Released, Adds Software Upgrades + Various Improvements"
date = 2022-04-13T10:50:37-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos_32/cover.svg"
tags = ["chimeraos update", "software release"]
keywords = ["chimeraos", "gameros"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Last night [ChimeraOS](https://chimeraos.org) -- the distro that turns your PC into a gaming console, similar to SteamOS 3.0 -- version 32 was released. The kernel was upgraded to [5.17](https://www.omgubuntu.co.uk/2022/03/linux-5-17-released-new-features).1, the Mesa drivers were upgraded to [22.0.1](https://www.phoronix.com/scan.php?page=news_item&px=Mesa-22.0.1-Released), the NVIDIA driver was upgraded to [510.54](https://www.gamingonlinux.com/2022/02/nvidia-fix-up-a-vulkan-problem-with-the-v51054-driver-release/), and a few other components also received an upgrade, including [`steamos-compositor-plus`](https://github.com/ChimeraOS/steamos-compositor-plus) and [RetroArch](https://www.retroarch.com/).

In addition to software upgrades, some other changes have been made. The GOG launcher script, for instance, has been improved to allow better compatibility, and the Deck UI has a fix for missing artwork, including from games outside of Steam, such as Epic, Flathub, etc. Aya Neo users should benefit from this updated version, as it fixes several issues the portable device had, including the touch screen, suspend, and reboot.

Note that Steam Play for all titles has been disabled by default now, due to [non-Steam games failing to launch](https://github.com/ValveSoftware/steam-for-linux/issues/8503). Also be aware the Deck UI only works on AMD GPUs.

Check the full patch notes from the [Steam Community](https://steamcommunity.com/groups/chimeraos/announcements/detail/3184616660099623546).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
