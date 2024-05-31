+++
title = "The Steam Deck May Be Vulnerable to \"Zenbleed\" Exploit"
date = 2023-07-28T18:50:03Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/zenbleed.png"
tags = ["news", "steam deck", "vulnerability"]
keywords = ["steam deck", "zenbleed", "steam deck zenbleed", "zen 2 vulnerability"]
description = "Note that this is mostly speculation, for the time being."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Google Information Security researcher Tavis Ormandy recently discovered a vulnerability with Zen 2 processors: ["Zenbleed"](https://lock.cmpxchg8b.com/zenbleed.html). In layman's terms, this exploit can allow "the theft of protected information from the CPU, such as encryption keys and user logins," according to [Tom's Hardware](https://www.tomshardware.com/news/zenbleed-bug-allows-data-theft-from-amds-zen-2-processors-patches-released). Any Zen 2-based processor is affected: the Ryzen 3000/4000/5000 series, and AMD's EPYC data center processors. PS5, Xbox Series consoles, and the Steam Deck -- which Valve have reported [has similar performance to the Ryzen 3000 series](https://www.techradar.com/news/valve-claims-the-steam-deck-can-handle-any-game-you-throw-at-it-including-aaas) -- could also potentially be affected since they are using Zen 2 APUs, although it's not clear at this point whether that's actually the case.

Microcode has already been [submitted to the Linux kernel](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/commit/?id=0bc3126c9cfa0b8c761483215c25382f831a7c6f), so perhaps Steam Deck users will get this patch in a future SteamOS update if Valve sees to it. There is a software workaround that you can use in the meantime by installing [msr-tools, then with it set the "chicken bit" on all cores](https://lock.cmpxchg8b.com/zenbleed.html#solution), but I don't recommend this. Not only will this require unlocking the file system, but Ormandy warns that this "may have some performance cost."

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
