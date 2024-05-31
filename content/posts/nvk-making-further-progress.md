+++
title = "Open-Source NVIDIA Driver NVK Making More Progress"
date = 2023-03-21T15:34:48Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvk/13fps.webp"
tags = ["news", "nvidia", "nvk"]
keywords = ["nvk", "open-source nvidia driver", "talos principle", "nvidia gpu system processor"]
description = "The Talos Principle has upgraded from 5 FPS to 13 FPS!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A few months ago, users could [run *The Talos Principle* at 5 FPS at 1024 x 576](https://linuxgamingcentral.com/posts/nvk-making-progress/) with NVK. Well, the open-source driver is quickly making more progress. The framerate for the same game has now more than doubled at **13 FPS.** I don't think I could adapt to that framerate; I would probably get a headache. But hey, that framerate is pretty close to the 20 FPS that *Zelda: Ocarina of Time* ran back in the N64 days.

Dave Airlie, developer at Red Hat, [showed off the progress](https://www.youtube.com/watch?v=B5nqYU_FPus). In their [Tweet](https://twitter.com/DaveAirlie/status/1638026355513376768) they mention that the game is being played on a laptop and "running the NVIDIA GPU in offload mode, so 4K image is being copied to the internal Intel GPU for display." Apparently this driver is also making use of NVIDIA's GPU System Processor (GSP), which -- according to [Phoronix](https://www.phoronix.com/news/NVK-Running-Talos-13-FPS) -- is "needed for being able to deliver better open-source driver support and performance."

I'm going to bet by the summer, this same game will be running at least 30 FPS. Great progress so far! See the [post from Phoronix](https://www.phoronix.com/news/NVK-Running-Talos-13-FPS) for more of the technical details.

*Cover image credit: Dave Airlie*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
