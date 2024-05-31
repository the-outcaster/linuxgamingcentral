+++
title = "Kernel 6.0 Is Now Here, Adds Raptor Lake Thunderbolt Support and Initial Support for Meteor Lake"
date = 2022-10-02T23:16:03-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/intel/meteor_lake.jpg"
tags = ["news", "software update", "kernel"]
keywords = ["linux", "linux kernel"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After a couple of dozen or so of releases, the Linux kernel version moves up to the next number. In this case kernel 5.19 has now moved on to kernel 6.0. This release doesn't seem too exciting for us gamers, although there is the usual support for new hardware, such as Intel Meteor Lake processors and AMD's RDNA3 graphics. Those of you who use hardware from [Tuxedo Computers](https://linuxgamingcentral.com/posts/tuxedo-pulse-gen2-review/) may also benefit here, as keyboard/touchpad fixes have been added when the device is suspended. Here's a brief overview of the new features introduced with this kernel update:
- improved NUMA balancing for Zen. Phoronix reported "very nice" performance improvements "on big systems"
- suspend-to-idle preparations for new AMD hardware
- audio driver support for AMD Raphael/Jadeite, as well as for Intel Meteor Lake
- PCI support for OpenRISC
- Intel SGX2 support
- initial support for Meteor Lake, Ponte Vecchio, and RDNA3 graphics
- touchpad and keyboard issues fixed for many Tuxedo Computers after suspend
- Raptor Lake Thunderbolt support
- H.265/HEVC media user-space API is now stable
- plenty of other fixes and improvements

It will probably be another couple of weeks -- even on Arch -- before this kernel becomes available in your update repos. Thanks to [Phoronix](https://www.phoronix.com/review/linux-60-features) for a complete overview of what's new in kernel 6.0.

*Cover image credit: wccftech.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
