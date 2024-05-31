+++
title = "Proton Experimental Enables Compatibility with The Witcher 3: Wild Hunt, Improved Steering Wheel Support"
date = 2022-12-21T15:32:27-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton_experimental/12-21-2022.jpg"
tags = ["news", "software update", "proton experimental"]
keywords = ["proton", "proton experimental", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "youropa", "the witcher 3", "mortal kombat x", "dxvk-nvapi", "monster hunter world"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The first day of winter also marks a new update to Proton Experimental. Small one, but a good one.

*The Witcher 3: Wild Hunt* now apparently works -- I'm assuming this is in reference to the recent DX12 upgrade that had been broken for so many people. Support for steering wheels has been improved, but in what way, the patch notes don't mention. You might be able to take a look at the [commit history](https://github.com/ValveSoftware/Proton/commits/experimental-7.0-20221219) to get a hint.

Two fixes have been added for *Mortal Kombat X* and [*Youropa*](https://store.steampowered.com/app/640120/Youropa/). The former had a regression -- it should now run with decent performance. The latter has a "OpenGL launch option" fixed.

Lastly, DXVK-NVAPI has been updated to [0.6](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6) (although I think this was already added in the [previous update](https://linuxgamingcentral.com/posts/proton-experimental-12-8-2022/)). This reports the Ada architecture for NVIDIA 4000 series, fixes DLSS from failing on Ada and later cards, prevents startup crashes with *Monster Hunter World* on Turing and later cards, internal optimzations, and some other features.

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog).

*Cover image credit: frecle*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
