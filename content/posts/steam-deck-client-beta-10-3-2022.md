+++
title = "Steam Deck Client Beta Makes Custom Boot Animations Even Easier, Automatically Scales Resolution when Connected to External Display"
date = 2022-10-03T22:13:50-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "software update", "steam deck", "steam deck client update"]
keywords = ["steam deck", "steamos", "custom boot video", "external display scaling"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Remember that tutorial on [how to replace the Deck's bootloader animation?](https://linuxgamingcentral.com/posts/how-to-replace-steam-deck-boot-video/) Well, all these guides that have been popping up caught Valve's attention. Today's new beta Deck client update makes this process even easier. Custom videos will now go in `/home/deck/.local/share/Steam/steamui/overrides/movies/` (note that this directory will need to be made first). These videos will now be in a safer place, and they won't get wiped with every update. Not only this, but these videos will be played in fullscreen automatically; no need to modify the `library.css` file!

Some other goodies have made it with this update. A toggle has been added which will automatically scale the Deck's resolution when connected to an external display for the best performance. An issue regarding startup haptics has been fixed.

See the patch notes on [Steam](https://store.steampowered.com/news/app/1675200/view/3301726014480099879).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
