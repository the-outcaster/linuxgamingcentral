+++
title = "NVK: An Open-Source Vulkan Driver for NVIDIA GPUs"
date = 2022-10-04T22:13:23-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvk/cover.webp"
tags = ["news", "nvidia", "vulkan", "mesa", "nvk"]
keywords = ["nvidia", "turing", "mesa", "vulkan", "nvk", "linux", "open-source", "collabora"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
This almost feels like an April Fools' Day joke that was six months late.

Nouveau -- that terrible open-source graphics driver for NVIDIA? That will soon get replaced with the new open-source [NVK](https://www.collabora.com/news-and-blog/news-and-events/introducing-nvk.html) driver. This was written by Jason Ekstrand from Collabora, as well as Koral Herbst and Dave Airlie at Red Hat.

Getting the driver to work, according to the blog post, was through the Turing class of GPUs, which contained a new unified firmware blob; NVIDIA's open-source [kernel driver](https://github.com/NVIDIA/open-gpu-kernel-modules); and obtaining the official headers for the 3D and compute hardware. You can read the blog post for all the technical information behind that process.

This new NVK driver has been written "almost entirely from scratch" using the new NVIDIA headers, and eventually, it will be merged into Mesa. The long-term goal for this ambitious project "is for NVK to be for NVIDIA hardware what RADV is to AMD hardware," although obviously, the developers have a long way to go to catch up to RADV's features and performance. Currently it's "passing about 98% of the Vulkan CTS with a very basic feature set." Which translates to roughly 20-25% to having a complete feature set. Architechurally, it's "in pretty good shape."

![RTX 2060 and 2070](/images/nvk/2060_and_2070.jpg)
*Image credit: IGN*

[Turing+ cards](https://en.wikipedia.org/wiki/Turing_(microarchitecture)#Products_using_Turing) are supported. Meaning I might actually give this a shot on my GTX 1660 Ti. Kepler, Maxwell, Pascal, Ampere, and Lovelace support should be coming in the future.

What's that? You can actually try it out *now*? Well, yes! Head over to the [Mesa GitLab page](https://gitlab.freedesktop.org/nouveau/mesa), and compile the `nvk/main` branch. It's in alpha quality right now, and bugs are to be expected. Contributions are certainly welcome. NVK won't be merged with Mesa until "a new kernel uAPI to support Vulkan properly" comes out.

All of this and plenty of more information on Collabora's [blog post](https://www.collabora.com/news-and-blog/news-and-events/introducing-nvk.html). I might give this driver a shot myself; hopefully I don't break my system.

*Cover image credit: Collabora*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
