+++
title = "Weekly News Recap (Kernel 6.1 on Deck, The Beginning of the RISC-V Era, D8VK)"
date = 2023-02-19T18:10:01Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/weekly_news/2_4-17.avif"
tags = ["weekly news"]
keywords = ["metroid prime remastered", "visionfive 2", "risc-v", "steamos 3.5", "framework ssds", "chimeraos", "clunky hero", "steam old bpm", "luke short", "winesapos", "d8vk"]
description = "Oh, and did I mention Metroid Prime Remastered?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Going over two weeks' worth of info since I missed last weekend, so let's get right to it!

# Steam Deck
- stable update [adds fast jump by letter, settings for initial OSK position](https://linuxgamingcentral.com/posts/steam-deck-client-stable-update-2-10-2023/)
- beta update [adds LAN game transfer support between desktop and Deck](https://linuxgamingcentral.com/posts/steam-deck-client-beta-update-2-17-2023/)
- you can [customize the theme, BGM, and SFX](https://linuxgamingcentral.com/posts/customize-steam-deck-theme-music-and-sfx/)
  - going along with this, you can also add [your own BGM/SFX](https://linuxgamingcentral.com/posts/how-to-add-custom-bgm-and-sfx-to-steam-deck/)
- you can record the screen with [Decky-Recorder](https://linuxgamingcentral.com/posts/decky-recorder/)
- SteamOS 3.5 is getting [SMT disabled support and kernel 6.1](https://linuxgamingcentral.com/posts/updated-kernel-and-smt-disabled-with-steamos-3.5/)
- overclocking the RAM speed? It's possible, [but I don't recommend it](https://linuxgamingcentral.com/posts/overclocking-steam-deck-ram-is-possible/)
- Framework [temporarily offered 2 TB drives](https://frame.work/gb/en/blog/now-offering-2tb-ssds-for-steam-deck-in-the-framework), but unsurprisinly they sold out fairly quickly
- seems like [kernel 6.3 will be getting Deck controller interface support](https://www.phoronix.com/news/Steam-HID-Steam-Deck-Linux-6.3)

# Native Games
- I went over a Metroidvania called [*Clunky Hero*](https://linuxgamingcentral.com/posts/clunky-hero-review/) -- in some ways it's funny, in other ways it's frustrating
- strangely enough, *Bioshock Infinite* [gets a Linux fix](https://store.steampowered.com/news/app/8870/view/3641758659211388390)

# Hardware
- [VisionFive 2](https://boilingsteam.com/visionfive-2-a-raspberry-pi-like-moment-for-risc-v/) appears to be the RISC-V moment that Raspberry Pi started for ARM
- Phoronix benchmarks the [RTX 4080/4090](https://www.phoronix.com/review/nvidia-rtx4080-rtx4090-linux)

# Software Updates
- **ChimeraOS** [39](https://linuxgamingcentral.com/posts/chimeraos-39/) adds new splash animation on boot and uses the new BPM by default
- **GE-Proton** [7-49](https://linuxgamingcentral.com/posts/ge-proton7-49-and-wine-ge-proton7-37/) adds Ubisoft Connect launcher fix
- **winesapOS** [3.2.1](https://linuxgamingcentral.com/posts/winesapos-3.2.1/) switches to SteamOS 3.4 repo names and decreases the swappiness level
- **Wine** [8.2](https://linuxgamingcentral.com/posts/wine-8.2/) adds codec support for Indeo IV50, fixes keyboard glitch with FFXI
- **Proton Experimental** [2.16.2023](https://linuxgamingcentral.com/posts/proton-experimental-2-16-2023/) fixes multiplayer in *Age of Empires III*, improves monitor names in *Hogwarts Legacy*, and fixes keyboard input with *Wild Hearts*
- **KDE Plasma** [5.27](https://kde.org/announcements/plasma/5/5.27.0/) is a massive update that apparently brings Deck improvements
- **Box64** can now apparently [run the full Steam for Linux client](https://boilingsteam.com/box64-can-now-run-the-full-steam-linux-client-on-arm-hardware/) on ARM devices
- **Godot 4.0** releases [the first release candidate](https://godotengine.org/article/release-candidate-godot-4-0-rc-1/)

# Metroid Prime Remastered
- [plays great on Deck](https://linuxgamingcentral.com/posts/metroid-prime-remastered-on-steam-deck/); just make sure if you're using Yuzu to switch to docked mode (hold Start and then press Up on the D-pad)
- an already fantastic game was made even more fantastic; [here's my thoughts](https://linuxgamingcentral.com/posts/metroid-prime-remastered-review/)
- I have Steam Deck gameplay on [Ryujinx](https://www.youtube.com/watch?v=eEZTJ57Jqkg), [Yuzu](https://www.youtube.com/watch?v=AWvjK2L2paQ), and [compared both emulators](https://www.youtube.com/watch?v=8Olrz3jRsTc)
- sound effects and music on Deck? Yup, [I put that in there](https://www.youtube.com/shorts/aLkJIe7J00s)
- can you tell I'm a bit of a *Metroid* fan?

# Other
- old BPM is [being retired](https://linuxgamingcentral.com/posts/rip-old-bpm/)
  - in tandem with this, Steam for Linux is now [10 years old](https://www.gamingonlinux.com/2023/02/10-years-ago-steam-released-for-linux/)
- I had an interview with [Luke Short](https://linuxgamingcentral.com/posts/interview-with-luke-short-creator-of-winesapos/), the main developer behind the excellent winesapOS distribution
- [D8VK](https://github.com/AlpyneDreams/d8vk) aims to bring Direct3D 8 support to DXVK with older titles
- we should no longer be getting [shader cache downloaded and compiled on every reboot](https://github.com/ValveSoftware/steam-for-linux/issues/8076#issuecomment-1430641159)

*Cover image credit: Nirav Patel from [Framework](https://frame.work/gb/en/blog/now-offering-2tb-ssds-for-steam-deck-in-the-framework)*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
