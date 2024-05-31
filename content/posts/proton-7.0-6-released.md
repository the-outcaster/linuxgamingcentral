+++
title = "Proton 7.0-6 Adds Compatibility to Eight New Titles, Including Gotham Knights and Uncharted Collection, Fixes Ubisoft Connect Launcher Failure"
date = 2023-02-03T18:23:45Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton_rc/7.0-6.jpg"
tags = ["news", "software update", "proton"]
keywords = ["proton", "proton 7.0-6", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gotham knights", "uncharted legacy of thieves collection"]
description = "This, plus 22 bugs fixes and improved video playback with a few titles."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Nearly two months after Proton 7.0-6 entered as [release candidate](https://linuxgamingcentral.com/posts/proton-7.0-6-rc/), then going to [Proton Next](https://linuxgamingcentral.com/posts/proton-next-7.0-6/), said version of Proton has now finally landed as stable. Eight new games are playable with this jam-packed update, a fix made it in for the [Ubisoft Connect launcher](https://linuxgamingcentral.com/posts/ubisoft-stance-on-steam-deck-support/), and many other fixes made it in for games like *Microsoft Flight Simulator*, *Persona 5 Royal*, *Marvel Snap*, and plenty of other titles.

The following titles are now playable:
- [*Gotham Knights*](https://store.steampowered.com/app/1496790/Gotham_Knights/)
- [*UNCHARTED: Legacy of Thieves Collection*](https://store.steampowered.com/app/1659420/UNCHARTED_Legacy_of_Thieves_Collection/)
- [*Heroes of the Dark*](https://store.steampowered.com/app/1851330/Heroes_Of_The_Dark/)
- [*Super Arcade Racing*](https://store.steampowered.com/app/1103770/Super_Arcade_Racing/)
- [*Crazy Machines 3*](https://store.steampowered.com/app/351920/Crazy_Machines_3/)
- [*King under the Mountain*](https://store.steampowered.com/app/930230/King_under_the_Mountain/)
- [*NinNinDays2*](https://store.steampowered.com/app/1698030/NinNinDays2/)
- [*雀姬 (Mahjong ladies)*](https://store.steampowered.com/app/1084520/_/)

Note however, that unlike Proton Next, [*Wargame: Red Dragon*](https://store.steampowered.com/app/251060/Wargame_Red_Dragon/) is apparently no longer a playable title. Instead, a different game has been added to the list: [*King under the Mountain*](https://store.steampowered.com/app/930230/King_under_the_Mountain/).

A total of 22 bugs were fixed:
- Fix Ubisoft Connect launcher failure caused by launcher update.
- Fix the new EA launcher displaying a blank window.
- Fix *Septerra Core* hanging on redistributables installation.
- Fix *Persona 5 Royal* crashing when creating game save data.
- Fix *Vampire Survivors* intermittent error message.
- Fix *Super House of Dead Ninjas*, *Enemy Mind*, and *Out There Somewhere* frame hitching every few seconds.
- Fix *Zeepkist* freezing when using controller.
- Fix *Overcooked! All You Can Eat* being unable to add a second controller-using player.
- Fix *Quake III: Arena* and *Quake III: Team Arena* displaying weird texture over the menu.
- Fix *Marvel Snap* not being able connect to online services.
- Fix *Microsoft Flight Simulator* crashing during longer flights.
- Fix *Microsoft Flight Simulator* not displaying live traffic.
- Fix *Microsoft Flight Simulator* not starting after a recent game update.
- Fix *Microsoft Flight Simulator* crashing when starting next to big cities.
- Fix *Sackboy: A Big Adventure* failing to start the first time it's launched.
- Fix *Spyro Reignited Trilogy* playing intro video in a wrong language.
- Fix *Jurassic World Evolution 2* bad performance with recent Proton versions.
- Fix multiple monitor support in *Project Cars 2* and *Project Cars 3*.
- Fix Korean not being rendered correctly in *Romance of the Three Kingdoms XIII* launcher.
- Fix multiple languages not rendering correctly in *Sins of a Solar Empire: Rebellion*.
- Fix *Lost Lands: Dark Overlord*, *Lost Lands: Dark Lord*, *Lost Lands: Redemption*, and *Haunted Hotel: Silent Waters Collector's Edition* crashing when trying to set a wallpaper.
- Fix video playback regression with *Chronos: Before the Ashes*.

Some other updates:
- Improve video playback with *OUTRIDERS* and *ToGather: Island*.
- Update wine-mono to [7.4.0](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.0).
- Update dxvk-nvapi to [v0.6](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6) -- this update reports the Ada architecture for NVIDIA 4000 series, fixes DLSS from failing on Ada and later cards, prevents startup crashes with *Monster Hunter World* on Turing and later cards, internal optimzations, and some other features

An update should be available to Proton in your Steam library. Download it, restart the Steam client, and you should be good to go!

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog#70-6).

*Cover image credit: Warner Bros. Games*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
