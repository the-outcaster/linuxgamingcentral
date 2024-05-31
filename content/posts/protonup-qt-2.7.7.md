+++
title = "ProtonUp-Qt 2.7.7 Adds NorthstarProton and Steam-Play-None Compatibility Tools, ProtonDB Ratings to Game List"
date = 2022-12-24T09:48:18-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/protonup-qt/2.7.7/cover.png"
tags = ["news", "software update", "protonup-qt"]
keywords = ["protonup-qt", "proton", "ge-proton", "northstarproton", "steam-play-none", "d8vk", "vkd3d", "protondb", "lutris"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
We've got a sweet new release for the excellent ProtonUp-Qt app, for managing all of your compatibility tools for Steam, Lutris, and more.

When viewing your game list, you can now check the ProtonDB ranking with the simple click of a button. Super convenient!

![ProtonUp-Qt ProtonDB ratings](/images/protonup-qt/2.7.7/protondb.png)

[NorthstarProton](https://github.com/cyrv6737/NorthstarProton) and [Steam-Play-None](https://github.com/Scrumplex/Steam-Play-None) have been added as compatibility tools. The former is "a Proton build based on TKG's Proton-tkg build system to run the Northstar client on Linux and SteamDeck, along with some enhancements out-of-the-box." It's basically the runner for *Titanfall 2*. The latter forces games with native clients to use said client, even if Valve recommends Proton.

![ProtonUp-Qt Northstar-Proton](/images/protonup-qt/2.7.7/northstar-proton.png)

![ProtonUp-Qt Steam-Play-None](/images/protonup-qt/2.7.7/steam-play-none.png)

For Lutris, you can now install [D8VK](https://github.com/AlpyneDreams/d8vk) and [VKD3D-Proton](https://github.com/HansKristian-Work/vkd3d-proton).

![ProtonUp-Qt D8VK](/images/protonup-qt/2.7.7/d8vk.png)

![ProtonUp-Qt vkd3d-proton](/images/protonup-qt/2.7.7/vkd3d-proton.png)

If you don't have an Internet connection, there will be an indicator. Or, at least there *should* be. I tested this and the window just says "Fetching releases..."

Finally, game list display should now work with the Flatpak version of Steam and after a recent [Steam update](https://github.com/DavidoTek/ProtonUp-Qt/issues/155).

**Important: in order to see the new compatibility tools, you will need to check off "Enable advanced mode" from the About window!**

![About ProtonUp-Qt](/images/protonup-qt/2.7.7/about.png)

Special thanks to **sonic2kk** -- who is also a [SteamTinkerLaunch contributor](https://linuxgamingcentral.com/posts/sonic-frontiers-modding-guide/) -- for making this release possible.

See the patch notes and download on [GitHub](https://github.com/DavidoTek/ProtonUp-Qt/releases/tag/v2.7.7).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
