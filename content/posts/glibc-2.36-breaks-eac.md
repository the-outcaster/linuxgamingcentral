+++
title = "GLIBC 2.36 Breaks EAC -- Don't Upgrade"
date = 2022-08-04T12:26:17-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/eac/eac_error.jpg"
tags = ["news", "glibc", "warning"]
keywords = ["glibc", "eac"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
glibc, or the GNU C Library, has recently been updated to [2.36](https://www.phoronix.com/news/GNU-C-Library-Glibc-2.36). While this release does contain quite a few bug fixes, it's also created others. For gamers in particular, it appears that this update has caused a [regression with games that use Easy Anti-Cheat (EAC)](https://github.com/ValveSoftware/Proton/issues/6051). That means *MultiVersus*, *Elden Ring*, *Apex Legends*, and any other game that uses EAC (depending on the version being used) will no longer work on Deck or on Linux via Proton.

If you're on Arch, *please* be careful when upgrading your system packages. Avoid upgrading glibc if you can, at least for the time being. If you already have 2.36, there are [instructions](https://github.com/ValveSoftware/Proton/issues/6051#issuecomment-1204543127) provided in the GitHub thread to downgrade the package. Fortunately Fedora hasn't picked up this update yet, and it seems like GloriousEggroll is [enjoying himself](https://twitter.com/GloriousEggroll/status/1555003985299374082) seeing Arch users suffer. Hopefully someone can figure out what is causing the regression.

*Cover image credit: Jelgnum from GitHub*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
