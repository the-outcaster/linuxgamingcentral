+++
title = "GE-Proton7-39 Adds Overwatch 2 Freeze Fix, Enables GameDrive for Elder Scrolls Online"
date = 2022-11-06T12:39:21-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-39.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["ge-proton", "ge proton", "proton-ge", "proton ge", "glorious eggroll", "proton", "sonic adventure 2", "overwatch 2", "far cry 5", "vkd3d-proton", "proton-wine", "dxvk", "nvapi", "eso", "mono"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton7-39 adds a freeze fix for *Overwatch 2*. Though GE-Proton is not meant to be used for games outside of Steam, this fix should help other games. *Elder Scrolls Online* now has the gamedrive option enabled by default (never heard of gamedrive, to be honest).

Protonfixes have been removed for the following titles/launchers:
- [*Sonic Adventure 2*](https://store.steampowered.com/app/213610/Sonic_Adventure_2/)
- [*Far Cry 5*](https://store.steampowered.com/app/552520/Far_Cry_5/) EAC -- yup, apparently the game has EAC
- Origin

The individual tools that make up GE-Proton have been updated to "latest bleeding edge" or "git":
- [Proton-Wine](https://github.com/GloriousEggroll/proton-wine)
- [DXVK](https://github.com/doitsujin/dxvk)
- [vkd3d-proton](https://github.com/HansKristian-Work/vkd3d-proton) -- this should include the [v2.7](https://linuxgamingcentral.com/posts/vkd3d-proton-2.7-fixes-many-previously-unsolvable-issues/) update which contains GPU performance improvements!
- Mono to [7.4.0](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.0)

Additionally, Proton NVAPI fixes have been "pulled in upstream."

Seems like a pretty exciting release to me! I might do some benchmarking on Deck later tonight and test the performance difference with this release over Proton 7.0-4.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-39). As always, you can refer to my [guide](https://linuxgamingcentral.com/posts/proton_ge_tutorial/) for obtaining the latest version of GE-Proton with just a few clicks.

*Cover image credit: Sega*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
