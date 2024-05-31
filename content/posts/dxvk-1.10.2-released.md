+++
title = "DXVK 1.10.2 Released, Adds Workaround for Plants Vs. Zombies Garden Warfare with AMD GPUs and Fixes Particle Effects for Sonic Adventure 2"
date = 2022-07-13T09:39:30-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/dxvk/1.10.2.jpg"
tags = ["news", "software update", "dxvk"]
keywords = ["dxvk", "proton", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Just a few minutes ago doitsujin from GitHub released a new version of DXVK, 1.10.2. It's been a few months since the previous 1.10.1 release. 1.10.2 mostly focuses on bug fixes and adds workarounds for a few specific titles. For example, *Star Wars: The Old Republic* has had rendering issues fixed. *Limbo* now has a 60 FPS limit as a workaround for a few bugs. All of this and some other more generic fixes that I couldn't even attempt to translate into basic English if I tried. Full patch notes are as follows:
```
- Implemented non-seamless cube maps for D3D9 using the VK_EXT_non_seamless_cube_map extension if supported by the driver
- Fixed an issue with current versions of the Nvidia Vulkan developer driver not using its on-disk shader cache with DXVK
- Fixed an issue which would cause the state cache file to not be written properly
- Fixed an issue where incorrect barriers would be emitted for UAV rendering (PR #2696)
- Fixed an issue where the d3d11.samplerAnisotropy option would apply to the wrong kind of samplers
- Fixed potential issues when using state caches that were created on a driver with a different feature set
- Fixed broken stencil resolves in D3D9
- Fixed build issues on GCC 12.1
- Optimized UAV clears in D3D11 to allow drivers to use image compression more frequently
- Optimized performance of in-memory compression for SPIR-V shader code

Game-specific:
- Beyond Good and Evil: Work around missing light shafts (#2680)
- Day Z: Enabled d3d11.cachedDynamicResources option to work around performance issues (PR #2709)
- Dead Space: Fixed shadow rendering and added 60 FPS lock to work around game bugs (#2704)
- Dirt Rally: Fixed potential GPU hang due to game bugs in a shader
- Godfather: Fixed crash on systems that don't support 16x MSAA (#2590)
- Limbo: Enable 60 FPS limit to work around game bugs (PR #2566)
- Majesty 2: Work around game bugs causing issues on integrated GPUs and systems with more than 2GB of VRAM (#1542, #PR 2612)
- Myst V: Work around an issue when the word "Radeon" is not part of the device name on AMD GPUs (#2661)
- Onechanbara Z2: Chaos: Fixed particle effects and UI elements not displaying properly (#2701)
- Planetary Annihilation: TITANS: Fixed crash when creating swap chain on a NULL window (PR #2665), as well as a crash due to creating too many internal worker threads (#2670).
- Plants vs. Zombies Garden Warfare 2: Work around crash when the game detects an AMD GPU (PR #2700)
- Return of Reckoning: Work around launcher issues (#2568, PR #2579)
- Scrapland Remastered: Work around black screen issues (#2398, PR #2574)
- Small Radios Big Televisions: Work around black screen issue (PR #2646)
- Sonic Adventure 2: Fixed missing particle effects (#2672, PR #2677)
- SpellForce Platinum Edition: Fixed crash (#2710, PR #2711)
- Supreme Commander: Fixed missing particle effects (#2638, PR #2682, PR #2684)
- Star Wars: The Force Unleashed II: Fixed some particle effects not rencering correctly (PR #2584)
- Star Wars: The Old Republic: Fixed rendering issues (#2676, PR #2681)
```

Please be aware that **this is the last version of DXVK to be released before requiring new Vulkan extensions.** On NVIDIA, for example, you'll need at least driver 510.47.03 or later. On RADV, you'll need Mesa 22 or later. See this [page](https://github.com/doitsujin/dxvk/wiki/Driver-support) for more info.

See the full patch notes on [GitHub](https://github.com/doitsujin/dxvk/releases/tag/v1.10.2). Proton Experimental will likely pick up this new version of DXVK with the next update (which will probably be tomorrow), but if you don't want to wait you can download the tarball and extract the x64 DLLs to `~/.local/share/Steam/steamapps/common/Proton - Experimental/files/lib64/wine/dxvk`. It would be a good idea to make a backup of Proton Experimental (or whatever version of Proton you want to update) before you do this.

*Cover image credit: isrtv.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
