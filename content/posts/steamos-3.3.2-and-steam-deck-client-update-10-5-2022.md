+++
title = "SteamOS 3.2.2 Brings An Improved Docking Experience, Steam Deck Client Update Allows Easy Startup Video Customization"
date = 2022-10-05T22:24:40-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "steam deck", "software update", "steam deck client update", "steamos", "steamos update"]
keywords = ["steam deck", "steamos", "steam input", "steam", "linux", "flickstick", "rdr2"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
SteamOS and the Steam Deck client have both been updated on the Stable branch. SteamOS 3.3.2 adds external display output resolution and refresh rate selection options in the Display Settings, as well as *tons* of bug fixes, ranging from the crash in *Red Dead Redemption 2*, in-game camera control issues when using a mouse, and SD card formatting failing erratically.

As for the Steam Deck client, well, there's just *way* too much to list here. You can have a look at the ["Steam Deck Client Update"](https://linuxgamingcentral.com/tags/steam-deck-client-update/) tags on my site for a list of all the changes since the last stable update, but basically, there's the following:
- homescreen performance improvements
- a toggle that allows the Deck to automatically control display resolution for external displays
- per-device controller configurations when multiple gamepads of the same type are connected
- "Slap Back" check added to FlickStick
- custom boot videos
- tons, and I mean *tons*, of fixes and improvements

Note that they changed the file path for the custom boot animations from the [previous beta update](https://linuxgamingcentral.com/posts/steam-deck-client-beta-10-3-2022/); they're now stored in `~/.steam/root/config/uioverrides/movies/`. The file still needs to be in `webm` format, but there's no need to truncate the file or modify the `library.css` file. It's automatically played in fullscreen.

See the full patch notes on [Steam](https://store.steampowered.com/news/app/1675200/view/3301726014486703380).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
