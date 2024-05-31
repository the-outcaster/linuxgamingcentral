+++
title = "Proton 7.0-6 Now Available as Proton Next, Fixes Video Playback with Chronos: Before the Ashes, Improves Video Playback with OUTRIDERS and ToGather:Island"
date = 2023-01-08T04:20:58Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton/proton_next/7.0-6.jpg"
tags = ["news", "software update", "proton", "proton next"]
keywords = ["proton", "proton next", "proton 7.0-6", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gotham knights", "uncharted collection", "heroes of the dark", "super arcade racing", "crazy machines 3", "king under the mountain", "ninnindays2"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The day [Proton Experimental](https://linuxgamingcentral.com/posts/proton-experimental-update-1-06-2023/) got updated, was also the day Proton 7.0-6 graduated from [release candidate](https://linuxgamingcentral.com/posts/proton-7.0-6-rc/) to Proton Next.

The changes are almost exactly the same as the release candidate. As a reminder, playable titles include:
- [*Gotham Knights*](https://store.steampowered.com/app/1496790/Gotham_Knights/)
- [*UNCHARTED: Legacy of Thieves Collection*](https://store.steampowered.com/app/1659420/UNCHARTED_Legacy_of_Thieves_Collection/)
- [*Wargame: Red Dragon*](https://store.steampowered.com/app/251060/Wargame_Red_Dragon/)
- [*Heroes of the Dark*](https://store.steampowered.com/app/1851330/Heroes_Of_The_Dark/)
- [*Super Arcade Racing*](https://store.steampowered.com/app/1103770/Super_Arcade_Racing/)
- [*Crazy Machines 3*](https://store.steampowered.com/app/351920/Crazy_Machines_3/)
- [*NinNinDays2*](https://store.steampowered.com/app/1698030/NinNinDays2/)
- [*雀姬 (Mahjong ladies)*](https://store.steampowered.com/app/1084520/_/)

Bug fixes are as follows:
- fix *Microsoft Flight Simulator*:
  - crashing during longer flights
  - not displaying live traffic
  - not starting after a recent game update
  - crashing when starting next to big cities
- fix being unable to log in to Xbox Live from Main Menu in *As Dusk Falls*
- fix *Septerra Core* hanging on redistributables installation
- fix *Super House of Dead Ninjas*, *Enemy Mind*, and *Out There Somewhere* frame hitching every few seconds
- fix on-screen keyboard popping up every time when starting *A Plague Tale: Requiem* on the Steam Deck
- fix *Zeepkist* freezing when using controller
- fix *Overcooked! All You Can Eat* being unable to add a second controller-using player
- fix *Quake III: Arena* and *Quake III: Team Arena* displaying weird texture over the menu
- fix the new EA launcher displaying a blank window
- fix *Marvel Snap* not being able connect to online services
- fix *Sackboy: A Big Adventure* failing to start the first time it's launched
- fix *Spyro Reignited Trilogy* playing intro video in a wrong language
- fix *Jurassic World Evolution 2* bad performance with recent Proton versions
- fix multiple monitor support in *Project Cars 2*
- fix Korean not being rendered correctly in *Romance of the Three Kingdoms XIII* launcher
- fix multiple languages not rendering correctly in *Sins of a Solar Empire: Rebellion*
- fix *Lost Lands: Dark Overlord*, *Lost Lands: Dark Lord*, *Lost Lands: Redemption*, and *Haunted Hotel: Silent Waters Collector's Edition* crashing when trying to set a wallpaper

Wine-mono has been updated to [7.4.0](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.0), and DXVK-NVAPI to [0.6](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6). The latter update reports the Ada architecture for NVIDIA 4000 series, fixes DLSS from failing on Ada and later cards, prevents startup crashes with *Monster Hunter World* on Turing and later cards, internal optimzations, and some other features.

The only differences I'm seeing with the Proton Next release is:
- fix video playback regression with *Chronos: Before the Ashes*
- improve video playback with *OUTRIDERS* and *ToGather: Island*

To use Proton Next, right-click the game you want to use it with -> Properties -> Compatibility. Check off "Force the use of a specific Steam Play compatibility tool" if it's not already checked. From the dropdown menu, select "Proton Next". Steam will automatically download Proton Next if it's not installed on your system.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/proton/setting_up_proton_next_7.0-6.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Alternatively, if you wish to use it across *all* of your games, go to Steam -> Settings -> Steam Play. Check off "Enable Steam Play for all other titles" if it's not already checked, then select "Proton Next" from the dropdown menu. Restart Steam for the changes to take effect.

![Setting Proton Next across all Steam games](/images/proton/proton_next/set_across_all_games.png)

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog#70-6-available-as-proton-next).

*Cover image credit: Gunfire Games/THQ Nordic*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
