+++
title = "GE-Proton7-15 Released, Enables Fall Guys Compatibility and Video Fixes for Several Titles"
date = 2022-04-22T11:10:41-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fall_guys/cover.jpg"
tags = ["software update", "ge-proton"]
keywords = ["ge-proton", "valve", "glorious eggroll", "fall guys"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Following hot off the heels of the official [Proton 7.0-2](https://linuxgamingcentral.com/posts/news-proton-7.0-2-released/) release yesterday, the developer of GE-Proton has followed up with [GE-Proton7-15](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-15). Included in this release is a few protonfixes for *State of Decay 2* and *Fall Guys*. The former no longer crashes, and now apparently the [*Fall Guys* EAC works on Proton!](https://linuxgamingcentral.com/posts/fall_guys_now_playable/) You no longer have to apply those weird tweaks anymore.

`WINE_DO_NOT_CREATE_DXGI_DEVICE_MANAGER` is a video fix that was enabled for the following titles:

- *Car Mechanic Simulator 2021*
- *Harspace: Shipbreaker*
- *Solasta*
- *Monster Train*
- *The Complex*
- *Cook-Out*
- *DJMAX Respect V*
- *Gloomhaven*

(Note that some of these titles already pulled in playback support in Proton 7.0-2.)

vp9 support was added for *Ghostwire: Tokyo* (in other words, video playback now works). Finally, the following tools were upgraded:

- Steam runtime/SDK
- "Various build commits pulled from upstream Proton"
- `vkd3d-proton`
- `dxvk` (to latest commit)
- `dxvk-nvapi` (to latest commit)
- `wine` (to latest bleeding-edge)

See the full patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-15). Also, if you're looking for a guide on how to install GE-Proton, I've got you [covered](https://linuxgamingcentral.com/posts/proton_ge_tutorial/).

*Cover image credit: fanbyte.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
