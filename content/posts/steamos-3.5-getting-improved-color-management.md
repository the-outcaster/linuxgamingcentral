+++
title = "Steam Deck to Get Improved Color Management with SteamOS 3.5"
date = 2023-04-24T16:15:48Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/photos/melee/steam.jpg"
tags = ["news", "steam deck", "steamos"]
keywords = ["steamos 3.5", "amd color management", "steam deck color management"]
description = "\"We are planning on shipping our color management support with gamut mapping, HDR, SDR on HDR, HDR on SDR, and much more in Steam OS 3.5.\""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
SteamOS 3.5 is becoming more and more of an exciting update to look forward to. Not only will we be getting [a setting to disable SMT](https://linuxgamingcentral.com/posts/updated-kernel-and-smt-disabled-with-steamos-3.5/), but we'll also be seeing an update to the kernel, and potentially an upgrade to the Mesa drivers, which will lead to [smaller shader cache by up to 60%](https://linuxgamingcentral.com/posts/steam-deck-getting-smaller-shader-cache/).

And now, there's yet *another* feature coming. Kernel mode-setting color pipeline enhancements will be available. This is brought to you by Melissa Wen, Joshua Ashton, and Harry Wentland. You can read the [patch series](https://lists.freedesktop.org/archives/amd-gfx/2023-April/092215.html) for more details, but basically:
- two patches "fix quantization issues on sharper LUT programming"
- a third "adds a config option to restrict AMD color feature usage"
- 13 of the patches "implement AMD driver-private color properties"
- the final 24 "rework the AMD display manager and color management to support the properties exposed"

![Deck display pipeline](/images/steam_deck/display_pipeline.webp)
*Image credit: [Joshua Ashton](https://github.com/ValveSoftware/gamescope/blob/master/src/docs/Steam%20Deck%20Display%20Pipeline.png)*

> We identified during [our work](https://gitlab.freedesktop.org/mwen/linux-amd/-/commits/amd-color-mgmt) that AMD provides many other valuable capabilities that we don't find in other vendors, so we started to work on AMD driver-private color properties that better describe its color pipeline, enabling us to expose full AMD color capabilities on Deck HW.

So, essentially, you're going to have better colors on your Deck's screen. I am aware that some of you have complained about the color quality, and I would imagine this update will alleviate some of your concerns.

> We are planning on shipping our color management support with gamut mapping, HDR, SDR on HDR, HDR on SDR, and much more in Steam OS 3.5.

Nice.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
