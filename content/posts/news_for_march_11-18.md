+++
title = "News Round-Up for March 11-18 (New Stadia Tech)"
date = 2022-03-19T12:47:19-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://chubimon.com/wp-content/uploads/2022/03/Steam-Deck-Now-Supports-Xbox-Game-Pass-and-Cloud-Thanks.jpg?is-pending-load=1"
tags = ["news", "steam deck"]
keywords = ["proton ge", "linux gaming", "foss"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Was hoping to get this out yesterday but time flies. Hope a day late isn't going to bother anyone.

# News
- Steam Deck-related
  - ETA Prime -- A YouTuber that mostly focuses on emulation -- released a Steam Deck review last week, and covers the gaming as well as the emulation aspect of the Deck. Needless to say, the Deck is one of the most powerful handhelds out there for emulation. [Gameranx](https://youtu.be/Xp9yvwJmrX4) also had a video review
{{< youtube "9upVLaFRh_I" >}}
  
  - That Boiling Steam contributer that got a Steam Deck? He recently wrote [his first impressions](https://boilingsteam.com/steam-deck-first-impressions/) of the device
  - Microsoft has announced official support of the Xbox Game Pass Ultimate subscription on the Steam Deck. They've even included [documentation](https://support.microsoft.com/en-us/topic/xbox-cloud-gaming-in-microsoft-edge-with-steam-deck-43dd011b-0ce8-4810-8302-965be6d53296) on their support website
  - The Steam Deck [gets a 15 FPS option and a few new keyboard themes](https://www.gamingonlinux.com/2022/03/steam-deck-gets-a-15fps-option-new-keyboard-themes/)
![steam deck new keyboard theme](https://uploads.golmedia.net/uploads/articles/article_media/thumbs/12961985211647076883gol1.jpg)
*Image credit: GamingOnLinux*
  
  - The Steam Deck finally got a [low battery warning](https://boilingsteam.com/the-steam-deck-finally-gets-a-low-battery-indicator/). Somehow, this wasn't in the QA process prior to the official launch
  - We've almost hit the 1,500 mark for [verified/playable Steam Deck titles](https://boilingsteam.com/1400-games-on-the-steam-deck-including-doom-2016/). Over [80% of verified/playable titles are from 2015 onwards](https://boilingsteam.com/more-than-80-of-steam-deck-verified-playable-games-are-from-2015-onwards/)
  - The Lutris developer was [sent a Steam Deck by Valve](https://twitter.com/LutrisGaming/status/1502786834908135424) to assist with the development of the program on said device
{{< tweet "1502786834908135424" >}}
  
  - Some titles on the Deck, even though it may be Playable, can still have issues. An example is [*Grand Theft Auto V*](https://www.gamingonlinux.com/2022/03/steam-deck-verified-has-issues-grand-theft-auto-v-edition/)
  - The file size for the Steam Deck client [has been reduced](https://www.gamingonlinux.com/2022/03/valve-reduces-size-of-steam-deck-client-in-the-latest-update/)
  - *Witcher 3* is now [Steam Deck Verified](https://steamcommunity.com/games/292030/announcements/detail/4712459761457742331)

- Scoot Larson -- a computer repair and data recovery service technician -- recently [blogged](https://www.scottrlarson.com/publications/publication-transition-windows-to-linux/) about the increasingly anti-consumer nature that is Windows 11 and made the switch to Linux. To Pop!_OS in particular. Interesting read there as far as how his journey went.
- It's possible to [play *DOOM* on a $4 Raspberry Pi Pico](https://invidious.kavin.rocks/watch?v=vXr7tOR3dis)
- Several new native Linux titles are added to the Steam store every week. Check the post from [Boiling Steam](https://boilingsteam.com/new-steam-games-with-native-linux-clients-2022-03-15-edition/) to learn more. A few games include *Pompom*, *Halftime Heroes*, and *Billiards of the Round Table*
- Google is working on building a Windows emulator from the ground up for Linux for their Stadia tech
{{< youtube "8-N7wDCRohg" >}}
- After years of rumors, Steam for ChromeOS [is finally coming](https://9to5google.com/2022/02/19/steam-chrome-os-supported-chromebooks/). Chromebooks that will have the initial support include a few Acer, ASUS, HP, and a few other devices
- Asahi Linux -- a distro that supports Apple's M1 chipset -- has released it's first [alpha](https://asahilinux.org/2022/03/asahi-linux-alpha-release/). Asahi Linux is a customized version of Arch Linux ARM with the Plasma desktop environment. Some things don't work just yet, including the DisplayPort, webcam, Bluetooth, GPU acceleration, and a few others
- I had written a review of the [Kudu laptop by System76](https://boilingsteam.com/the-kudu-laptop-what-system76-does-best/) over on Boiling Steam. This powerful laptop ships with Pop!_OS 21.10 and comes with a Ryzen 9 5900HX and a RTX 3060, with 16 GB RAM
- *Apex Legends* apparently [stopped working](https://www.gamingonlinux.com/2022/03/apex-legends-now-broken-on-steam-deck-and-linux-desktops/) on Proton/the Deck, but now it's working again
- The Linux and Mac ports for *Psychonauts 2* [are still coming](https://www.fig.co/campaigns/psychonauts-2/updates/1504)
- AMD's FSR will soon be upgraded to version [2.0](https://gpuopen.com/fsr2-announce/)

# Software Updates/Releases
- Iris [1.2.2](https://github.com/IrisShaders/Iris/releases/tag/1.18.x-v1.2.2) was released for *Minecraft*. Iris enhances the graphical fidelity of the game. v1.2.2 fixes a low performance regression, updates two translations, and contains a few other bug fixes
- A project that's been in the works for quite a while now, but something I still wanted to highlight, is a game called [*Liblast*](https://codeberg.org/unfa/Liblast) (short for Libre Blast). It's a FOSS 3D FPS created with Godot 4
- Recalbox -- an emulation-oriented distro for Odroid, Raspberry Pi, and other devices -- was updated to [8.1-Beta10](https://gitlab.com/recalbox/recalbox/-/releases/8.1-Beta10). This release provides a bunch of bug fixes
- Bottles has been updated to [2022.3.14-trento](https://github.com/bottlesdevs/Bottles/releases/tag/2022.3.14-trento). This brings MangoHUD support, experimental support for Steam Proton prefixes, support for GE-Proton runners, improvements to the Wine backend, and plenty of other features and bug fixes
- [*MineClone 2*](https://content.minetest.net/packages/Wuzzy/mineclone2/) -- a survival game for *MineTest* -- has recently been updated to 0.72.0. It's been over a year since the last release, but unfortunately I'm not able to find what's new with this release
- Rare -- an alternative to the Heroic Games Launcher, written in Python -- was updated to [1.8.8](https://github.com/Dummerle/Rare/releases/tag/1.8.8). This release includes Discord real-time presence (RPC), fixes to the launcher crashing, fixes to color schemes, as well as a few other bug fixes
![rare launcher](https://github.com/Dummerle/Rare/blob/main/Screenshots/Rare.png?raw=true)
*Image credit: Rare on GitHub*

- Lakka -- a distro which transforms a computer into a retro emulation console, similar to Recalbox -- was updated to [v4.0](https://github.com/libretro/Lakka-LibreELEC/blob/Lakka-v4.x/CHANGELOG.md). This upgrades the Mesa drivers, RetroArch, the mainline kernel, the Raspberry Pi kernel/firmware, and LibreELEC. New libretro cores were added: `sameduck` and `superbroswar`. There's a few other changes as well
- Lapce -- a "lightning-fast and powerful code editor" -- has been updated to [v0.0.11](https://github.com/lapce/lapce/releases/tag/v0.0.11). This brings the new Code Lens feature, and also supports multiple cursors
- Wine [7.4](https://www.winehq.org/announce/7.4) was released. This sets the light theme as the default theme, converted WineD3D, D3d12, and DXGI modules, bug fixes, a bundled vkd3d library, and large scale cleanups to support 'long' type
- [GE-Proton7-10](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-10) was released. This upgrades wine, dxvk, and vkd3d-proton. It also adds video support for *Nioh 2* and *Persona 5 Strikers*

I know for a fact there's some other news that I missed, but I just wanted to cover the more interesting topics.

*Cover image courtesy of Chubimon.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
