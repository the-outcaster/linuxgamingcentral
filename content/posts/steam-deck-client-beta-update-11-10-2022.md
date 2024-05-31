+++
title = "Steam Deck Client Beta Adds Fixes to Downloads Page, Properly Renders Library UI in Desktop Mode While Offline"
date = 2022-11-11T14:56:19-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "steam deck", "software update", "steam deck client update", "beta"]
keywords = ["steam deck", "steam deck client", "steam deck client update"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday's Steam Deck client update (beta) has added a bunch of fixes, particularly for the Downloads page in Game Mode, the OSK, Desktop Mode, and the "New" Big Picture Mode. Patch notes are as follows:

**General**
- Fixed downloads page crashing when starting in offline mode
- Downloads page now properly responds to online/offline status
- Virtual Keyboard now has a maximum width, so that it doesn't stretch to an unusable size on large screens in Docked mode

**Desktop Mode**
- Fixed issue preventing the Virtual Keyboard from accessing the clipboard and being able to perform paste operations
- Fixed duplicate dialogs (e.g. uninstall dialog) after opening the standalone keyboard or controller configurator
- Fixed regression where Browse Local Files was no longer working
- Fixed circular download progress indicator being broken in game entry list
- Fixed issue where the library UI would not render in offline mode

**New Big Picture Mode**
- Fixed issue where custom artwork and local screenshots were not found when running with -newbigpicture
- Fixed issue where transitioning from Desktop => BPM => Desktop would cause the Friends List to be signed out
- Fixed issue where advanced display settings were not visible outside of the Steam Deck
- Fixed issue where the old Big Picture Mode was started when the checkbox in Settings => Interface specified that Big Picture Mode should be the startup UI, even though -newbigpicture was specified.
- Fixed Virtual Keyboard not working properly when brought up manually or by automatically by the game

Patch notes can also be read on [Steam](https://store.steampowered.com/news/app/1675200/view/3383920059425809022).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
