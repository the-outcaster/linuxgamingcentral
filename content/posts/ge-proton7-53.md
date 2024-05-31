+++
title = "GE-Proton7-53 Adds EAC Fix for Star Citizen, Diablo IV Fix"
date = 2023-03-24T13:30:06Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-53.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "halo infinite", "diablo iv", "outlaws + a handful of missions", "underdog detective", "star citizen"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton7-52 released yesterday. Aside from DXVK, VKD3D-Proton, and Wine getting updated, two Protonfixes were added for [*Outlaws + A Handful of Missions*](https://store.steampowered.com/app/559620/Outlaws__A_Handful_of_Missions/) and [*Underdog Detective*](https://store.steampowered.com/app/1681970/_Underdog_Detective/). The "proper fix from Proton upstream" for *Diablo IV* has been added, and the *Halo Infinite* patches have been updated once again.

A new release followed shortly thereafter with an EAC fix for *Star Citizen*. This "allows *Star Citizen* to run without needing to change the `/etc/hosts` file and does not interfere with EAC for other games." Note that you will need to do the following prior to running the game:
1. Set the `SteamGameId=starcitizen` environment variable.
2. Run a script that's provided in the patch notes to remove existing EAC files.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-53).

*Cover image credit: Cloud Imperium Games*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
