+++
title = "Proton 8.0-4 Adds Compatibility to Star Wars: KOTOR II, Fixes Overwatch 2 and EA Desktop App"
date = 2023-10-06T04:56:51Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton/8.0-4.jpg"
tags = ["news", "software update", "proton", "stable"]
keywords = ["proton", "proton 8.0-4", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "baldur's gate 3", "steam deck", "portal prelude rtx", "spider man mile morales", "rainbox six extraction", "star wars kotor 2", "ratchet and clank", "overwatch 2"]
description = "Plus NVAPI support for nearly two dozen titles and bug fixes for a dozen more!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After three weeks of testing, Proton 8.0-4 has now released as stable and is available for download on the Steam Deck and the desktop Steam client. This release adds a whole sloth of bug fixes, including regression fixes from earlier Proton 8 releases; compatibility to seven new titles; NVAPI support for nearly two dozen games; and the usual set of individual tool updates.

**Newly playable games** with this release include:
- Arthurian Legends
- CHAOS CODE -NEW SIGN OF CATSTROPHE-
- EverQuest 2
- Oddworld: Stranger's Wrath HD
- Songs for a Hero - Definitive Edition
- STAR WARS Knights of the Old Republic II
- The Longest Journey

**NVAPI** has been enabled to the following titles:
- Alone in the Dark
- Atomic Heart
- Baldur's Gate 3
- Demonologist
- Desordre
- Doge Simulator
- Icarus
- Layers of Fear
- Portal Prelude RTX
- Rainbow Six Extraction
- Ratchet & Clank: Rift Apart
- Remnant 2
- Severed Steel
- Sherlock Holmes The Awakened
- Showgunners
- Spider-Man: Miles Morales
- Strayed Lights
- Trepang2
- Voidtrain
- Warhammer 40,000: Darktide

Nearly **three-dozen bug fixes** have made it in to Proton 8.0-4, ranging from *Overwatch 2* not being able to register gamepad inputs after an online match has started; a few fixes for Battle.NET, Ubisoft Connect, and the EA Desktop app; the *Baldur's Gate 3* launcher; *SF6* incorrectly saying a user is connected via Ethernet if they're actually using Wi-Fi; UE4 titles not working correctly on Intel GPUs; *Rainbow Six Extraction* not working properly on Deck; and *plenty* of others. Additionally, half-a-dozen regressions were fixed from Proton 8 -- controller hotplugging should now properly work, and a few fixes made it in for *Resident Evil 4* and *Have a Nice Death*.

Proton 8.0-4 now supports Steamworks SDK version 1.58. Wine-Mono was updated to [8.0.1](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-8.0.1). VKD3D-Proton was updated to [2.10](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.10), which "rolls up a ton of bug fixes, game and driver workarounds, and other improvements." DXVK was updated to [2.3](https://github.com/doitsujin/dxvk/releases/tag/v2.3). DXVK-NVAPI was updated to [0.6.4](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6.4) -- this release adds HDR support and fixes a crash with *Call of Duty: Ghosts*. Finally, the VKD3D shader compiler was updated "to include recent upstream improvements."

See the full patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog#80-4).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
