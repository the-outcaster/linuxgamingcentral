+++
title = "GE-Proton7-55 Fixes EAC Compatibility, Updates Tools to Latest Bleeding Edge"
date = 2023-04-10T19:38:28Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-55.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge"]
description = "A patch is needed for Lutris users."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The hotfix for *Star Citizen* in [GE-Proton7-53](https://linuxgamingcentral.com/posts/ge-proton7-53/) evidently "broke EAC compatibility for other games," so today's update to GE-Proton fixes this.

In addition, the usual set of tools have been updated to git or latest bleeding-edge, including Wine, DXVK, and VKD3D-Proton. NVAPI is enabled for *Stranger of Paradise: Final Fantasy Origin*, and the legacy xactengine Winetricks Protonfix was removed.

The patch notes also mention that if you're using Lutris 0.5.13-beta1, you'll need to use a [patch](https://github.com/lutris/lutris/commit/6d78eeb9fb18680905572d2e35f2d4666106119c) to prevent SteamGameId from being overridden.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-55).

*Cover image credit: Square Enix*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
