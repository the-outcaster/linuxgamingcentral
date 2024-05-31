+++
title = "Shader Compilation on Linux Desktop/Steam Deck Is About to Get Much Better!"
date = 2023-04-10T15:06:49Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/downloading_nonsense/cover.webp"
tags = ["news", "steam deck", "shader compilation", "mesa"]
keywords = ["mesa 23.1", "shader compilation", "shader compilation improvements", "faster shader caching", "VK_EXT_graphics_pipeline_library", "radv"]
description = "Mesa 23.1 will get a new extension for better load times and less stutter."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
While [SteamOS 3.4.6](https://linuxgamingcentral.com/posts/steamos-3.4.6-stable/) upgraded Mesa to 23.1, it didn't include faster shader compilation improvements. At least, not out of the box. I've noticed it myself; shader compilation times are just as ridiculous as it was before.

But here's the good news: a [merge request](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/22362) now enables the `VK_EXT_graphics_pipeline_library` extension by default. This is thanks for Samuel Pitoiset, who's a part of Valve's Linux graphics driver team. While you previously had to set the proper environment variables, this extension will now be enabled by default with Mesa 23.1.

I won't get into too much detail regarding the MR itself, as it's a bit over my head, but basically, according to [Phoronix](https://www.phoronix.com/news/RADV-GPL-Mesa-23.1-Default), this feature "should help with game load times and stutter avoidance."

Only problem now is we're going to have to wait a while before Mesa 23.1 becomes stable -- the earliest we can expect is [May 3rd](https://docs.mesa3d.org/release-calendar.html). And who knows how long it will take after that before Valve decides to push an update out for SteamOS to include the stable release. In the meantime though, I guess you could [compile Mesa from source](https://gitlab.freedesktop.org/mesa/mesa) to get this benefit immediately, if you're feeling brave enough.

*Cover image credit: Steam Deck Gaming*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
