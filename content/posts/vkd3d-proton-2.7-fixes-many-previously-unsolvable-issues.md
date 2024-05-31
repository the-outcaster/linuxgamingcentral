+++
title = "VKD3D-Proton 2.7 'Fixes Many Previously Unsolvable Issues,' Improves GPU Performance"
date = 2022-10-27T11:40:40-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/vkd3d-proton/f1_2022.jpg"
tags = ["news", "software update", "vkd3d-proton"]
keywords = ["proton", "proton experimental", "ge-proton", "proton-ge", "vkd3d", "vkd3d-proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
An exciting new update has landed for [vkd3d-proton](https://github.com/HansKristian-Work/vkd3d-proton). For those who aren't aware, vkd3d-proton is a part of what makes up Proton, and "aims to implement the full Direct3D API on top of Vulkan." It probably won't be long before Proton Experimental or GE-Proton picks up this update. When it does, we will be seeing *lots* of benefits.

So first off, we have an **improved pipeline cache**. This release incorporates an "internal 'magic' disk cache to enable SPIR-V caching for *all* games." The `VK_EXT_shader_module_identifier` extension will apparently reduce the on-disk footprint cache by 95%. This helps when the cache needs to be regenerated.

Some **optimizations** have been made, mostly in the GPU department. GPU performance has been improved in regards to depth render passes, certain floating-point images where UAV usage was enabled, certain use cases of WriteBufferImmediate(), certain access patterns of root descriptors, back-to-back buffer-image copies, and when allocating large zero-cleared resources and heaps. I honestly don't know what any of that means, but I guess the translation is improved GPU performance in a lot of areas. "Misc things here and there" have been added to reduce overhead.

**D3D12 got a couple of new features**: mesh shaders, advanced ExecuteIndirect, DirectX Raytracing (DXR) [1.1](https://devblogs.microsoft.com/directx/dxr-1-1/), shared resources, SV_Barycentrics, and preliminary HDR support. Advanced ExecuteIndirect uses `VK_NV_device_generated_commands`, which will allow [*Halo Infinite*](https://linuxgamingcentral.com/posts/halo-infinite-on-deck-guide/) to run on RADV and NVIDIA systems (although this game has already been playable for a while now). With some missing features now added to DXR 1.1, *Cyperpunk 2077* DXR should work. Keep in mind you'll need to use the `VKD3D_CONFIG=dxr11` launch parameter in order to make use of DXR 1.1 for now.

![Guardians of the Galaxy](/images/vkd3d-proton/gotg.jpg)
*Image credit: Eidos-Montreal/Square Enix*

**Fixes and workarounds have been added for various games.** For example, crashes/GPU hangs/flickering has been fixed for *Hitman 3*, *Redout 2*, *F1 2020/2021/2022*, and *Guardians of the Galaxy*.  "Various workarounds for game bugs" have been added for *Halo Infinite*. "Countless bug fixes for games" are also in here.

Besides all of this, we have **improved compatibility with Intel's ANV driver, improved stability when minimizing/alt-tabbing in and out of certain games that are in fullscreen**, and plenty of other additions.

Note that since this release uses four new extensions, **you'll need Mesa 22.0/NVIDIA 510.x drivers or higher.** Proton 7.0 stable will stay with vkd3d-proton v2.6. Proton Experimental as well as any future stable Proton release after 7.0 will use v2.7.

Want to try this out before Proton Experimental/GE-Proton incorporates this release? Head over to the [Releases](https://github.com/HansKristian-Work/vkd3d-proton/releases) page and download the tarball. Extract the 64-bit DLL file (`d3d12.dll`) to the same folder where your game's executable file is located (alternatively, extract the 32-bit version if the game you want to use it with is 32-bit). It probably won't be long before either Proton Experimental or GE-Proton picks up vkd3d-proton v2.7 though.

See the full patch notes on [GitHub](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.7). Special thanks to [Ruineka](https://linuxgamingcentral.com/posts/hp-dev-one-review-by-chimeraos-dev/) for helping translate some of these patch notes for me.

*Cover image credit: Codemasters/EA*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
