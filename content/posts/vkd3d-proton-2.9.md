+++
title = "VKD3D-Proton 2.9 \"Greatly\" Reduces System Memory Requirements, Improves CPU Performance"
date = 2023-05-21T17:06:31Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/elden_ring.jpg"
tags = ["news", "software update", "vkd3d-proton"]
keywords = ["vkd3d-proton", "vkd3d-proton 2.9", "elden ring", "radv", "nvidia", "intel", "dxr 1.1"]
description = "This, along with plenty of bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
On Friday the DX12 to Vulkan translation tool VKD3D-Proton was updated to version 2.9. Some awesome additions that came with this update are "greatly" reduced RAM requirements when a game/application is run for the first time, shader compilation stutter avoidance "in some extreme edge cases," improved performance "with certain bad occlusion query patterns," such as *Elden Ring*, improved CPU performance with AMD and NVIDIA (Intel remains to be determined), improved "VRAM oversubscription behavior" when a certain Vulkan extension is supported, improved DXR 1.1 support, compatibility with [DXVK 2.2](https://linuxgamingcentral.com/posts/dxvk-2.2/), native Linux swapchain support, "several 100s of MBs of memory" saved with a RADV workaround, and much more.

There's also plenty of bug fixes, although the patch notes mention that "listing individual games is becoming impractical at this point," and shader bugs have also been fixed in DXIL-SPIRV.

See the full patch notes on [GitHub](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.9).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
