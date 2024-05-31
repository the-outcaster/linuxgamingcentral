+++
title = "Kernel 6.2 Adds Official DualShock 4 Support, Stable Intel Arc GPU Graphics"
date = 2023-02-20T03:40:39Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/playstation/ds4.jpg"
tags = ["news", "software update", "kernel"]
keywords = ["linux kernel", "kernel 6.2", "ds4 support on linux", "intel arc", "rtx 30 series", "onexplayer", "risc-v", "raspberry pi", "rust language"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Kernel 6.2, released just a few hours ago, is quite a feature-packed release. As fast as Btrfs speeds got with [6.1](https://linuxgamingcentral.com/posts/kernel-6.1-released/), the file system is even *faster* with 6.2, and it's also been improved as far as reliability, apparently. Raspberry Pi gets 4K display support at 60 Hz, Intel's DG2/Alchemist GPUs are now declared "stable," DS4 pads have official driver support, and plenty of other goodies with this release.

There's too many changes to list, but here are some highlights:
- Arc GPU graphics are now stable; they're no longer behind a module flag
- initial RTX 30 series support in Nouveau, but unsurprisingly [performance is terrible](https://www.phoronix.com/review/linux-62-rtx30) (good thing we have [NVK](https://linuxgamingcentral.com/posts/nvk-making-progress/) in the works)
- [official DualShock 4 support](https://linuxgamingcentral.com/posts/ds4-support-added-to-hid-playstation/) (uses official driver rather than the community-maintained one)
- [OneXPlayer sensor and fan driver support](https://linuxgamingcentral.com/posts/fan-control-driver-ported-to-oxp-mini-pro-and-aokzoe-a1/)
- RISC-V: support for persistent memory devices
- power savings for Intel Alder Lake N and Raptor Lake P CPUs
- 4K/60 Hz support for Raspberry Pi
- Btrfs: performance *and* reliability improvements
- Ext4: clean-ups and bug fixes
- exFAT: faster file/directory creation
- USB4 wake-on-connect/disconnect support
- faster Zstd kernel implementation
- power-saving improvements for idle or lightly loaded systems 
- further Rust implementation, but drivers still aren't using it yet

Check Phoronix's [feature list](https://www.phoronix.com/review/linux-62-features) to get a more complete overview!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
