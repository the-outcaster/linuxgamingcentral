+++
title = "ChimeraOS 35 Adds GNOME Desktop, Fixes for Aya Neo Air/OneXPlayer Mini, and System Update Notifications on the Steam Deck UI"
date = 2022-09-20T22:41:05-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos/logo.jpg"
tags = ["news", "distro update", "software update", "chimeraos"]
keywords = ["chimeraos", "steam deck", "gnome", "aya neo", "onexplayer", "epic games store", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
ChimeraOS 35 marks a pretty big release for the SteamOS-like distro. The biggest feature is probably the addition of a desktop environment. Previously, you were stuck in Big Picture Mode, the Steam Deck UI, or the CLI. Now, similar to SteamOS, you can use your living room console or Deck for work or other production purposes, thanks to the addition of a desktop. Unlike SteamOS 3, however, ChimeraOS makes use of **GNOME**.

To access GNOME from Steam BPM, you'll need to enter the terminal with `CTRL + ALT + F3`, then run `chimera-session desktop`. Otherwise, on the Deck UI, you can simply enter Desktop Mode in the same way as SteamOS 3 via the Steam button.

The **Aya Neo Air and OneXPlayer Mini (AMD version) got some love** in this update. Screen orientation was fixed for both devices, and the latter got a screen frequency change feature (by the way, if you need a fan driver for the OneXPlayer, check out the [script](https://linuxgamingcentral.com/posts/kernel-module-for-onexplayer-now-available/) by **Samsagax**).

Several enhancements have been made:
- download speeds and connectivity has been improved "for some WiFi modules"
- some hard drive space has been freed by removing "many previously installed packages" that the developers didn't officially support
- Steam libraries are automatically detected on internal as well as external hard drives
- basic system update notification support on the Deck UI, with "further improvements to come"
- CPU microcode has been added to boot parameters, whatever that means

And several bugs were fixed:
- Bluetooth is now automatically enabled in Steam's configuration file, meaning Steam should no longer disable Bluetooth
- progress display for game installation or uninstallation in the Chimera app should no longer become stuck at random times
- workaround has been added for applying custom banner images to Steam collection names that have non-ASCII characters
- you should now be able to properly log in to the Epic Games Store and install games
- setting the hostname and/or timezone on the Deck UI should now work
- "spurious removable media related error messages" are fixed

Unfortunately the audio patch for the Deck didn't make it in this release, but hopefully that patch should be merged with kernel 6. ChimeraOS could very well be a decent alternative to SteamOS 3 -- including having much more up-to-date software packages -- once the audio works.

See the patch notes on [GitHub](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-35-2022-09-20). Download ChimeraOS from the [official website](https://chimeraos.org/download).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
