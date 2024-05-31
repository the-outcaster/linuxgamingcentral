+++
title = "Massive SteamTinkerLaunch v12 'Still Alive' Update Adds Steam Deck Improvements, Initial Support for Hedge Mod Manager"
date = 2022-12-24T12:13:09-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/stl/v12/cover.jpg"
tags = ["news", "software update", "steamtinkerlaunch"]
keywords = ["steamtinkerlaunch", "sonic frontiers", "steam deck", "hedge mod manager"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
It's been well worth the three-month wait for today's SteamTinkerLaunch update. We've got *so* many new features, improvements, and bug fixes with the "Still Alive" update that is v12.0. Those of you who use this Swiss army knife utility on Steam Deck, and those of you who use [mods with *Sonic Frontiers*](https://linuxgamingcentral.com/posts/sonic-frontiers-modding-guide/), should be particularly excited about this update, as there's some goodies tossed in your way.

To start, frostworx, the original author of STL, has stepped down as maintainer. Fortunately, sonic2kk has picked up the torture stake and is continuing the work where frostworx left off. And boy, let me tell you, they've been busy. This is probably the largest changelog I've ever seen.

Here's a few highlights from the *many* new features with this release:

**Steam Deck**
- GameScope, GameMode, and MangoApp options have all been enabled in Desktop Mode
- tray icon and notifier in Desktop Mode have also been enabled
- SteamOS 3.4 support
- better visual feedback while installing with notifiers, echo statements, and more logging
- offline installation improvements, such as adding a warning before installing and overwriting older install files if the local files are newer
- quality-of-life improvements; improved language file loading process, and a Quiet mode to disable notifications during install

![STL tray icon](/images/stl/v12/open_issue.jpg)

**UI**
- "various user interface elements" have been added in bold
- "prettier" game name in main menu, quotes removed from some text elements
- last played time displayed in hours, minutes, and seconds; only show this if the game was played with STL before
- scrollbar "slightly thinner" on Deck, Deck compatibility rating added to main menu and wait requester
- program version added to wait requester
- "Open Issue" option added to tray icon menu -- this will open up the Issue tracker on the STL GitHub, where you can add a support ticket

**CLI**
- `steamtinkerlaunch steamdeckcompat <appid>` gets a game's Deck compatibility rating
- `openissue`, `-v` (or `--version`), and `-h` functions added (`-h` shows help screen, `-v` shows STL version)
- "prettier" output for various commands

![STL various CLI commands](/images/stl/v12/cli.png)

**One-Time Run**
- buttons have been added for Winecfg and Winetricks for a one-time run
- the custom executable directory can be set as the working directory; the custom working directory can also be used to run an executable

**ReShade**
- per-game ReShade override versions, and the global version of ReShade can automatically be bumped

**ModOrganizer2**
- "major overhaul" of MO2 implementation
- *Valheim* added to games list
- "prettier" output of `mo2 list-installed` and `mo2 list-supported`

**Vortex Mod Manager**
- quite a number of titles -- from *Dragon Quest XI S*, to *Horizon Zero Dawn*, to *Elden Ring*, among many others -- have been added "in an attempt to improve autodetection when selecting these games for managing"
- "prettier" (yes, I know I'm using that word a lot) output for various commands

**Hedge Mod Manager**
- initial support -- [HMM](https://github.com/thesupersonic16/HedgeModManager) is an open-source mod manager for games that use the Hedgehog Engine, such as *Sonic Generations* and *Sonic Frontiers*
- automatically installs all the Winetricks tools needed for HMM to run -- this would include `dotnet48`, `d3dx9`, `vcrun2019`, and `d3dcompiler_47`
- both the latest stable and nightly releases are supported
- automatic link handling for GameBanana's 1-Click mod install button *should* work, but that may not be the case if you're on Deck -- instructions are provided in the patch notes
- `.desktop` file is created so you can quickly launch HMM on desktop
- "various command-line options" have been added

![HMM on Deck](/images/stl/v12/hmm.jpg)

**Fixes**
- "various Steam Deck fixes"; don't update STL on Steam run, less notifier spam, some UI elements should no longer be hidden by the scrollbar, Yad path fixed
- fix missing headers when a game is run offline
- better Proton Experimental mismatch handling
- path fixes for local installs on Linux desktop
- half-a-dozen fixes for Vortex Mod Manager
- and *plenty* of other fixes

**Other**
- STL can be kept open once a game is closed
- general Wiki improvements
- updated translations
- CheatEngine and GameConquerer support have been removed, since apparently the use of these can result in [player bans](https://github.com/sonic2kk/steamtinkerlaunch/issues/618)
- better installation of STL via [ProtonUp-Qt](https://linuxgamingcentral.com/posts/protonup-qt-2.7.7/) -- Flatpak installation bugs fixed, fix incorrect game count in STL remove dialog, and some other features

Man, quite a list huh? And those are only the highlights...

Note that if you're on Deck, make sure you're using [SteamOS 3.4](https://linuxgamingcentral.com/posts/steamos-3.4-stable/) or later in order to use [ModOrganizer2](https://www.modorganizer.org/). This update has shipped to the stable branch a few days ago, so everyone should have it by now.

See the full patch notes on [GitHub](https://github.com/sonic2kk/steamtinkerlaunch/releases/tag/v12.0). I will likely have an updated video guide on how to get mods to work with *Sonic Frontiers* on Deck sometime next week with this new release, so stay tuned for that!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
