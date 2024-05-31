+++
title = "WinesapOS 3.3.0 Adds Support for the Steam Deck, Enables Vulkan GFX Pipeline Library by Default"
date = 2023-07-17T13:38:51Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/3.3.0.jpg"
tags = ["news", "distro update", "software update", "winesapos"]
keywords = ["winesapos", "winesapos 3.3.0", "appimagepool", "mac linux gaming stick"]
description = "Plus an upgrade to kernel 6.1, and the ability to install AppImages via AppImagePool!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Five months after the previous update, the excellent [winesapOS](https://linuxgamingcentral.com/tags/winesapos/) gets a major upgrade. Codenamed "The Major Upgrade Update," winesapOS 3.3.0 comes with improved hardware support for the Steam Deck (including sound support), Steam Machines, Framework laptops, and Microsoft Surface laptops. If you previously used Mac Linux Gaming Stick 2 (what the project was called prior to version 3), you can now upgrade to version 3 with just a few commands from the terminal. Quite a few more file systems are now supported, AppImages can be installed via the [AppImagePool](https://github.com/prateekmedia/appimagepool) package manager, and the kernel has been upgraded to 6.1.

Along with this, the distro now resorts to using upstream Arch packages rather than the outdated SteamOS packages, providing a more stable experience for the user; and the Vulkan graphics pipeline library is now enabled by default -- which, according to the patch notes, "will lead to little to no stuttering in most games that do not already have shader cache." A few fixes related to corrupt graphics or graphical applications failing to launch have made it in as well.

Note that, if you're using winesapOS on the Steam Deck, the built-in controls may not work. If this happens, select `Arch Linux, with Linux linux` from the boot menu to workaround this issue.

See the abbreviated patch notes on the [Releases](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.3.0) page, and the full patch notes [here](https://github.com/LukeShortCloud/winesapOS/blob/3.3.0/CHANGELOG.md). Be sure to check out the interview that I had with the project founder, [Luke Short](https://linuxgamingcentral.com/posts/interview-with-luke-short-creator-of-winesapos/). And who knows -- I might do a review of the distro soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
