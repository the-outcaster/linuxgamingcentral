+++
title = "Steam Deck Client Beta Adds LAN Game Transfer, Improves BPM Performance on Desktop with NVIDIA GPUs"
date = 2023-02-17T21:45:50Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/beta_2-17-2023.webp"
tags = ["news", "steam deck", "software update", "steam deck client update", "beta"]
keywords = ["steam deck", "steam deck client", "steam deck client update", "steam deck client beta update", "steam deck beta client update", "steam local network game transfer", "steam bpm with nvidia"]
description = "Pretty big update with fixes and UI enhancements."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
New beefy update out for beta users. But keep in mind some of these patch notes are specific to the desktop client.

As had been revealed back in January, local transfer of games between your desktop and Deck [are now a reality](https://linuxgamingcentral.com/posts/steam-p2p-coming-soon/). The patch notes mention both clients must be opted into Steam Beta, and is only available between PC to Deck, or PC to PC.

Good news for those of you with NVIDIA GPUs. Seems like performance has been improved in the new Big Picture Mode. Guess you won't have to use the [old BPM](https://linuxgamingcentral.com/posts/rip-old-bpm/) anymore.

Patch notes, listed below, can also be read on [Steam](https://store.steampowered.com/news/app/1675200/view/3673285123502439065).  

**General**
- Fixed some issues where focus was lost after exiting a game
- Improved performance in Big Picture Mode when using Nvidia GPUs
- Reduced flashing in background when scrolling through games on home screen

**Local Network Game Transfers**
- Added new feature that allows Steam users to copy existing Steam game installation and update files from one PC to another over a local area network, without having to download and install from a Steam content server on the internet. This reduces internet traffic and can speed up installs or updates.
- This feature is currently only PC - PC or PC - Steam Deck, and both sender and receiver must be opted into Steam Beta.
- Steam users have control over who files can be sent to: self only, friends only, or everyone. The default setting is self only.
- More info about this new feature can be found [here](https://help.steampowered.com/en/faqs/view/46BD-6BA8-B012-CE43).

**Steam Input**
- Added a loading throbber when waiting on Steam Cloud to update 
- Improved the latency of querying the workshop in the Configuration Browser and fix issues with configurations popping-in or opening the wrong tab because results weren't fully received
- Added a loading throbber that shows while the Configuration Browser workshop query is running

**Desktop Mode: Steam**
- Added UI that temporarily takes over the What's New section of the Library when pre-purchased games are available to pre-load or install and play
- Added UI at startup for account selection
- Added a sign out option to the main menu that removes credentials for the signed in account from the machine
- Fixed a crash when the OS is notifying Steam that it should shutdown
- Improved performance of games when using Steam Workshop APIs
- Refreshed the profile games page with a new style and improved performance

**Desktop Mode: Big Picture**
- Fixed issue where the old BPM on-screen keyboard would appear at the same time as the new BPM virtual keyboard
- Fixed issue where user could not re-enter a context submenu after backing out of it.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
