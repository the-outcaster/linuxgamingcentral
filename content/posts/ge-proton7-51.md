+++
title = "GE-Proton7-51 Adds Fix for Halo Infinite and Anno 1800 Multiplayer"
date = 2023-03-16T02:14:18Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/codeweavers/halo.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "halo infinite", "anno 1800 multiplayer", "tokyo recro", "resident evil 0", "star wars jedi fallen order", "pentiment"]
description = "Plus a Protonfix for Tokyo Necro."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*Halo Infinite* has been playable way back to GE-Proton7-22 in [June](https://linuxgamingcentral.com/posts/halo-infinite-now-runs-with-ge-proton/). Evidently there must have been a regression -- the game now uses "even more esoteric D3D12 features" according to [HansKristian](https://github.com/HansKristian-Work/vkd3d-proton/pull/1465), who works on VKD3D-Proton. A patch has been submitted, and while it hasn't been merged with VKD3D-Proton yet, GE-Proton7-51 has already added it. So, I guess you can keep playing *Halo Infinite* now.

A [fix](https://github.com/ValveSoftware/wine/pull/181) was also added for *Anno 1800*'s multiplayer mode. A Protonfix for *Tokyo Necro* was added.

A few Protonfixes have been removed: *Resident Evil 0*, *Star Wars Jedi: Fallen Order*, and *Pentiment*.

Wine, DXVK, and VKD3D-Proton have all been updated to "git" or "bleeding-edge." Finally, a typo for *The Witcher 2*'s Protonfix was fixed.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-51).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
