+++
title = "CryoUtilities Gets Massive 2.0 Update With a New Interface and More Performance Boost Options"
date = 2023-02-20T05:41:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cryoutilities/2.0/cover.webp"
tags = ["news", "software update", "cryoutilities"]
keywords = ["cryoutilities", "cryoutilities 2.0", "cryobyte33", "steam-deck-utilities"]
description = "The best performance-boosting app for the Deck just got better."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
CryoByte33 updates the already excellent [CryoUtilities](https://linuxgamingcentral.com/posts/cryoutilities/) app for the Deck with the massive 2.0 release. The app has been re-written in Go, the interface is more user-friendly, and even more optimizations can be set. Here are the highlights:
- code has been re-written in Go (super fast language by Google...the same language that powers LGC)
- UI overhaul
- CryoByte's recommended settings can easily be set with one click now, and stock Deck settings are also a click away
- swap size/swappiness can be individually set
- new options for memory; huge pages, shared memory in transparent huge pages, compaction proactiveness, huge page defragmentation, page lock unfairness
- game prefixes and shader caches can be synced between the internal SSD and MicroSD card
- game prefixes and shader caches can be removed on an individual basis (useful for freeing up space for uninstalled games that still have prefix and shaders on disk)

In addition to this, the program can be used entirely via the CLI. Useful for quickly applying settings without having to use the GUI.

![CryoUtilities CLI](/images/steam_deck/cryoutilities/2.0/cli.webp)

If none of this stuff sounds familiar to you, I highly recommend checking out CryoByte's [video](https://www.youtube.com/watch?v=C9EjXYZUqUs); he goes over everything with the new version, and explains what each setting does.

Check out the [GitHub](https://github.com/CryoByte33/steam-deck-utilities) for more info. And while you're at it, subscribe to his YouTube channel, and maybe even [support him](https://patreon.com/cryobyte33). He put a *ton* of work into this new release, after all.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
