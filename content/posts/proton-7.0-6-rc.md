+++
title = "Proton 7.0-6 Now Available for Testing, Adds Compatibility with Gotham Knights and UNCHARTED Collection, Fixes 20 Bugs"
date = 2022-12-22T10:24:56-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton_rc/7.0-6.jpg"
tags = ["news", "software update", "proton rc"]
keywords = ["proton", "proton experimental", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Somehow I missed this. This has been around for a week now (thanks to [GOL](https://www.gamingonlinux.com/2022/12/proton-70-6-now-in-testing-for-steam-deck-linux-desktop/) for noticing). At any rate, Proton 7.0-6 is now available as a release candidate. Playable titles include:
- [*Gotham Knights*](https://store.steampowered.com/app/1496790/Gotham_Knights/)
- [*UNCHARTED: Legacy of Thieves Collection*](https://store.steampowered.com/app/1659420/UNCHARTED_Legacy_of_Thieves_Collection/)
- [*Wargame: Red Dragon*](https://store.steampowered.com/app/251060/Wargame_Red_Dragon/)
- [*Heroes of the Dark*](https://store.steampowered.com/app/1851330/Heroes_Of_The_Dark/)
- [*Super Arcade Racing*](https://store.steampowered.com/app/1103770/Super_Arcade_Racing/)
- [*Crazy Machines 3*](https://store.steampowered.com/app/351920/Crazy_Machines_3/)
- [*NinNinDays2*](https://store.steampowered.com/app/1698030/NinNinDays2/)
- [*雀姬 (Mahjong ladies)*](https://store.steampowered.com/app/1084520/_/)

20 bugs have been fixed, ranging from the OSK on Deck for *A Plague Tale: Requiem*, Xbox Live login fail for *As Dusk Falls*, multiple monitor support for *Project CARS 2*, and the blank window when starting the EA app launcher. Four of them are dedicated just to *Microsoft Flight Simulator*:
- Fix Microsoft Flight Simulator crashing during longer flights.
- Fix Microsoft Flight Simulator not displaying live traffic.
- Fix Microsoft Flight Simulator not starting after a recent game update.
- Fix Microsoft Flight Simulator crashing when starting next to big cities.
- Fix being unable to log in to Xbox Live from Main Menu in As Dusk Falls.
- Fix Septerra Core hanging on redistributables installation.
- Fix Super House of Dead Ninjas, Enemy Mind, and Out There Somewhere frame hitching every few seconds.
- Fix on-screen keyboard popping up every time when starting A Plague Tale: Requiem on the Steam Deck.
- Fix Zeepkist freezing when using controller.
- Fix Overcooked! All You Can Eat being unable to add a second controller-using player.
- Fix Quake III: Arena and Quake III: Team Arena displaying weird texture over the menu.
- Fix the new EA launcher displaying a blank window.
- Fix Marvel Snap not being able connect to online services.
- Fix Sackboy: A Big Adventure failing to start the first time it's launched.
- Fix Spyro Reignited Trilogy playing intro video in a wrong language.
- Fix Jurassic World Evolution 2 bad performance with recent Proton versions.
- Fix multiple monitor support in Project Cars 2.
- Fix Korean not being rendered correctly in Romance of the Three Kingdoms XIII launcher.
- Fix multiple languages not rendering correctly in Sins of a Solar Empire: Rebellion.
- Fix Lost Lands: Dark Overlord, Lost Lands: Dark Lord, Lost Lands: Redemption, and Haunted Hotel: Silent Waters Collector's Edition crashing when trying to set a wallpaper.

Additionally, wine-mono has been updated to [7.4.0](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.0), and DXVK-NVAPI to [0.6](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6). The latter update reports the Ada architecture for NVIDIA 4000 series, fixes DLSS from failing on Ada and later cards, prevents startup crashes with *Monster Hunter World* on Turing and later cards, internal optimzations, and some other features.

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/issues/6385). If you come across any issues with this release, be sure to report them on that thread.

As a reminder, to get access to the release candidate build, right-click Proton 7.0 in your Steam library (make sure "Tools" is checked off on the top-left dropdown menu to see it) -> Properties -> Betas -> Select `release-candidate` from the dropdown menu.

![Selecting Proton 7.0-6 RC](/images/proton_rc/switching_to_7.0-6.png)

*Cover image credit: Warner Bros. Games*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
