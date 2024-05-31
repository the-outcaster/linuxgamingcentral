+++
title = "You Can (Apparently) Run Portal RTX on AMD"
date = 2022-12-22T12:25:54-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/portal_rtx/cover.jpg"
tags = ["news", "portal series", "portal rtx"]
keywords = ["portal with rtx", "portal rtx", "portal rtx on amd", "portal rtx on mesa", "portal rtx on radv"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Looks like Reddit user [Spacefish008](https://www.reddit.com/r/linux_gaming/comments/zs7luf/portal_rtx_on_5700xt_working/) got [*Portal with RTX*](https://linuxgamingcentral.com/posts/portal-with-rtx-now-out/) running on a 5700 XT. They note that they get "~45 FPS on 846x643" on High settings. All that's needed is the `RADV_PERFTEST=rt,emulate_rt %command%` launch parameter. The OP explains how this works:
> It uses DirectX and DXVK exposes the DXR APIs to the game if it detects raytracing support in the underlying Vulkan driver. The Vulkan driver is RADV, which can emulate raytracing via shaders on older-gen AMD GPUs like NAVI10 / RDNA1.

They also have a [video](https://www.youtube.com/watch?v=g2qvN17m9KA) showcasing the game with simulated ray-tracing.

Note that I added the word "apparently" in the title because it's not working on my end with a 6700 XT and Mesa 23. The game will launch but it will crash at the main menu. Using different versions of Proton didn't help. I'm going to take a wild wager that the ray-tracing works with older RDNA1 cards and not RDNA2, which is what the 6700 XT uses (but I'd love it if someone could fill me in on the actual reason why it's not working).

Since the Deck is using RDNA2 as well, *Portal with RTX* probably won't run on it with this setting. Matter of fact, running the game without any launch parameters makes a very trippy experience. I might give it a try though.

![Portal RTX on Deck](/images/steam_deck/photos/portal_with_rtx.jpg)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
