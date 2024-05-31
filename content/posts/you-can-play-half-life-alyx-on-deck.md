+++
title = "You Can Play Half-Life: Alyx on Steam Deck"
date = 2023-03-30T15:37:22Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/hla/cover.webp"
tags = ["news", "steam deck", "half life"]
keywords = ["half life alyx on steam deck", "half life alyx"]
description = "No VR required!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Well, here's a bit of a surprise. Modders have been able to remove the VR requirement for *Half-Life: Alyx*. You no longer need to buy that $1,000 Valve Index kit in order to play the game that has been rated "Overwhelmingly Positive" on Steam.

And it seems like it's possible to get the game running pretty smoothly on Deck. YouTuber Deck Wizard [goes over the process of getting it to work on Deck](https://www.youtube.com/watch?v=sQcOA6Ex8dA) and shows off some gameplay footage. The process to get it to work on Deck is as follows:
1. After the game is installed, go to Desktop Mode and clone the [HLA-NOVR-Script repo](https://github.com/bfeber/hla-novr-script).
2. Copy the `game` folder to your game's install directory, overwriting the existing files if prompted. (By default the install directory is `~/.steam/steam/steamapps/common/Half-Life Alyx/`)
3. Add the following launch options: `-novr -vsync -console -vconsole -w 1280 -h 800`
4. Change the controller layout to "Half-Life Alyx NoVR - OFFICIAL STEAM DECK LAYOUT" from the Community Layouts tab.

A couple of caveats to keep in mind, for now:
- the mod uses the *Half-Life 2* HUD
- can only play up to chapter 7

Nice. *Half-Life: Alyx* is available on [Steam](https://store.steampowered.com/app/546560/HalfLife_Alyx/).

*Cover image credit: Deck Wizard*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
