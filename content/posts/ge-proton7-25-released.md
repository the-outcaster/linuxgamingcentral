+++
title = "GE-Proton7-25 Released, Updates Wine to Bleeding-Edge and Adds FSR Auto-Calculation"
date = 2022-07-18T08:34:35-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/trove/trove_logo.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["ge-proton", "proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Today's update to GE-Proton adds some fixes to *Final Fantasy XIV* (seems like that game *always* needs some kind of patching). Specifically the intro video after the datacenter select should be fixed (apparently this isn't the first time this has happened). The patch notes mention that this may also fix WMV playback in a few other titles. *Trove* and *Rift* have been fixed as well.

Wine has been updated to bleeding-edge, which "brings in numerous fixes," DXVK has been updated to [1.10.2](https://linuxgamingcentral.com/posts/dxvk-1.10.2-released/), vkd3d-proton has been updated to git, a `MODS=1` option has been added for *Skyrim*, and "FSR will now auto-calculate resolutions based on screen aspect ratio rather than adding pre-defined entries based on width."

As a reminder, enabling FSR on a Steam game requires this launch parameter:

`WINE_FULLSCREEN_FSR=1 WINE_FULLSCREEN_FSR_MODE=ultra %command%`

You can replace "ultra" with "quality", "balanced", or "performance", depending on how much you want the graphics to scale, with ultra using the least scaling (1.3x), to performance using the most (2x). Check the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-25) for more info, and be sure to support GloriousEggroll via [Patreon](https://www.patreon.com/gloriouseggroll) if you like his work!

*Cover image credit: wccftech.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
