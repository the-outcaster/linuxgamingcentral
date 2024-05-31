+++
title = "You Can Play Genshin Impact on Deck"
date = 2023-04-04T20:24:52Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/genshin_impact.webp"
tags = ["news", "steam deck", "genshin impact"]
keywords = ["genshin impact on steam deck", "genshin impact"]
description = "Weeb anime lovers, rejoice that your favorite game now runs on Deck."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**UPDATE (4/12/2023):** According to [Steam Deck Gaming](https://www.steamdeckgaming.net/post/genshin-impact-is-no-longer-working-on-steam-deck-since-update-3-6), *Genshin Impact* no longer runs on Deck with the recent 3.6 update. They report "the game no longer loads and sits on a black screen."

In the meantime, I suppose you could try An Anime Game Launcher. I'm not going to link to the GitHub repo since the devs asked so, but a quick Google search should lead you to it along with a few YouTube tutorials. 

*Original article:*

Steam Deck Gaming has figured out [how to get *Genshin Impact* running on Steam Deck](https://www.youtube.com/watch?v=SQYp6prSf88). They note:
> It will take some time, the install process and verification process takes a long time so be sure to set a couple of hours aside to get up and running or do it in-between other tasks.

They also mention you'll need a whopping *135 GB* of available hard drive space to install.

Don't let the 34 total steps daunt you -- it's not that difficult. You'll have to download the [*Genshin Impact* installer](https://genshin.hoyoverse.com/en/), add it as a non-Steam game, force Proton Experimental, and install the bad boy. Step 13 notes "Once the download is complete it will likely get stuck verifying resources, exit the launcher at this point, otherwise let it complete."

![Genshin Impact in-game on Deck](/images/steam_deck/genshin_impact_in_game.webp)

From there you'll need to add the `launcher.exe` file as a non-Steam game, which will be located inside the `compatdata` folder. Set Proton Experimental as the compatibility tool. Run the launcher again, set auto-launch to on, and show pop-up when exiting game. Make sure "Gamepad with Joystick Trackpad" is set as the controller profile in Game Mode. You'll need to use the touchscreen in the main menu, then change the control type to controller from the Settings menu.

For optimized gameplay, set the game to Low settings, and cap the framerate to 45 FPS.

Steam Deck Checker also has a [written post](https://www.steamdeckgaming.net/post/how-to-play-genshin-impact-on-steam-deck-steam-os) in addition to the video if you'd like to learn more.

*Images are credit of Steam Deck Gaming*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
