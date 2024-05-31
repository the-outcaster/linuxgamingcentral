+++
title = "Kernel 6.3 Brings Native Steam Deck Controller Support, Better Power Efficiency with Ryzen Laptops"
date = 2023-04-24T02:03:23Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/8bitdo/pro2_on_deck.jpg"
tags = ["news", "software update", "kernel"]
keywords = ["kernel 6.3", "linux 6.3", "native steam deck controller support", "ryzen 7000", "intel meteor lake", "ext4", "btrfs", "logitech g923", "8bitdo pro 2"]
description = "Native Steam Deck controller support, support for the 8BitDo Pro 2, Logitech G923, and plenty more!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Kernel 6.3 has launched as stable today. An eighth release candidate was not needed this time around; Linus noted that it was ["a calm release"](https://lore.kernel.org/lkml/CAHk-=wg02PoScxDO0wwD5EkFpx50DF1c2TxXqyAnzGjdFf71jw@mail.gmail.com/). We've got plenty of great stuff with this release, including:
- "slightly better" Zen 4 performance with the Ryzen 7000 series via AMD's automatic IBRS feature
- better battery efficiency with Ryzen laptops
- further Intel Meteor Lake support; display support now works
- Ext4 direct I/O and Btrfs performance/optimization improvements
- [native Steam Deck controller interface support](https://www.phoronix.com/news/Steam-HID-Steam-Deck-Linux-6.3)
- support for the Logitech G923 racing wheel
- [support for the 8BitDo Pro 2 wired controller](https://linuxgamingcentral.com/posts/8bitdo-pro-2-support-coming-to-kernel-6.3/)
- further Rust implementation; the first Rust drivers will be "debuting in the near future"
- new ARM/RISC-V power management drivers
- and many, *many* more features/improvements/fixes

See the [feature overview from Phoronix](https://www.phoronix.com/review/linux-63-features) for a more complete overview.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
