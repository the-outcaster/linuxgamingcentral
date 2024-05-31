+++
title = "SteamOS 3.4 Now Stable, Updates Arch Base, Allows Screen Tearing, Enables TRIM (And Much More!)"
date = 2022-12-22T09:44:35-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/steamos_updates/3.4_preview/mangohud.jpeg"
tags = ["news", "steam deck", "software update", "steamos", "stable"]
keywords = ["steam deck", "steamos", "steamos update", "steamos 3.4"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
SteamOS 3.4 has now reached the stable branch. I'm not going to re-hash what [I've already said](https://linuxgamingcentral.com/posts/steamos-3.4-preview-updates-arch-base/) about it, but as a quick refresh, here's a few of the new features:
- update to the Arch base; Plasma, Mesa, GLIBC, and more software have been updated
- [KDE Connect](https://linuxgamingcentral.com/posts/steamos-3.4-includes-kde-connect/) is now included
- tons of bug fixes, ranging from graphics driver crashes to input to audio
- new firmware for docking station
- you can now force vsync off by enabling screen tearing
- level 2 MangoHUD now goes *across* the screen rather than going down; perfect for games that use 16:9
- TRIM has been re-enabled
- eject option added for removable drives
- automatic mounting of ext4 external drives
- support for 8BitDo Ultimate wireless controller dongle

Two hotfixes were added later on to "address a regression in how SD cards were handled" and to "fix an issue with HDMI/DisplayPort audio going to sleep after being idle on external displays." And I guess [hardware encoding for remote play works now](https://github.com/ValveSoftware/SteamOS/issues/903).

CryoByte33, author of the [CryoUtilities script](https://linuxgamingcentral.com/posts/cryoutilities/), has added a friendly [reminder](https://mastodon.cryobyte.net/@cryobyte33/109556254027014903) that "you need to check that the VRAM setting persisted in BIOS and can optionally disable my TRIM-on-schedule," since TRIM has already been re-enabled with this release.

See the full patch notes on [Steam](https://steamcommunity.com/games/1675200/announcements/detail/3646258449514531839).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
