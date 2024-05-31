+++
title = "8BitDo Pro 2 Getting Better Support with Kernel 6.3"
date = 2023-03-06T18:58:34Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/8bitdo/pro2_on_deck.jpg"
tags = ["news", "kernel", "8bitdo"]
keywords = ["8bitdo pro 2", "linux 6.3", "kernel 6.3"]
description = "The wired gamepad is getting better support for the X-Input mode."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you go to [8BitDo's website](https://www.8bitdo.com/pro2-wired-controller/) you'll notice the Pro 2 wired gamepad is advertised as working for SteamOS 3.4/Steam Deck. While it technically does, there's a bit of a hurdle. According to [Phoronix](https://www.phoronix.com/news/Linux-6.3-8BitDo-Pro-2-Wired), users have had "problematic" issues using the X-Input mode. If they want to use this mode, they've often had to resort to xboxdrv to get it to work nicely.

Well, beginning with kernel 6.3, this workaround will no longer be required. The wired version of the gamepad will be "added to the XPad driver as an Xbox 360 compatible device type" with the "necessary vendor/product IDs." This is thanks to a [pull request](https://lore.kernel.org/lkml/Y%2Fhc1bPMmOlD+vW2@google.com/) submitted by Dmitry Torokhov, which, in part, contains the XPad driver for said gamepad. This has been approved and will be merged into 6.3.

As the first RC for kernel 6.3 just released yesterday, it will be a while before 6.3 becomes stable -- late April/early May. And since the next SteamOS update is [updating to 6.1](https://linuxgamingcentral.com/posts/updated-kernel-and-smt-disabled-with-steamos-3.5/), it will be even longer before users get proper X-Input support on Deck. Guess you'll have to keep using xboxdrv for now.

*Cover image credit: 8BitDo*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
