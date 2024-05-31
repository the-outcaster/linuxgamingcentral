+++
title = "Play Super Smash Bros. on Steam Deck/Linux? I Could Use Your Help with Some Testing"
date = 2023-12-26T04:32:25Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/competitive-smash-decker/cover.jpg"
tags = ["testers wanted", "smash bros", "slippi", "steam deck"]
keywords = ["smash 64 remix", "slippi", "project plus game", "project m ex remix", "pmex remix", "hewdraw remix", "smash bros on steam deck", "overclock gcc adapter on steam deck", "steam deck", "steam deck oled"]
description = "Made a script that allows you to easily install mods!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Over the past several days I have been huddled up on my laptop working away at a Swiss army knife script that does all things *Smash Bros.*. Though it's primarily intended to work with the Steam Deck, just about any Linux distro should also work -- except for the part of overclocking the GCC adapter, since that part is a little less distro-agnostic.

So what does the script do? It allows you to download, update, and play the following *Smash* mods:
- Smash 64 Remix (*Smash 64* with more characters and stages)
- Slippi (*Melee* with online multiplayer)
- Project+ (continuation of Project M, turning *Brawl* into a more competitive game)
- Project M EX Remix (Project+ with an expanded roster of characters and stages)
- HewDraw Remix (HDR - *Smash Ultimate* with competitive mechanics)

You can also view the patch notes for a few of the mods, get download links for Animelee and Diet Melee, and launch the netplay version of the associated emulator. If you have a GameCube controller adapter on hand you can also easily install/uninstall the overclock module.

![Screenshot](/images/steam_deck_oled/competitive-smash-decker/screenshot.png)

There will be a few inconveniences. For instance, if you want to download PMEX Remix, you'll have to manually download the mod for now. If you're looking to try out HDR you'll need to not only have a dump of *Smash Ultimate* but also your save file, update file, and any associated DLC and install these on Ryujinx.

To get started, head over to the [GitHub page](https://github.com/linuxgamingcentral/competitive-smash-decker). The README will provide instructions on what you need to do. Obviously, you're going to need to supply your own legally-dumped ROMs/ISOs and put them in the appropriate place in order for the script to work.

Give it a shot and let me know how it goes. If you have any suggestions or bug reports, be sure to file an issue on the tracker. I'll have a video tutorial soon. Have fun!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
