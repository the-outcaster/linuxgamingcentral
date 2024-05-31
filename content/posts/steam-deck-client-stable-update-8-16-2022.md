+++
title = "Steam Deck Client Update Adds a Better Offline Experience, Along with Keyboard Fixes (Stable)"
date = 2022-08-16T16:30:33-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "software update", "steam deck client update", "steam deck"]
keywords = ["steam deck", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The past few beta updates to the Steam Deck client have now been pushed to the **stable** branch. Notably, some fixes were added to Offline Mode, a couple of fixes to the on-screen keyboard have made it in, and the hot/cold temperature notification has temporarily been disabled "while we address issues with false postives." Patch notes are as follows:

**Offline Mode Fixes**

*We're continuing to look at making the user experience of playing games without an Internet connection a better, more intuitive experience.*
- Fixed issue where rebooting while in Steam Offline Mode would cause games to fail to launch
- Fixed the Cloud Sync error notification popping up when offline
- Disabled Steam Offline Mode button when not connected to the internet, as trying to do this currently gets Steam Deck into a bad state.
  - This change disables this button but does not in any way affect your ability to play games without an active Internet connection.

**Keyboard**
- Fixed styling for CJK keyboard glyphs so everything appears centered correctly on keys
- Fixed Recommended Layout not always showing up for the author of controller configuration
- Fixed CJK font issues in SteamOS updater when running on Steam Deck
- Fixed focus issue when tapping the show/hide password button
- Removed the gap between keys on the virtual keyboard for improved typing

**Other**
- Temporarily disabling hot / cold temperature notifications while we address issues with false positives

Patch notes can also be found on [Steam](https://store.steampowered.com/news/app/1675200/view/3401926123937490701).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
