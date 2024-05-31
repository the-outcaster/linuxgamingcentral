+++
title = "Kernel 6.1 Released, Implements Rust Foundation, Significantly Faster Btrfs, Improved Third-Party Nintendo Gamepad Support"
date = 2022-12-11T22:21:42-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/kernel/6.1.webp"
tags = ["news", "software update", "kernel"]
keywords = ["linux kernel", "linux 6.1", "kernel 6.1"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After a week of being held back due to so many changes coming in, kernel 6.1 has now officially [become stable](https://lore.kernel.org/lkml/CAHk-=wj_HcgFZNyZHTLJ7qC2613zphKDtLh6ndciwopZRfH0aQ@mail.gmail.com/T/#u) and is the next LTS release. It's quite an exciting release! First of all, we have better support for knockoff Nintendo controllers. Second, Rust has finally made its way in, although we're not really going to see anything significant as only the infrastructure has been re-written so far. Kernel 6.2 will gradually see more Rust code implemented. One step at a time. Third, both ext4 and Btrfs got performance improvements, especially with the latter. But there's so much more.

Here's some of the highlights:
- initial Rust infrastructure (no drivers or kernel subsystem abstractions are currently using it)
- support for more ARM devices, including Sony Xperia 1 IV, Samsung Galaxy E5/E7/Grand Max, and PinePhone Pro
- a few fixes for AMD Rembrandt laptops
- more Intel Meteor Lake support
- various improvements to Intel Arc graphics and firmware handling
- proper mesh shader support for the RADV Vulkan driver
- physical CD-ROM support on RISC-V systems
- Ext4 bug fixes and performance improvements
- *huge* Btrfs performance improvements (supposedly it's [twice as fast](https://www.phoronix.com/news/Btrfs-Async-Buffered-Writes-6.1))
- enables HID++ for all Logitech Bluetooth devices, as well as the auto-detection of high resolution scrolling support
- initial groundwork for Wi-Fi 7 support (802.11be)
- PinePhone/PinePhone Pro keyboard case driver input support
- laptop improvements "by making AMD PCs smarter, quieter, [and more] power efficient by adapting to user behavior and environment."
- Intel Meteor Lake Thunderbolt support
- better support for third-party Nintendo controllers (ensure "sane" calibration values)
- and much, *much* more

Big thanks to [Phoronix](https://www.phoronix.com/search/Linux+6.1) to reporting on all of the changes going on with kernel 6.1. You can see their [overview](https://www.phoronix.com/review/linux-61-features) of what's new with this kernel to see more changes.

[Kernel 6.2](https://www.phoronix.com/news/Linux-6.2-Early-Features) is going to be an even more interesting release, with fully supported ARC graphics, 4K support for Raspberry Pi, more Rust code, official DS4 support, and *tons* of more features. We should be expecting that sometime in February-March.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
