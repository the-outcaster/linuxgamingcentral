+++
title = "SteamOS Stable Update, Deck Client Beta Update, and Upgrade to Arch Base Coming Soon"
date = 2022-08-17T19:22:14-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["steam deck", "deck client update", "steamos", "steamos update"]
keywords = ["steam deck", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A little over a week ago Valve pushed an [update](https://linuxgamingcentral.com/posts/steamos-beta-update-8-8-2022/) to the Preview branch that reverted a VRAM workaround for *Red Dead Redemption 2* and fixed some issues regarding random stutter and performance drops if the performance HUD was enabled. Well, that update is now available in the **Stable** branch, starting today. There's also improved performance for *Forza Horizon 5* from a beta [update](https://linuxgamingcentral.com/posts/steam-deck-client-beta-update-8-10-2022/) that shipped a couple of days later. See the patch notes on [Steam](https://steamcommunity.com/app/1675200/eventcomments/3428948355361020929).

But that's not all. The Deck client beta has been updated at the same time. Finally, community layouts can be deleted. There's also support for Nintendo's Joy-Cons, and an "improved FlickStick mode." Some other minor bug fixes were added, including no longer showing a Steam Cloud sync error when installing a game, and game resolution can be modified with non-Steam games now. [Full patch notes](https://steamcommunity.com/app/1675200/eventcomments/3428948355360837698) are as follows:

**Steam Input**
- Allow users to remove community layouts that they've created. Users who have this config selected won't lose it, but it will no longer be listed in the community layouts.
- Removed a check which would only show your layouts in your personal layouts, even when shared with the community - this was causing users to think their configuration has not been exported.
- Fixed a bug on saving configurations where the controller type could attempt to use a cached valued which was incorrect, causing the layout controller type to appear to be incorrect.
- Changed the OSK chord to be on button release instead of press to resolve some issues with focus on the desktop window.
- Added Shared Layout preview of layouts which shows a layout and allows it to be optionally assigned. If the user clicks on a steam url link to a config (via chat for example) while in Game Mode, this will be shown.
- Added support for Nintendo Joy-Cons
- Improved FlickStick mode

**Other**
- Added Discovery Queue to Home screen under the Recommended tab
- No longer showing a Steam Cloud sync error notification when installing a game
- Fixed issue where a 2.9GB read-only library is displayed when the microSD card is unmounted manually
- Added game resolution setting to non-Steam app properties

Additionally, there's something we can look forward to: an update to the Arch base. Valve employee Pierre-Loup Griffais mentioned on [Twitter](https://twitter.com/Plagman2/status/1560015983317696514):
> We're now working on the upcoming 3.4 Beta, which will contain an update to the Arch base.

Hopefully that means SteamOS will get some much-needed upgrades to its' software base. Time will tell.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
