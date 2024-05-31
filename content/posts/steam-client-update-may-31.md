+++
title = "New Steam Client Update Supports More Filesystems, Plus Fixed Color Quality when Streaming to Steam Deck from a Linux Machine"
date = 2022-05-31T21:38:27-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam/SteamLogo.jpg"
tags = ["news", "software update", "steam"]
keywords = ["steam", "steam deck", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Earlier today Valve released an [update](https://store.steampowered.com/news/app/593110/view/3309595354196474313) to the stable branch of the Steam client. Included in the update is an important fix for Linux and Mac OS users: filesystems that don't support pre-allocation (FAT32 or ExFAT, for instance) should no longer fail when installing a game or a game update. For the Steam Deck, color quality has been fixed when streaming from a Linux host. A streaming connection should remain intact when Steam has been restarted.

There's a few other fixes here as well, particularly when using Remote Play. Full patch notes are as follows:

**Remote Play**
- Greatly improved desktop capture quality on Windows, now supporting variable framerates
- Fixed crash on Windows when the stream resolution is changed
- Fixed streaming connections failing after Steam has been restarted
- Fixed Remote Play Together dialogs occasionally not resizing correctly
- Fixed color quality when streaming from Linux to Steam Deck

**macOS/Linux**
- Fixed game install/update failing for Steam libraries installed on a filesystem that does not support preallocation (e.g. ExFAT, FAT32)

*Cover image credit: PCGamesN*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
