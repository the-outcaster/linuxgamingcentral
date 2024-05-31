+++
title = "GE-Proton8-27 Fixes Farlight 84, Renegade Ops, The Forest"
date = 2024-01-09T19:38:04Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/8-27.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "farlight 84", "beam.ng.drive", "blazblue centralfiction", "renegade ops", "the great ace attorney chronicles", "the forest", "super naughty maid 2", "nvidia reflex"]
description = "As well as fixes for a few other games."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Thomas Crider is "back from visiting" his "family for the holidays and thus work is back in full swing." So here's what we got with yesterday's update to GE-Proton.

Fixes have either been added or updated for the following titles:
- [*Farlight 84*](https://store.steampowered.com/app/1928420/Farlight_84/)
- [*Beam.NG.Drive*](https://store.steampowered.com/app/284160/BeamNGdrive/)
- [*BlazBlue Centralfiction*](https://store.steampowered.com/app/586140/BlazBlue_Centralfiction/)
- [*Renegade Ops*](https://store.steampowered.com/app/99300/Renegade_Ops/)
- [*The Great Ace Attorney Chronicles*](https://store.steampowered.com/app/1158850/The_Great_Ace_Attorney_Chronicles/)
- [*The Forest*](https://store.steampowered.com/app/242760/The_Forest/)
- [*Super Naughty Maid 2*](https://store.steampowered.com/app/1097880/Super_Naughty_Maid_2/)

There is now a "unified fix" for the following:
- CPU topology
- ProtonAudioConv
- XLiveLess XLive (I guess this is a [mod](https://gtamods.com/wiki/XLiveLess) for *GTA 4*)
- Esync/Fsync enable/disable

NVIDIA Reflex was initially implemented in 8-26 but was quickly pulled away a few hours later with the 8-27 hotfix:
> After discussion with dxvk devs they are currently deemed problematic and need more work, and are known to currently cause stutters in games even when the feature is disabled. We will re-enable the patches when they are ready.

A fix was backported for HID devices with more than 8 axes.

Finally, Wine, DXVK, VKD3D-Proton, DXVK-NVAPI, and "latest upstream Proton bleeding edge changes" have all been updated to bleeding edge or git.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton8-27).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
