+++
title = "VKD3D-Proton 2.8 Reduces CPU Overhead, Adds Last-Minute Fixes for The Witcher 3 Next-Gen Upgrade"
date = 2022-12-15T14:28:51-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/vkd3d-proton/2.8.jpg"
tags = ["news", "software update", "vkd3d-proton"]
keywords = ["vkd3d-proton", "vkd3d", "wine", "dx12", "dxvk", "vkd3d-proton 2.8"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
VKD3D-Proton -- the layer responsible for translating DX12 calls to Vulkan, and an essential part of Proton -- version 2.8 just released, and "rolls up some significant new developments before the holidays."

First of all, 2.8 adds support for the `VK_EXT_descriptor_buffer` extension. This **"removes a ton of CPU overhead."** This will particularly benefit desktop users who are on NVIDIA, Intel, Turnip, and "other AMD driver implementations" that are not pertaining to the Steam Deck. RADV and Steam Deck already has "most of this in place." Also, we have some **slight GPU bound performance increases** "since we can also remove some shader code that was required to workaround lack of descriptor buffers."

Note that `VK_KHR_buffer_device_address` and `VK_KHR_push_descriptor` will be required in order to take advantage of the "descriptor buffers." However, these features "are widely supported already"; if you could use 2.7, you should be able to use 2.8 as well without issue.

Second, **support for host accessible images has been re-written** from scratch. This will support "more implementations and edge cases without a lot of per-application hacks and workarounds." Basically, *Guardians of the Galaxy* should run "well" on NVIDIA with this re-write.

Third, **the "swap chain" has also been re-written.** This should allow for reduced CPU overhead, as mentioned earlier, fixes a "spurious hang" in *Hitman III*, and some other features that are over my head, so I won't even bother explaining them. A note for those of you on the NVIDIA 525.x driver:
> A driver crash was observed on NVIDIA 525.x drivers when running in some PRIME configurations. For now, we disable use of present_wait on these drivers.

![Guardians of the Galaxy](/images/vkd3d-proton/gotg.jpg)
*Image credit: Eidos-Montreal/Square Enix*

Fourth, **there are fixes and workarounds for various games.** GPU hangs in *Spiderman Remastered: Miles Morales* and *Age of Empires IV* have been worked around or fixed. On RADV, a rendering bug in *Borderlands 3* was fixed regarding the gun damage. Intel Arc actually got some love in this update as well -- *RE: Village* should now boot on Arc. Minor issues in mesh shader implementation have been fixed. Resizable BAR has been re-factored: GPUs with 4 GB of VRAM or less won't use it, which can "avoid some out-of-memory situations."

Ah, that *Witcher 3* DX12 upgrade, which has been causing issues for many. Last-minute "frenzied fixes" have made it in. On RADV, all features albeit RT (ray-tracing?) should work. On NVIDIA, hairworks is known to crash, so disable it for now. Furthermore, while some RT effects work on the latter card, make sure AO is disabled, since it apparently crashes the GPU.

Some other less significant changes made it in as well. A regression for *Gears 5* that caused the game to lockup on boot has been fixed.

**TL;DR**

- reduced CPU overhead (though this is mostly for desktop users since the Deck already had this in place)
- small GPU-bound performance improvements
- *Guardians of the Galaxy* should run well on NVIDIA with the "host accessible images" re-write
- fixes and workarounds added for *Hitman III*, *Spiderman Remastered: Miles Morales*, *Age of Empires IV*, and *Borderlands 3* (gun damage rendering bug)
- *RE: Village* should now boot on Arc
- Resizable BAR is no longer used on GPUs < = 4 GB VRAM to prevent out-of-memory issues
- minor mesh shader implementation fixes
- last-minute fixes for *The Witcher 3* DX12 upgrade; should mostly work on RADV without RT. NVIDIA needs AO and hairworks disabled
- *Gears 5* lockup on boot regression fixed

See the full patch notes on [GitHub](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.8).

*Cover image credit: Insomniac Games/PlayStation*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
