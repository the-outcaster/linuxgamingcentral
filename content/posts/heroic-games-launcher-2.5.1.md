+++
title = "Heroic Games Launcher 2.5.1 Gets Hotfix, MacOS Improvements"
date = 2022-12-06T09:59:15-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/heroic/2.5.0/download_manager.png"
tags = ["news", "software update", "heroic games launcher"]
keywords = ["heroic games launcher", "legendary", "epic games store"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Heroic Games Launcher continues to get TLC from its massive [2.5.0 update](https://linuxgamingcentral.com/posts/heroic-games-launcher-2.5.0/). The Mac version of the app definitely got some attention here -- with the inclusion of Wine, DXVK, and Winetricks support -- but the Linux version got some updates as well. It's mostly fixes. They are as follows:
- Fix the issue with the download's progress going crazy and duplicating the installation/update.
- Fix a crash on the Install dialog on some games
- Fix sideload games not being added to steam automatically.
- Fix Games failing to start when launched from Steam because they have an update
- Fix games falling to start when launched from Steam when they had Sync Saves but the path was not defined
- Fix Auto detect saves path going on forever. Now it will have a timeout of 15s.
- Fix GOG games failing to install due to not supported language error.
- Fix a crash that was happening when uninstalling Sideloaded Apps
- Fix Login Page container size max Width
- Possibly fix the state of the game card not correctly updating. Not showing an update button, for instance.
- [Linux/macOS] Fix the windows version of a game version being recognized as native and not showing Wine settings and others.
- [macOS] Fixed an issue where the game save path was not correct for native games.
- [Windows] Fix an issue where Heroic was crashing when opening the install dialog.
- Some other minor fixes and improvements.

Other changes include:
- Increased the connectivity check timeout at startup and added a button to ignore the status.
- Heroic will clean the cache now after upgrading to a new release since some issues are associated with that after updating.

The Linux version in particular got the following fix: "fix the Windows version of a game version being recognized as native and not showing Wine settings and others."

Please note that **"Heroic will clean the cache now after every update so it can start fresh, but in some cases, you might need to log in again on Epic and GOG, and on Linux or macOS start a new prefix in case the game fails to launch."**

See the full patch notes on [GitHub](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher/releases/tag/v2.5.1).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
