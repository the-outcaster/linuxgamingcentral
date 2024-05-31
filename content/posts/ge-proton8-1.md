+++
title = "GE-Proton8-1 Rebases to Proton 8 Experimental, Fixes Overwatch from Losing Focus"
date = 2023-05-01T04:30:03Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/weekly_news/oct_1-7.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "ge-proton8-1", "overwatch", "daedalic entertainment", "megadimension neptunia vii"]
description = "But be aware FSR is currently disabled."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton8-1 has been released, and as one could probably tell from the versioning number, it has now been rebased to [Proton 8](https://linuxgamingcentral.com/posts/proton-8.0-1/) -- experimental.

The following tools have also been updated or rebased to the "latest experimental" or "latest git":
- Proton-Wine
- Wine-Staging
- Proton-GE game patches/pending Wine upstream patches
- DXVK
- VKD3D-Proton

Fixes have been added to the following titles:
- Daedalic Entertainment games -- cutscene audio
- *Megadimension Neptunia VII*
- *Overwatch* should no longer lose focus after death

A couple of notes to be aware of:
1. **FSR is currently disabled** as "it needs a massive rebase."
2. It is recommended to remove the NVAPI hack for Lutris Battle.NET installations as it can cause the launcher to crash otherwise.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton8-1).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
