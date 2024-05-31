+++
title = "NVIDIA Image Scaling Now Merged With GameScope"
date = 2022-05-18T21:43:46-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvidia/cover.jpg"
tags = ["news", "nvidia", "gamescope"]
keywords = ["gamescope", "nvidia"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[GameScope](https://github.com/Plagman/gamescope), the micro-compositor formerly known as steamcompmgr, recently [merged](https://github.com/Plagman/gamescope/pull/488) support for NVIDIA's image scaling technology as of yesterday. Theoretically this means NVIDIA users should now be able to make use of GameScope (just make sure you add `-Y` or `--nis-upscaling` when using). Previously, only AMD users could make use of the technology (technically Intel has it too, albeit in limited capacity).

Don't get too excited. Someone has already [reported](https://github.com/Plagman/gamescope/issues/498) that the scaling technology doesn't work on a 940M. Keep in mind you'll also need NVIDIA's latest beta driver as of the time of writing this, [515.43.04](https://www.nvidia.com/download/driverResults.aspx/187826/en-us), in order to make use out of it.

But hopefully this will be good news if Valve was waiting for NVIDIA to support GameScope before releasing SteamOS 3 to be used on devices outside of the Steam Deck.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
