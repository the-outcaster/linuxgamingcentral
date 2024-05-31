+++
title = "SteamTinkerLaunch Version 10 Released, Adds Initial Steam Deck Support and More Gamescope Options"
date = 2022-04-29T10:21:50-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/stl/cover.jpg"
tags = ["news", "software update"]
keywords = ["steamtinkerlaunch", "stl", "frostworx"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[SteamTinkerLaunch](https://github.com/frostworx/steamtinkerlaunch) -- the massive Swiss army knife when it comes to managing your Proton-based games on Steam -- hit a new milestone with the release of [version 10](https://github.com/frostworx/steamtinkerlaunch/releases/tag/v10.0), codenamed "Bagatelle." One major feature that was added is **initial Steam Deck support**. Though the script doesn't get installed as a Flatpak, you can simply download the `steamtinkerlaunch` script from the project's GitHub and start it as deck `user`. You can actually navigate across the different options with the Deck's built-in controls. There's a couple of gotchas with this, however; check the [Wiki](https://github.com/frostworx/steamtinkerlaunch/wiki/Steam-Deck) for more details.

**More gamescope features and options have been added**. FSR can now be used in conjunction with gamescope, FSR strength is now set at a default of 2, Nearest Neighbor has been added as a filter option, and even more stuff packed in. Additionally, a new [gamescope Wiki](https://github.com/frostworx/steamtinkerlaunch/wiki/GameScope) has been added. Keep in mind that currently gamescope doesn't work with NVIDIA graphics.

There's a *bunch* of other features added, including Zink support, bug fixes, and improved translations. The full patch notes are as follows:

- added initial Steam Deck support
  - see Steam Deck Wiki for Steam Deck specific functions
  - added pretty solid, but optional steam controller controls for Steam Deck
- multiple new gamescope features and options - thanks @sonic2kk for all of them!
  - change Integer Scaling flag to reflect updated gamescope code #435
  - the default FSR strength value is now 2
  - added FSR option to Gamescope
  - added option for Nearest Neighbor filtering to Gamescope
  - added Gamescope FSR sharpness numberbox
  - added option for Steam integration with -e flag, for working around a Gamescope bug
  - brand new Gamescope wiki
- added Zink support - thanks @sonic2kk for testing
- fixed Shader Repo window glitch
- removed useless Steam Deck default window resolutions
- find renamed GE proton as compatibility tool
- get correct latest GE-Proton with two-digits
- polish translation update by @Faalagorn
- multiple improvements for Mod Organizer 2 and Vortex
  - custom STL proton removed as requirement for installing DotNet
  - several installer enhancements
  - high speed MO2 auto installation/configuration
    - DotNet is not even required for MO2 (confirmation welcome) and therefore no longer installed
    - MO2 can be optionally installed using innoextract (used when installed)
  - both Vortex and Mod Organizer 2 install and auto-configure without any configuration on the Steam Deck
-  added Side-by-Side ReShade and native support for 3D monitors (see #443)
-  added support for winesync - thanks @Moonl1ghter
-  added option for creating user-customized ENV Variables
-  comprehensive MangoHud re-implementation - thanks @sonic2kk for testing and the new wiki!
-  fixed steamwebhelper toggle (#456) - thanks @zany130 for continous testing and reporting
-  better use of absolute game exe path - helps f.e. with ReShade/Shader-Management
-  added dxvk-async support
-  added flatpak helper thanks @TheEvilSkeleton for working on flatpak support!

Interested in trying it out yourself? Check out the guide on [Boiling Steam](https://boilingsteam.com/supercharge-steam-with-steamtinkerlaunch-stl/) to see how you can install the super-handy script on your distro and the many, *many* things you can do with it!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
