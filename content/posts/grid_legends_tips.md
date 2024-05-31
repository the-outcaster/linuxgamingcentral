+++
title = "Getting the Best Experience for GRID Legends on NVIDIA"
date = 2022-03-15T13:28:52-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://cdn.akamai.steamstatic.com/steam/apps/1307710/ss_d9ed036463f9c93539174d24d930e5b62766b6c1.jpg?t=1646752436"
tags = ["tips", "racing"]
keywords = ["grid legends", "nvidia", "proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you have [*GRID Legends*](https://store.steampowered.com/app/1307710/GRID_Legends/) but have been tired of the constant crashing on NVIDIA graphics cards, well, I may very well have a solution to that.

The **TL;DR** of this article is essentially:
- add `dxvk.conf` to the game's installation directory, then add `dxgi.nvapiHack = False` to get rid of the AMD driver error on launch
- Use Medium graphics settings or lower to avoid crashes

I got *GRID Legends* as part of my subscription to EA Play. Once I got the game installed, I would get this error every time I launched it:

![grid legends amd driver error on launch](https://user-images.githubusercontent.com/12868939/155752338-0f40f74e-8f2c-4eeb-924d-a89d6c6c53e6.png)

The error can be ignored and the game will still launch. But then, after any sort of race, the game would just crash. After tinkering with the game some more today, I have a solution for both problems.

You'll first want to add a file named `dxvk.conf` within the game's installation directory. Add this line to it, then save the file:

`dxgi.nvapiHack = False`

This will remove the AMD driver error when launching the game with a NVIDIA GPU. Now when you get into the game, if your graphics settings are set to High or Ultra High, tone it down to Medium. Restart the game and you're all set. You shouldn't be getting any more crashes or launcher errors throughout the time you play the game.

Not sure what is the problem with High and Ultra High settings. There must be some sort of video option that breaks Proton compatibility on NVIDIA.

Speaking of Proton, I've found that the game works best with the stable **7.0-1** release. Proton Experimental and Proton GE would not work. I think that may be due to the Denuvo DRM getting triggered though; that can happen if you change Proton versions too often.

![grid legends screenshot from steam store](https://cdn.akamai.steamstatic.com/steam/apps/1307710/ss_e404e8327cb798060209238575b550473979740b.1920x1080.jpg?t=1646752436)

Note that if you're on AMD, you shouldn't have to do any of this, at least according to the reports on [ProtonDB](https://www.protondb.com/app/1307710). You should be able to play on any preset and have a stable experience. Well, except on the Steam Deck, because apparently it doesn't work on the handheld for some reason.

Some optional things you may want to do to get an even better experience, regardless of whether you're using NVIDIA or not, is:
- skip the intro video on startup by renaming the `cm_logo.bk2` file found in `(game install dir)/ui_package/videos/` to `cm_logo.bk2.bak`
- use [GameMode](https://github.com/FeralInteractive/gamemode) for higher framerates
- use FSR and set the in-game resolution to something lower than your monitor's native resolution

So, your Steam launch parameters would be something like:

`WINE_FULLSCREEN_FSR=1 gamemoderun %command%`

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
