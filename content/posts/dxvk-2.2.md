+++
title = "DXVK 2.2 Introduces D3D11On12 Support, Improves Compatibility with Game Launchers and Visual Novels"
date = 2023-05-12T20:32:04Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/halo_mcc/cover.jpg"
tags = ["news", "software update", "dxvk"]
keywords = ["dxvk", "directx to vulkan", "dxvk 2.2", "d3d11on12", "d3d9", "d3d11", "d3d12", "jade empire", "sid meier's pirates", "total war shogun", "battle fantasia", "cold fear", "dawn of magic 2", "dc universe online", "far cry 2", "halo mcc", "warhammer 40k space marine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Shortly after the release of [D8VK 1.0](https://linuxgamingcentral.com/posts/d8vk-v1.0/) comes DXVK 2.2. It's a pretty hefty update that "introduces support for creating D3D11 devices from a D3D12 device," improved compatibility with game launchers and certain visual novels that use Microsoft's WPF toolkit, less redundant logging, along with plenty of bug fixes.

Keep in mind that even though there is improved game launcher compatibility, there is "a noticable performance hit." Users are encouraged to report the full Proton log when filing bug reports.

Additionally, there are in-game videos fixed with certain titles, improved performance with others, and memory leaks have been addressed:
- in-game videos for *Jade Empire* and *Sid Meier's Pirates* fixed
- *Total War: Shogun 2* no longer runs out of address space when using the D3D9 renderer
- performance issues with "recent RE engine games (D3D12)" fixed on systems with multiple GPUs
- "significantly reduced memory usage" for games that create "unused D3D11 devices"
- *Battle Fantasia Revised Edition* now capped to 60 FPs "to work around game bugs at higher frame rates"
- missing geometry fixed with *Cold Fear*
- *Dawn of Magic 2* should no longer crash on start
- Alt+Tab hang with *DC Universe Online* now fixed
- low GPU performance and rendering issues on Intel with *Far Cry 2* has been worked around
- fixed memory leak with *Halo: MCC*
- fixed shadow rendering with *Warhammer 40k: Space Marine*

Proton Experimental should add this release in soon, if it hasn't already. GE-Proton likely has this baked in already since every release updates DXVK to the "latest git."

See the patch notes on [GitHub](https://github.com/doitsujin/dxvk/releases/tag/v2.2).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
