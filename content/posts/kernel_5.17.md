+++
title = "Kernel 5.17 Released, Here's What's New (AMD P-State support for Zen 2)"
date = 2022-03-20T20:17:51-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = ""
tags = ["kernel update", "linux"]
keywords = ["linux kernel", "kernel 5.17"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Today marks the release of Linux kernel 5.17. Doesn't seem to offer much of anything in the gaming landscape, but there's hardware support for a bunch of new motherboards and processors.

Here's a basic rundown of what's new:
- support for AMD's new P-State driver for AMD Zen 2 APUs -- this is particularly good news for the Steam Deck as that is the APU it's using and P-State delivers better power efficiency.
- initial Intel Raptor Lake/Raptor Lake S/Alder Lake N support
- Intel AMX support in KVM virtualization
- the [StarFive JH7100](https://www.banana-pi.org/banana-pi-sbcs/121.html) is the very first RISC-V platform to get Linux support with this kernel
- faster boot times on AMD Fusion APUs with Hudson D4 chipsets
- lighting and fan control support for the NZXT controller
![nzxt fan controller](https://www.phoronix.net/image.php?id=2021&image=nzxt_smart_2)
*Image credit: Phoronix*
- better support for x86-based Android tablets, along with general laptop and tablet driver improvements
- support for older Tegra-based tablets
- support for privacy screens which are integrated in newer laptops
- general graphics and display driver updates
- F2FS, EXT4, BTRFS, and XFS performance improvements
- GameCube/Wii/Wii U real-time clock driver support -- allows people to run Linux on these devices
- Intel Wi-Fi driver improvements
- General network performance improvements
- A lot of other stuff

Check [Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.17-Features) for more details as to what was added to kernel 5.17.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
