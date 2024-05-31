+++
title = "GE-Proton8-4 Fixes Four Games, Removes EAC Workaround for Fall Guys"
date = 2023-06-05T20:48:45Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fall_guys/cover.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "ge-proton8-4", "moero chronicle", "shadows on the vatican", "the blind prophet", "alter ego", "fall guys", "northstar launcher"]
description = "Be sure to cancel the second step when installing Fall Guys."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Protonfixes have been added to the following titles:
- *Moero Chronicle*
- *Shadows on the Vatican* series
- *The Blind Prophet*
- *Alter Ego*

The `easyanticheat_x64.so` workaround for *Fall Guys* has been removed. A fix was added for the Northstar launch argument not working.

The following "upstream" tools have been added:
- Proton script changes
- font changes
- OpenXR changes
- Steam helper fixes
- user_settings changes

The following tools have been updated to "latest bleeding edge" or "git":
- Wine
- DXVK
- VKD3D-Proton
- DXVK-NVAPI

Note that, when the EOS installer is running on a clean prefix with *Fall Guys*, "Cancel" needs to be clicked on the second step, "otherwise *Fall Guys* will tell you the game is missing files and force you to exit."

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton8-4).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
