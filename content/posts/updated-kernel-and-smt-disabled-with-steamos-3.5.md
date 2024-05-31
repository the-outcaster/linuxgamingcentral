+++
title = "Updated Kernel and SMT Disabled Feature Coming to SteamOS 3.5"
date = 2023-02-16T03:43:01Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/powertools/powertools_settings.jpeg"
tags = ["news", "steam deck", "steamos"]
keywords = ["steamos 3.5", "steam deck smt disabled", "steam deck updated kernel", "smt"]
description = "Valve developer says there are 'performance improvements in the pipe.'"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
This post is purely coming off of a Tweet from a Valve developer, but it's worth talking about nonetheless.

Pierre-Loup Griffais mentioned [this](https://twitter.com/Plagman2/status/1626041563737645056):
> There are performance improvements in the pipe on workloads that need SMT disabled to perform well. Those are being tested now and will release as part of the updated kernel we are working on for SteamOS 3.5.

So, two things we can glean here:
1. The kernel is *finally* getting an update. Griffais didn't say what kernel the new one will be based on, but anything newer than 5.13 -- which is *over a year-and-a-half old* at this point -- is definitely a welcome addition.
2. It seems there will be a way to disable simultaneous multithreading ([SMT](https://en.wikipedia.org/wiki/Simultaneous_multithreading)), which can lead to "performance improvements." Whether this can be turned on or off on a per-game basis wasn't stated.

Basically, when SMT is disabled, the number of CPU threads available is halved. Only the even-numbered threads will be used. On the Steam Deck, this is particularly useful for [emulation](https://linuxgamingcentral.com/posts/metroid-prime-remastered-review/#emulation-tips) and older titles; it can lead to an increase in performance while also reducing power consumption.

In the meantime, while we're waiting for SteamOS 3.5, if you want to control SMT and other advanced power options on your Deck, you can make use of [PowerTools](https://linuxgamingcentral.com/posts/preserve-battery-life-on-deck-with-powertools/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
