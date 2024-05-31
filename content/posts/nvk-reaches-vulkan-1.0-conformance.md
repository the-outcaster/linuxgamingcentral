+++
title = "NVK Reaches Vulkan 1.0 Conformance"
date = 2023-11-20T18:17:36Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvk/cover.webp"
tags = ["news", "nvk", "nvidia"]
keywords = ["nvk", "mesa", "vulkan", "nvidia gpus"]
description = "\"This is the first time any Nouveau driver has gotten the Khronos conformance badge on any API.\""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[NVK](https://linuxgamingcentral.com/tags/nvk/) -- the open-source driver for NVIDIA GPUs, spearheaded by the team at Collabora -- is getting better and better as the months go by. Starting today, NVK "is now an officially [conformant implementation](https://www.khronos.org/conformance/adopters/conformant-products/vulkan#submission_757) of the Vulkan 1.0 API on NVIDIA Turing hardware." The blog post from Collabora, written by Faith Ekstrand, mentions that this "is the first time any Nouveau driver has gotten the Khronos conformance badge on any API."

The basic English translation of this: Turing GPUs and later "should pretty much work" with this driver, albeit for app-specific bugs. Maxwell GPUs will get support later down the road. The new back-end compiler for NVK had also gotten [merged](https://gitlab.freedesktop.org/mesa/mesa/-/merge_requests/24998) this week in Mesa, which fixes a number of bugs from the old one.

Faith also outlines their plans for NVK heading into the new year:
> I'll continue improving the new compiler, both in terms of features and performance. Most of the Vulkan API features we're still missing relative to other drivers are effectively compiler features. We're not very far off from being able to advertise Vulkan 1.3 but it's all compiler work between here and there.

At this rate, it wouldn't surprise me if in a few years' time users with NVIDIA GPUs will be able to use NVK as their daily driver without needing to use NVIDIA's proprietary drivers.

See the [blog post](https://www.collabora.com/news-and-blog/news-and-events/nvk-reaches-vulkan-conformance.html) for more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
