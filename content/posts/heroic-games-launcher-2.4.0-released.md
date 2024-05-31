+++
title = "Heroic Games Launcher 2.4.0 'Chopper' Released as Stable, Adds GOG Cloud Save Support and the Ability to Add Games as Non-Steam Games"
date = 2022-08-11T10:09:28-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/heroic/2.4.0/stable.jpg"
tags = ["news", "software update", "heroic games launcher"]
keywords = ["heroic games launcher", "epic games", "gog"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Quite a massive release for the popular Heroic Games Launcher today. Codenamed "Chopper," this is apparently the team's biggest release, containing over 200 commits. There's *too many* patch notes to cover, but here's some of the noteworthy changes:
- improvements to the UI, including a unified Epic/GOG library, the ability to mark games as your favorite, new sidebar design, game language selection, and the ability to see if there's a new version available if you're not using the Flatpak
- GOG cloud save support
- if a gamepad is connected, the interface will be updated to show button icons. Super handy for Steam Deck!
- Epic Overlay support, as well as EAC/BattlEye anticheat runtimes
- easier to add environmental variables with a new editable table
- games can now be added as non-Steam shortcuts
- Wine executable path can now be shown
- several bug fixes, ranging from the controller on boot setting being disabled to the setting up of GOG games with Proton and ScummVM patch
- update to Legendary (the backend for Heroic) [0.20.27](https://github.com/derrod/legendary/releases/tag/0.20.27) and Electron to [20.0.1](https://github.com/electron/electron/releases/tag/v20.0.1)
- display should no longer go to sleep during playtime
- improvements to Desktop and Menu shortcut functionality
- recently played games are now sorted by playtime

![add to steam heroic games launcher example](/images/heroic/2.4.0/add_to_steam_example.jpg)

All of this and plenty, *plenty* of more changes! See the patch notes on [GitHub](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher/releases/tag/v2.4.0) for more info. Heroic is available as a Flatpak, by the way, so you can easily make use of it on the Deck. Only side note is at the time of writing this, the Flatpak version hasn't been updated to 2.4.0 just yet.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
