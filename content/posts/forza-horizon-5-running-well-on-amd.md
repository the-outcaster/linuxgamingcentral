+++
title = "Forza Horizon 5 Running \"Well\" On AMD"
date = 2023-04-23T16:33:13Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fh5/fh5.webp"
tags = ["news", "forza horizon series"]
keywords = ["forza horizon 5", "forza horizon 5 on linux", "forza horizon 5 on amd"]
description = "Game can be run without much stutter, but it's going to need some work."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Seems like there are some mixed reports about *Forza Horizon 5* compatibility on [ProtonDB](https://www.protondb.com/app/1551360). But Reddit user [d3vilguard](https://www.reddit.com/r/linux_gaming/comments/12w1vdi/finally_got_forza_horizon_5_running_well_amd/) seems to have found a solution on Linux desktop, with the 6600 XT.
> I've been battling with this game for a year now trying to get it to run smooth...after a moderate -80mV undervolt, a overclock of +100 on the core and +200 on the memory I can say that the stutters are gone. Gone for good! Game still crashes from time to time, but hear me out.. crashing frequency is the same as Windows.

They're using openSUSE Tumbleweed with KDE Wayland, with the native Steam package, stock kernel, and stock Mesa drivers. Here's what they did to get the game running decently:
- [hugepages](https://www.reddit.com/r/linux_gaming/comments/uhfjyt/underrated_advice_for_improving_gaming/) enabled
- "Performance" and "Compute" power modes set for the CPU and GPU respectively
- using Proton Experimental - bleeding edge
- GameMode enabled
- Steam overlay disabled
- GPU undervolted and overclocked; set with [CoreCtrl](https://linuxgamingcentral.com/posts/increase-power-on-amd-gpus/)
- fTMP and HPET disabled in BIOS
- resizable BAR/SAM enabled

In-game settings also had to be altered:
- SSAO quality set to OFF - this can apparently cause artifacts otherwise
- TAA set to OFF - causes crashing otherwise

See the game in action with their [video](https://www.youtube.com/watch?v=KHQvf46Tudo). The description notes that NVIDIA users should be "OK" with [Proton 8](https://linuxgamingcentral.com/posts/proton-8.0-1/) and also provides a guide on how to enable resizable bar with AMD.

Even after all this work, please be advised that kernel 6.2 or higher "can cause crashes on AMD GPUs."

Meantime, if you're on Deck, CryoByte33 has an excellent [video guide](https://www.youtube.com/watch?v=pceOIAGYdbM) for getting *Forza Horizon 5* to work nicely.

*Cover image credit: d3vilguard*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
