+++
title = "New Steam Deck Client Update, SteamOS 3.2 Now Official"
date = 2022-05-27T14:30:14-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "software update", "steam deck"]
keywords = ["steam deck", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A new Steam Deck client update [rolled out](https://store.steampowered.com/news/app/1675200/view/3297210455204145216) yesterday. Steam Remote Play Together is now fully functional, and one of the keyboard themes received improved performance. A few notifications have been added. Full changelog is as follows:
```
- Remote Play Together is now completely functional on Steam Deck. Includes hosting and joining game sessions. Try out a supported game and open the Quick Access Menu to get started.
- Added notification when the Steam Deck's SSD has less than 2GB of free space left
- Improved performance of Night Shift keyboard theme
- Added the ability to name controller layout commands
- Added icons for gamepad and mouse commands shown on in-game virtual menus
- Fixed being unable to connect to hidden wireless networks
- Added time zone region for Saskatchewan
- Added ability to close a window if the running application has more than one visible
- Added ability to change accounts from the power menu
```

At the same time, SteamOS as a whole has graduated from the 3.2 beta to a stable release. This update includes an OS-controlled fan curve, adjustable refresh rate, more internal resolution options, and faster MicroSD card formatting. Here's the scope on that:
```
- Added an OS-controlled fan curve to improve the experience in low usage scenarios, and adjusting how the fan responds to different scenarios and temperatures.
  - The old version of the fan curve is still available, and can be turned on in Settings > System
- Added support for changing the in-game screen refresh rate. The refresh rate will automatically be adjusted to the desired option when going in and out of game.
  - There is a new slider in the Quick Access Menu > Performance tab that allows you to choose a screen refresh rate between 40-60Hz
  - The framerate limit slider values will update accordingly, and will include 1:1, 1:2, 1:4, or uncapped framerate options.
- Fixed an issue with typing the € key using the Steam keyboard
- Performance HUD now shows a more accurate reading of VRAM used (previously would cap out at 1G used)
- Added more internal screen resolution options for games to choose from
- Fixed gain staging, resulting in higher max speaker volume, and removes white noise coming through 3.5mm jack with some headphones.
- Fixed PipeWire and Steam failing to elevate their thread priorities
- Fixed the language dropdown in the Warframe launcher
- microSD card formatting process now performs a quick format
```

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
