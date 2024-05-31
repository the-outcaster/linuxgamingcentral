+++
title = "VKD3D-Proton 2.11 Enables DXR By Default, Improves Performance in Halo Infinite by 15%"
date = 2023-11-24T16:57:01Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/codeweavers/halo.jpg"
tags = ["news", "software update", "vkd3d-proton"]
keywords = ["vkd3d-proton", "halo infinite", "radv", "steam deck", "dxr", "starfield"]
description = "Starfield also gets some small performance gains."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
VKD3D-Proton 2.11 released less than an hour ago and with it comes "a bunch of features, perf improvements and bug fixes / workarounds."

**DXR (DirectX Raytracing) is now enabled by default.** No need to supply the `VKD3D_CONFIG=dxr` launch parameter anymore. Note, however, there are certain cases where it's *not* enabled by default, such as *Hellblade: Senua's Sacrifice* on Steam Deck. Game-specific fixes that use DXR include *Battlefield V*, *Warhammer: Darktide*, and *Jurassic World Evolution 2*. Workarounds for *Witcher 3* causing broken shadows and GPU hangs when DXR was enabled have been added.

RDNA2+ and Turing+ GPUs have the DX Ultimate feature set exposed. **FSR 3 can now be used with supported games** thanks to the implementation of the missing MSAD instruction in DXIL.

In the performance department, it has been noted that *Halo Infinite* on RADV has "15% FPS gains" due to the **improved performance** of NV_device_generated_commands and NV_device_generated_commands_compute "by reordering and batching command preprocessing." *Starfield* is also seeing some minor performance gains, by 1-2%. Note, however, that these performance gains will need "pending Mesa work to land" in order for users to receive this benefit. CPU overhead on NVIDIA has been 'greatly reduced.'

Workarounds have been added to the following titles, whether it was a GPU hang, broken shadows, or random crashes:
- *Resident Evil 4: Separate Ways* DLC
- *Lords of the Fallen*
- *Witcher 3*
- *Cyberpunk 2077*
- *Windjammers 2*

See the full patch notes on [GitHub](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.11).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
