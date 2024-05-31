+++
title = "D8VK 1.0 Adds Many Game-Specific Configurations, Features, and Tweaks"
date = 2023-05-10T17:05:28Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/d8vk/1.0.jpg"
tags = ["news", "software update", "d8vk"]
keywords = ["d8vk", "d8vk 1.0", "wined3d", "d3d8to9"]
description = "d3d9.dll no longer needs to be installed!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
D8VK -- the project responsible for translating Direct3D 8 titles to Vulkan -- sees a massive update with version 1.0. It's been over five months since the last release, and the patch notes mention 1.0 "is the definitive release...with the widest possible support for Direct3D 8 games and apps on Linux."

Great news with this release is that D3D9 is now statically linked with `d3d8.dll`. Meaning that you no longer need to install `d3d9.dll` for D8VK to work. "Countless game-specific configurations and minor features and tweaks" also made it in, along with a *ton* of other changes. Many bug fixes have been baked in as well, including a game-specific fix for *Red Faction*.

If you look at their benchmark chart, you'll notice D8VK is significantly faster than WineD3D and D3D8to9. For instance, the Car Chase implementation with 3DMark 2001 SE performs over 1.5 times faster than WineD3D on High settings at 553.8 FPS. It runs more than *three times* faster than D3D8to9 with DXVK 2.1.

See the full patch notes on [GitHub](https://github.com/AlpyneDreams/d8vk/releases/tag/d8vk-v1.0).

*Cover image credit: AlpyneDreams*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
