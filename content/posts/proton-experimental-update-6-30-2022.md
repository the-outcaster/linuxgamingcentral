+++
title = "Proton Experimental Update Adds Several Fixes to Launchers and Adds Network Video Support for a Few Titles"
date = 2022-06-30T15:38:18-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton_experimental/6_30_2022.avif"
tags = ["news", "software update", "proton experimental"]
keywords = ["proton", "proton experimental", "steam play", "chrono trigger", "ffxiv", "elite dangerous", "black ops", "azur lane", "persona 4", "the good life", "vrchat"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The same day the first batch of Q3 emails for the Steam Deck go out also happens to be the day we get an update to Proton Experimental, just a little over a week after the previous one. This update mostly focuses on bug fixes, ranging from the following:
- the launcher for *Final Fantasy XIV* should no longer close if there isn't enough space to download an update
- *Elite Dangerous* and other launchers should no longer exert strange behavior when using cloned displays
- *Call of Duty: Black Ops II Zombies* and *Multiplayer* should remain playable after connecting online
- *Azur Lane: Crosswave* should no longer hang on a black screen
- *Chrono Trigger* should no longer suffer from random crashing during cutscenes

In addition to these bug fixes, we also have improved video playback for *Persona 4 Golden*. There's two new features that have been added:
- implement Vulkan other process rendering (used by nw.js games)
- implement network video support for *The Good Life* and *VRChat*

Don't really know what the former does but I'm sure it's good news for any game that uses nw.js.

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog). Changes in bold are the ones that have been added in the latest update.

*Cover image credit: The Gamer*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
