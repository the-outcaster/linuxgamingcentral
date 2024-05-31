+++
title = "Steam Deck Client (Beta) Fixes 'Exiting Forever' State when Closing Games, Adds Checkbox to Set Default Choice when Launching a Game"
date = 2022-12-08T23:32:00-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/beta_12-8-2022.jpg"
tags = ["news", "steam deck", "steam deck client update", "software update", "beta"]
keywords = ["steam deck", "steam deck client update", "new big picture mode"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Today's Deck client update (beta) continues further optimization for loading times for users with big game libraries. A case has been fixed "where the UI would think that a game is running when it's not, leaving games in an 'exiting forever' state." Desktop Mode got some love as well, particularly with the New Big Picture Mode. A checkbox can now be checked off when launching a game that has a selection, making that choice the default selection. You can see the cover photo as an example of what I'm talking about. Some fixes have made it in as well, including UI scaling issues in the new BPM overlay when running games in high resolution.

[Full patch notes](https://steamcommunity.com/games/1675200/announcements/detail/3637250052869584408) are as follows:

**General**
- Further optimizations to load times for users with large game libraries
- Fixed a case where the UI would think that a game is running when it's not, leaving games in an "exiting forever' state
- Fixed a case where disconnecting a controller while navigating would not cancel repeating movements

**Desktop Mode**
- Replaced launch option dialog with new UI that includes a checkbox to remember the user's selection. Added a dropdown in game properties to change that selection after it is remembered.
- Fixed intermittent browser crash when closing Update news dialog
- Fixed a rare crash exiting New Big Picture Mode
- Use the New Big Picture Mode standalone keyboard if Steam is configured to run in new BPM (e.g. -newbigpicture was specified on the command-line)
- Fix some UI scaling issues in the New Big Picture Mode overlay when running in games in high resolution

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
