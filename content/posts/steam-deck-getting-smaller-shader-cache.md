+++
title = "Steam Deck Shader Cache Sizes to be Cut in Half"
date = 2023-04-13T18:21:43Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/mesa/vk_pipeline_cache.webp"
tags = ["news", "steam deck"]
keywords = ["steam deck shader cache", "mesa 23.1"]
description = "Space savings of up to 60%!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As if [faster shader compilation](https://linuxgamingcentral.com/posts/shader-compilation-improved-with-mesa-23.1/) wasn't good enough, there's another exciting update to look forward to with Mesa 23.1: shader cache size being reduced by up to 60%.

See the [merge request](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/22030) for more details. This MR reworks the Vulkan pipeline cache for RADV, and as a result, this supposedly means smaller shader cache sizes for your games. Certainly a welcome change, particularly for those on Steam Deck with sparse storage and limited time available for keeping the device online for downloading shader updates.

Pierre-Loup Griffais confirmed to [PCGamer](https://www.pcgamer.com/valve-is-about-to-slash-the-file-sizes-of-the-steam-decks-ssd-hogging-shader-caches-in-half/) that not all games may necessarily get 60% space savings, due to "the size of transcoded video depots" not being changed at all.

I have a hunch this Mesa 23.1 update will come to Deck users with the upcoming [SteamOS 3.5 update](https://linuxgamingcentral.com/posts/updated-kernel-and-smt-disabled-with-steamos-3.5/), which will also have a much-needed kernel upgrade and a feature to disable SMT. If I were to take a guess, this update will arrive sometime mid-May to early summer. The reduced shader cache size should also benefit Linux desktop users who are using RADV.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
