+++
title = "Halo Infinite Now Runs on Deck!"
date = 2022-07-20T14:28:10-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/photos/halo_infinite.jpg"
tags = ["news", "halo infinite", "steam deck"]
keywords = ["halo infinite", "steam deck", "ge-proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*UPDATE (7/22): I've put out a [guide](https://linuxgamingcentral.com/posts/halo-infinite-on-deck-guide/) for those of you who can't get the game to run, plus what I've found to be the best settings for a smooth 60 FPS.*

Earlier today GloriousEggroll released [GE-Proton7-26](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-26). Though this update is rather minor compared to 7-25, it nevertheless fixes a regression in `vkd3d-proton` that prevented *Halo Infinite* from going past the initial screen.

Low and behold, the game not only runs, but the textures have been fixed! No need to apply GE's custom Mesa patch on AMD anymore!

On the default graphics settings, I noticed the audio was quite stretchy, and the framerate was poor. After lowering to Medium settings and restarting the game, the audio stretchiness is gone and it comfortably plays around 45-50 FPS. I'm sure I could acheive 60 by lowering the resolution and using FSR, but I just set the refresh rate to 45 Hz.

I haven't tested single-player as I don't own the DLC, but multiplayer has been working so far. Keep in mind you'll still need to rename or delete the video files found in the `videos` folder in the game's install directory, and the mouse cursor is still stuck at the center of the screen.

*Halo Infinite* is available on [Steam](https://store.steampowered.com/app/1240440/Halo_Infinite/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
