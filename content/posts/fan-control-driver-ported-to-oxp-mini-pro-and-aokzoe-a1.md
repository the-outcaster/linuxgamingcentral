+++
title = "Fan Controller Driver for OneXPlayer Mini PRO and AOKZOE Now Available"
date = 2022-11-19T23:29:44-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/aokzoe/cover.jpg"
tags = ["news", "kernel driver", "onexplayer", "aokzoe", "fan control"]
keywords = ["aokzoe", "onexplayer", "onexplayer mini", "fan controller"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Leave it up to the keyboard tap dancer Joaquín Ignacio Aramendía (Samsagax) to add [fan controller functionality](https://linuxgamingcentral.com/posts/oxp-amd-sensor-driver-will-be-merged-with-kernel-6.2/) to devices outside of the OneXPlayer Mini. In addition to the Mini, the Mini PRO is now also supported. The [AOKZOE](https://linuxgamingcentral.com/posts/aokzoe/) has support as well! Both devices are powered by the Ryzen 6800U. Still no news on Intel-based devices.

The [patch](https://lore.kernel.org/linux-hwmon/20221119162347.36698-1-samsagax@gmail.com/T/#u) has been submitted for review. In the meantime, if you own either of these devices, you can compile the [driver](https://gitlab.com/Samsagax/oxp-platform-dkms) from source. Arch users have the advantage of the [AUR](https://aur.archlinux.org/packages/oxp-platform-dkms-git) package.

Also, be sure to check out the [interview](https://linuxgamingcentral.com/posts/interview-with-chimeraos-devs/) that I had with Joaquín and one of the other ChimeraOS developers!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
