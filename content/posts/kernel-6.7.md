+++
title = "Kernel 6.7 Adds Support for BcacheFS, Intel Meteor Lake Graphics"
date = 2024-01-08T09:58:05Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/emdoor/cover.webp"
tags = ["news", "software update", "kernel"]
keywords = ["linux kernel", "kernel 6.7", "linux 6.7", "intel meteor lake", "btrfs", "bcachefs", "futex2", "nouveau", "nvidia gsp"]
description = "\"6.7 is one of the largest kernel releases we've ever had.\""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Kernel 6.7 was released yesterday and with it comes initial support for the BcacheFS file system and a host of other improvements. Per Linus Torvalds in the official announcement, this is ["one of the largest kernel releases we've ever had."](https://lore.kernel.org/lkml/CAHk-=widprp4XoHUcsDe7e16YZjLYJWra-dK0hE1MnfPMf6C3Q@mail.gmail.com/T/#u) 

According to the [BcacheFS official website](https://bcachefs.org/), this is a new file system that has "an emphasis on reliability and robustness and the complete set of features one would expect from a modern filesystem." However, according to some benchmarks from [Phoronix](https://www.phoronix.com/review/bcachefs-benchmarks-linux67) a few months ago, it would appear that in most cases BcacheFS can't keep up with the likes of EXT4 and BTRFS. BcacheFS has been steadily improving since then, though, so perhaps it has a better chance of offering similar performance to other file systems.

Intel Meteor Lake graphics are now officially supported. According to Phoronix, these graphics drivers are ["in very good shape"](https://www.phoronix.com/news/Linux-6.7-Features-Today). So who knows; maybe that [Meteor Lake-powered handheld](https://linuxgamingcentral.com/posts/new-meteor-lake-pc-gaming-handheld-by-emdoor/) will have a fighting chance against AMD.

There is initial acceleration support for the RTX 40-series GPUs via NVIDIA GSP support in the Nouveau driver. This also improves the support for the 20- and 30-series cards.

Some other features with kernel 6.7:
- new Btrfs features -- which [the Steam Deck in particular will benefit from](https://www.phoronix.com/news/Linux-6.7-Btrfs-Same-FSID)
- some more work done on FUTEX2, which benefits gaming with Wine/Proton

Along with a *ton* of other fixes/improvements -- most of which don't seem to be related to gaming though. See the [full feature list](https://www.phoronix.com/review/linux-67-features) from Phoronix for more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
