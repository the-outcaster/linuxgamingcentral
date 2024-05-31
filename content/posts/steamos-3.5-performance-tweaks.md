+++
title = "Looking To Increase Performance on the Steam Deck? There's a Script for That"
date = 2023-10-04T02:06:24Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/steamos_3.5_performance_tweaks/cover.webp"
tags = ["news", "steam deck", "steamos", "tweak"]
keywords = ["steamos 3.5", "steamos", "steam deck", "steam deck performance boost", "mglru", "watchdog timers", "kyber"]
description = "Be aware there are some caveats to running the script."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Recently I came across a [blog post](https://medium.com/@a.b.t./here-are-some-possibly-useful-tweaks-for-steamos-on-the-steam-deck-fcb6b571b577) that, supposedly, enhances the performance of the Steam Deck by running a few commands from the terminal. The post breaks down what each chunk of the script does. In essence, the script will do the following:
- **sets the CPU governor to "performance"** as opposed to the default "schedutil". According to the post the result of this switch will 'reduce many of the dreaded frame-time spikes plaguing the schedutil governor.'
- **enables MGLRU** (multi-gen least recently used). This will "dramatically improve upon the memory management of Linux."
- **disables watchdog timers.** This "can actually help the Steam Deck by not generating any interrupt requests of its own."
- **disables the memory clock.** Supposedly this helps with RPCS3
- **changes the I/O scheduler to "Kyber".** This "allows the diverse storage devices to both reach the maximum capacity of their respective throughput (i.e. read & write) speeds while at the same time still providing low enough latencies even among high I/O pressure."
- **disables the tracking of file access times.** "It will actually help in extending the lifetime of your storage devices, since it will cut-down on the wear & tear write operations cause on flash-based storage mediums."
- **disables CPU security flaw mitigations.** "Can boost the performance of SteamOS quite a bit," at the risk of exposing your Deck to potential security risks

I have personally run this script myself with the SteamOS 3.5 preview branch (albeit with the CPU security flaw mitigations still enabled) and can confirm I haven't run any issues so far during my brief testing. That being said, I haven't noticed much of a jump in performance, either.

![Xonotic benchmarks](/images/steam_deck/steamos_3.5_performance_tweaks/xonotic-1280-x-800-high-2.png)

Phoronix had recently [benchmarked](https://www.phoronix.com/review/steam-deck-steamos-tweaks) the performance differences between vanilla SteamOS 3.5 and the same OS version with the performance tweaks applied. *CS:GO*, *F1 2022*, *Hitman 3*, and *Cyberpunk 2077* barely saw a performance difference at all. On the other hand, "very CPU bound workloads not too demanding on the GPU" saw a decent difference. For example, *Unvanquished* saw an 11 FPS boost with the tweaks applied. *Xonotic* saw a 10 FPS boost.

Have a look at the [blog post](https://medium.com/@a.b.t./here-are-some-possibly-useful-tweaks-for-steamos-on-the-steam-deck-fcb6b571b577) if you want to give it a try. Be aware that you do so at your own risk. Also, applying these tweaks will likely impact the battery life.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
