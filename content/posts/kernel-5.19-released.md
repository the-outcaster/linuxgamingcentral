+++
title = "Kernel 5.19 Released, Adds NVMe Support for M1 Chips and Further Support to Intel's Discrete GPU"
date = 2022-07-31T21:17:52-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/kernel/5.19.jpg"
tags = ["news", "kernel update"]
keywords = ["linux kernel", "dg2", "alchemist", "intel", "amd"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Kernel 5.19 released as stable just a few hours ago. Notable features include further Zen 4 APU support, further support for the Intel DG2/Alchemist GPU, idle driver support for Alder Lake processors, initial support for Raptor Lake P processors, Apple M1 NVMe controller support, and *tons* of other features/bug fixes/performance improvements. There's also supposedly performance improvements for the [HP Dev One](https://www.phoronix.com/review/hp-devone-kernels). Linus himself [wrote](https://lore.kernel.org/lkml/CAHk-=wgrz5BBk=rCz7W28Fj_o02s0Xi0OEQ3H1uQgOdFvHgx0w@mail.gmail.com/T/#u) regarding the ARM support for MacBooks:

> The most interesting part here is that I did the release (and am writing this) on an arm64 laptop. It's something I've been waiting for for a _loong_ time, and it's finally reality, thanks to the Asahi team. We've had arm64 hardware around running Linux for a long time, but none of it has really been usable as a development platform until now.

Check the three-page-long [article from Phoronix](https://www.phoronix.com/review/linux-519-features) to see the rest of the changes made. Hopefully Arch will pick this update up in the next few days.

*Cover image credit: taringa.net*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
