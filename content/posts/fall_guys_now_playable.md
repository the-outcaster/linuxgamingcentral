+++
title = "Apparently Fall Guys Now Works with Proton Experimental (Bleeding-Edge Branch)"
date = 2022-03-29T12:40:06-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://www.fanbyte.com/wp-content/uploads/2020/08/fall-guys-title.jpg?x96128"
tags = ["new proton game", "eac"]
keywords = ["fall guys", "eac", "proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Someone had recently wrote a [ProtonDB report](https://www.protondb.com/app/1097150#aRzxJIFk7c) for [*Fall Guys*](https://store.steampowered.com/app/1097150/Fall_Guys_Ultimate_Knockout/) that adds instructions to get the game to work through Proton. When Easy Anti-Cheat was [added to the game](https://www.reddit.com/r/FallGuysGame/comments/it76jf/fall_guys_has_received_an_update_adding_easy/) a few years ago, unfortunately the massively popular game would no longer work on Linux with Proton.

According to the new ProtonDB report, the good news now is it's apparently playable on Proton once again. The report adds the following instructions:
1. Opt-in to the `bleeding-edge` branch for Proton Experimental (right-click Proton Experimental from your Steam library, go to *Properties -> Betas -> Select `bleeding-edge` from the dropdown menu*)
2. Copy the `easyanticheat_x64.so` file from `(game installation directory)/EasyAntiCheat/` to `(game install dir)/FallGuys_client_game_Data/Plugins/x86_64/.`
3. Change the first line in the `FallGuys_client.ini` file found in the game's installation directory to `TargetApplicationPath=FallGuys_client_game.exe`

Seems like a little bit of a hacky approach, but I'm happy for anyone who has been wanting to play this on Linux. I don't own the game myself so I can't test to verify. Make sure you back up your Proton/Wine prefixes as well before launching the game. And for all I know this might not be official; later down the line something may come up that breaks compatibility once again.

Let me know if it works for you!

*Cover image credit: FanByte*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
