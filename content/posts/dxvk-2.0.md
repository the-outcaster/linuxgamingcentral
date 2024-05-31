+++
title = "DXVK 2.0 Brings Memory Management Improvements, Reduces CPU Overhead and Shader Compilation Times"
date = 2022-11-10T09:32:16-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/dxvk/2.0.jpg"
tags = ["news", "software update", "dxvk"]
keywords = ["dxvk", "proton", "proton experimental", "steam play", "steam deck", "amd", "nvidia", "vulkan"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
DXVK (DirectX to Vulkan, a translation layer for D3D9/10/11 games, a part of the Proton toolkit) has had quite the upgrade. D3D9 games now have the following:
- memory management improvements for 32-bit games -- "up to several hundred megabytes"!
- render target feedback loops -- you shouldn't be getting "rendering artifacts" on newer AMD hardware with games like *Grand Theft Auto IV*
- alpha test improvements -- "fixes inaccuracies in various games," and games that needed the `d3d9.alphaTestWiggleRoom` option should no longer need it

As for D3D10, this new version of DXVK no longer ships the `d3d10.dll` or `d3d10_1.dll` files, since the implementation is "incomplete." However, the D3D10 API is still supported via `d3d10core.dll`.

D3D11 improvements:
- feature support for tiled resources and conservative rasterization up to tier 3, as well as rasterizer ordered views, "provided that the corresponding Vulkan fragment shader interlock features are supported." Don't ask me what any of this means
- support for `D3D11_FEATURE_SHADER_CACHE` and `D3D11_FEATURE_D3D11_OPTIONS5` feature queries
- refactored implementations of `ID3D11DeviceContext`, which "may improve compatibility to third-party libraries," while also reducing CPU overhead. *Assassin's Creed: Origins* and *God of War* will especially benefit from the reduced CPU overhead

AMD's Vulkan driver apparently doesn't support "fragment shader interlock" and is limited to feature level `12_0`. I guess NVIDIA gets the upper hand here, as this release supports feature level `12_1`.

Another nice feature is **reduced shader compilation stutter in many games**. It may even be eliminated entirely! This is because Vulkan shaders get compiled "at the time the game loads its D3D shaders, rather than at draw time." Note that your graphics driver will need `VK_EXT_graphics_pipeline_library` in order to benefit from this. On NVIDIA you'll also need driver 520.56.06 or newer. Patch notes doesn't mention what the driver requirement is for AMD.

For games that load their shaders during loading screen or in the menu, it is recommended to wait for shader compilation to finish before starting the game "to avoid stutter and low performance." The shader compiler activity can be observed with `DXVK_HUD=compiler`.

![Alan Wake](/images/dxvk/alan_wake.jpg)
*Image credit: Remedy Entertainment*

Despite how much this release contains, there's *still* more to cover! There's plenty of bug fixes and improvements:
- fixes/workarounds for *Alan Wake*, *Alice Madness Returns*, *Anomaly: Warzone Earth*, *Beyond Good and Evil*, *Dragon Age Origins*, *Empire: Total War*, *Final Fantasy XV*, *GTA IV*, *Heroes of Annihilated Empires*, *Limit King of Fighters XIII*, *MGS V: Ground Zeroes*, *SiN Episodes: Emergence*, *Sonic Generations*, *Spider-Man: Shattered Dimensions*, *The Ship*, *Warhammer Online*, *Ys Seven*
- better Linux build support and repo changes
- tons of other fixes and improvements that are over my head

Bear in mind there are a few caveats with this release:
- some games will still have a little bit of stutter, particularly *The Witcher 3* and "most Unreal Engine games," though this "should still be less severe" -- this is due to loading D3D shaders at draw time
- 32-bit games may have stutter "if the driver's on-disk shader cache is not working properly"
- on-disk shader cache will be "significantly larger" on NVIDIA -- you may need to pass `__GL_SHADER_DISK_CACHE_SKIP_CLEANUP=1` or `__GL_SHADER_DISK_CACHE_SIZE` to overcome the size limit

**NOTE: your graphics driver will need Vulkan 1.3 or newer. If you're on NVIDIA, you'll need driver 520.56.06 or newer. On AMD, you'll need Mesa 22.2 or newer.** Steam Deck users are going to have to wait a while in order to reap these benefits. See the DXVK [driver support](https://github.com/doitsujin/dxvk/wiki/Driver-support) page for more details.

I guess the **TL;DR** version of the patch notes would be as follows:
- memory management improvement to 32-bit D3D9 titles
- no rendering artifacts on D3D9 games on newer AMD hardware
- plenty of "inaccuracies" fixed for D3D9 games
- improved compatibility to third-party libraries for D3D11 titles, with reduced CPU overhead
- reduced shader compilation stutter!
- game-specific fixes and workarounds
- *tons* of other misc improvements and fixes

See the full patch notes for DXVK 2.0 on [GitHub](https://github.com/doitsujin/dxvk/releases/tag/v2.0). If you're too impatient to wait for Proton Experimental or GE-Proton to update to include this release, you can test it yourself by downloading the tarball from the Releases page. Extract the DLL files to the appropriate place, depending on where your Proton version is installed. For example, if I wanted to upgrade GE-Proton7-41, I would extract the 64-bit files to:

`~/.local/share/Steam/compatibilitytools.d/GE-Proton7-41/files/lib64/wine/dxvk/`

The 32-bit DLL files would go in `lib` rather than `lib64`. If you wanted to upgrade Proton Experimental, you would normally extract the DLL files to:

`~/.local/share/Steam/steamapps/common/Proton - Experimental/files/lib64/wine/dxvk/`

This is such an exciting release! I might just do a comparison for shader compilation times with this version and the previous 1.10.3 release.

*Cover image credit: Sega*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
