+++
title = "GE-Proton7-36 Adds Protonfix for Halo Reach Mod Tools, Temporarily Disables FSR"
date = 2022-10-02T23:46:27-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-36.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["ge-proton", "proton", "halo reach", "fsr", "Ougon Musoukyoku", "shatterline", "dxvk", "vkd3d-proton", "wine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton7-36 has imported the [NVAPI enablements](https://linuxgamingcentral.com/posts/proton-experimental-9-20-2022/) and media-converter changes from upstream Proton. In addition to updating DXVK, VKD3D-Proton, and Wine-Bleeding Edge, Protonfixes have been added to the following:
- *Shatterline*
- *Halo Reach* mod tools
- *Ougon Musoukyoku*

But one feature in this update has been removed, at least for now: FSR. The reasoning, according to the patch notes, is as follows:
> The [commit](https://github.com/ValveSoftware/wine/commit/7c5306e3b834a29b66c6d4dc6a1bb901a9ec82c9) is important because it fixes some problems that were happening with winevulkan, but unfortunately it also patches in a lot of components that were already part of the FSR patch. The problem is that the commit has much of the same contents as the FSR patch, but the FSR patch has the FSR bits all mixed in and it's not within my know-how to rebase.

And unfortunately "the FSR patches have been increasingly problematic to maintain over time due to the lack of the original author willing to rebase the Wine version in favor of using the GameScope version." So from now on, we'll have to rely on GameScope to make use of FSR. Either that or hope that the game you're playing has a built-in FSR feature.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-36). Easily install GE-Proton7-36 on your system/Steam Deck with my [guide](https://linuxgamingcentral.com/posts/proton_ge_tutorial/).

*Cover image credit: Shinjin-sama from DeviantArt*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
