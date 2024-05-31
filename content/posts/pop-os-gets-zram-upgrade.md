+++
title = "Pop!_OS Enables ZRAM, Increasing Available RAM and Improving Game Performance"
date = 2023-01-11T02:54:27Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/pop_os/22_04/updates.jpg"
tags = ["news", "pop!_os", "system76", "ubuntu"]
keywords = ["zram on pop!_os", "zram", "system76", "pop!_os"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
System76's Pop!_OS distribution now enables [ZRAM](https://en.wikipedia.org/wiki/Zram). This is thanks to Pop!_OS developer [Michael Murphy](https://github.com/mmstick). Per the [Tweet](https://twitter.com/pop_os_official/status/1612591582330621952) from the official Pop!_OS account, this will increase "the amount of free memory your system has available." Supposedly this adds "increased FPS in games, or faster simulations and compiler runs," especially on systems with a low amount of RAM. Someone on the [pull request](https://github.com/pop-os/default-settings/pull/163) commented that on a PC with 8 GB RAM, the result of ZRAM enablement was "a solid boost from sometimes 80 FPS to 120 FPS (my refresh rate) and other times from 80 FPS to 90 FPS."

Another commenter noted this:
> I tested on RAM configurations between 4GB and 64GB...the most extreme case of this making a difference was a 10-year-old ThinkPad with 8GB of RAM. I was able to play *Control* for a while at around 30 FPS. It did still crash, but it was working for a bit. Without this PR it showed around 11 FPS as it loaded the menu and then crashed.

You can see more details from the [pull request](https://github.com/pop-os/default-settings/pull/163), which has now been merged with Pop!_OS.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
