+++
title = "Steam Deck Client Beta Fixes Reboot Loop When Updating Broken Steam Install, Adds Controller Settings for Non-Steam Games"
date = 2023-01-07T03:58:54Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/beta_1-05-2022.jpeg"
tags = ["news", "software update", "steam deck", "steam deck client update", "beta"]
keywords = ["steam deck", "steam deck client update", "steam input", "new big picture mode", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
New Deck client is out for Beta and Preview users. This fixes the reboot loop that could occur when failing to update a broken Steam install (could this perhaps fix the ["brick" situation](https://linuxgamingcentral.com/posts/your-deck-could-be-a-walking-brick-without-internet/) that I had described last weekend?). The New Big Picture Mode got some improvements as well -- Steam controller dongle pairing is now possible, and controllers can be turned off when exiting BPM.

As far as Steam Input, the [ThrustMaster eSwap PRO Xbox controller](https://www.thrustmaster.com/products/eswap-s-pro-controller/) has been added, and the long delay when connecting Razer keyboards should no longer be present. Non-Steam games should now have controller settings in the app properties.

Some other fixes have made it in as well. Full patch notes are as follows:

**General**
- Fixed reboot loop when failing to update a broken Steam install
- Changed selected launch option reminder to show three times per user instead of continuing to show every time the user returns to the game details.
- Fixed issues w/ digital navigation getting stuck on text boxes when using a physical keyboard

**New Big Picture Mode**
- Fixed issue viewing the hardware survey web page after submitting results
- Added option to turn off controllers when exiting BPM
- Implemented Steam Controller dongle pairing
- Added controller setting dropdown for controller idle turn off timeout
- Prevented launch option reminder from appearing on top of other UI while a game is launching
- UI Digital Navigation Key Repeats are faster

**Steam Input**
- Added support for the ThrustMaster eSwap PRO Controller Xbox
- Fixed long delay at startup when Razer keyboards are connected
- Show controller settings in app properties game for non-Steam games
- Fixed crash with games that use "Windows Gaming Input"
- Gyro Calibration Rework: Calibration Calculates an anti-drift value as normal, but also records Gyro and Accelerometer noise while stationary, so that Auto Calibration (toggle) is more discerning

**Linux**
- Fix instances of Steam freezing or crashing in desktop mode.
- Fix closing non-steam shortcuts via the overlay when two or more are running.

Patch notes can also be read on [Steam](https://steamcommunity.com/games/1675200/announcements/detail/3646258449571615798).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
