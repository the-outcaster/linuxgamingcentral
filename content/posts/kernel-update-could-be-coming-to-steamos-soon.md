+++
title = "SteamOS: Kernel Update Could Be Coming Soon"
date = 2022-08-10T22:19:58-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steamos/cover.jpg"
tags = ["news", "steam deck", "steamos"]
keywords = ["steam deck", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Seems like the voices of [outdated packages on SteamOS](https://linuxgamingcentral.com/posts/the-growing-security-risk-with-steamos/) have finally been reaching Valve's ears. Firefox was [replaced with the Flatpak version](https://linuxgamingcentral.com/posts/steamos-3.4-update/) a few weeks ago, and now, my acquaintence Luke Short -- the creator of [WinesapOS](https://linuxgamingcentral.com/posts/winesapos-3.1.1-released/) -- noticed that Valve has been at work rebasing their Neptune kernel from the current 5.13 to [5.19](https://linuxgamingcentral.com/posts/kernel-5.19-released/). On Twitter he [mentions](https://twitter.com/LukeShortCloud/status/1557418098424102912):

> #Valve #SteamOS #SteamDeck is currently working on rebasing their #Linux kernel from 5.13 to 5.19. They were even testing 5.17 at one point. I discovered this last night while I was updating my linux-steamos and mesa-steamos packages on the #AUR. 👀

And indeed that appears to be the case if we look at Valve's [Arch Linux mirror](https://steamdeck-packages.steamos.cloud/archlinux-mirror/jupiter-main/os/x86_64/). Looks like Valve was working on adding `linux-neptune-519-wip-5.19.0.valve1.wip-2-x86_64` as of a few weeks ago, on July 21. 

![kernel 5.19 coming to SteamOS soon?](/images/steamos/kernel_update.jpg)

If this is anything to go by, perhaps we could be seeing kernel 5.19 in SteamOS "soon(TM)." I'm wrapping that word in quotes and adding a trademark, because, you know, Valve time. At least we know now it's a matter of *when* rather than *if*. It doesn't seem like glibc, Plasma, or Mesa has been updated yet, but it's good to know Valve is at least taking baby steps towards improving the security of the device.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
