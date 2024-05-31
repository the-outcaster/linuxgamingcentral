+++
title = "GE-Proton7-48 Updates Proton-Wine to Bleeding Edge, Includes Dead Space Remake Fixes"
date = 2023-01-30T03:28:08Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-48.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "dead space remake on steam deck", "dead space remake on linux"]
description = "Dead Space Remake fixes should be in as well as DXVK 2.1."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Nothing really noteworthy about today's GE-Proton update. The following tools have been updated:
- Proton-Wine
- VKD3D-Proton
- DXVK
- DXVK-NVAPI

Proton-Wine in particular was updated to "bleeding-edge." Everything else was just "updated"; presumably to the latest git.

Now that these tools have been updated, they *should* include the most recent fixes for *Dead Space Remake*. Game should work reasonably well on Deck with these fixes. The update to DXVK should also include the recent [2.1](https://linuxgamingcentral.com/posts/dxvk-2.1-released/) update with HDR support, shader compilation improvements, and sample rate shading.

Regarding *Monster Hunter: Rise*, apparently there's an issue specific to the 7900 XT/XTX GPUs, which is [currently](https://gitlab.freedesktop.org/mesa/mesa/-/issues/8153) [pending](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/20941) for a fix.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-48).

*Cover image credit: Motive/EA*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
