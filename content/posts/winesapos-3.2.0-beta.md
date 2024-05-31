+++
title = "WinesapOS 3.2.0 (Beta) Adds Support for VMware Virtualization, Provides More Stable Mesa Drivers"
date = 2022-10-23T13:55:36-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/cover2.jpg"
tags = ["news", "software update", "distro update", "winesapos"]
keywords = ["winesapos", "steam deck", "vmware", "mesa", "bauh", "pamac", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[WinesapOS](https://linuxgamingcentral.com/posts/winesapos-3.1.1-released/) -- the brilliant Arch-based gaming distro created by Luke Short -- has evolved from 3.2.0 alpha to beta. Noteworthy updates in this release include:
- support for VMware Fusion/Workstation
- bauh replaces Pamac -- this is evidently more stable
- now built against "the latest Arch Linux" rather than targeting the outdated SteamOS 3's packages -- provides a more stable graphics library
- progress bar is now shown on initial setup rather than using terminal
- minimum requirements to run the distro have been lowered -- you can run it on a single CPU core and 2 GB RAM!

Bear in mind there are a couple of known issues:
- Steam Deck client shows corrupt graphics -- use "Steam Desktop" instead
- Steam Deck client can't login -- check the [guide](https://ps4linux.com/steam-deck-ui-ps4-linux/) on PS4Linux for troubleshooting tips

This release hasn't incorporated audio support for the Deck. However, provided everything goes according to plan, the [patch](https://lore.kernel.org/all/20220818010059.403776-1-cristian.ciocaltea@collabora.com/) for it should be merged into kernel 6.1.

See the patch notes on [GitHub](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.2.0-beta.0).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
