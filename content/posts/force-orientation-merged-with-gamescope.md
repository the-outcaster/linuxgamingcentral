+++
title = "You Can Now Force Screen Orientation with GameScope (Useful for OneXPlayer and Aya Neo)"
date = 2022-10-07T16:04:20-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos_interview/chimeraos_on_ayaneo.jpeg"
tags = ["news", "gamescope", "aya neo", "onexplayer"]
keywords = ["gamescope", "--force-orientation", "chimeraos", "aya neo", "onexplayer"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Thanks to the [ChimeraOS team](https://linuxgamingcentral.com/posts/chimeraos-35/), a new feature has recently been merged into [GameScope](https://github.com/Plagman/gamescope): the `--force-orientation` option. Basically, what this allows users to do is to force the screen orientation via the command line when they're using GameScope. A common problem that PC handhelds face -- albeit for the Deck -- is that the screen is in portrait mode rather than in landscape. With this merge, this problem can now be fixed with:

`gamescope --force-orientation left`

As this commit is fresh out of the oven from just a few hours ago, you'll need to [compile GameScope from source](https://github.com/Plagman/gamescope#building) in order to take advantage of this (of course, if you're on Arch, you can also install the [gamescope-git](https://aur.archlinux.org/packages/gamescope-git) AUR package). Matthew Anderson, AKA ruineka, is currently working on a [pull request](https://github.com/Plagman/gamescope/pull/640) to enhance this feature even further by automatically rotating the screen, without having to enter the command. Note that GPD devices may not be supported at this time.

See the [commit](https://github.com/Plagman/gamescope/commit/647e1d96d0c2e8ab3f36704e5345d0604c9830aa) for more details.

*Cover image credit: ChimeraOS team*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
