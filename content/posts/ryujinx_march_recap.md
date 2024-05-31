+++
title = "Ryujinx: Highlights from March 2022"
date = 2022-04-12T09:13:08-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ryujinx_march/cover.jpg"
tags = ["news", "emulation"]
keywords = ["nintendo switch", "ryujinx"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday a new [blog post](https://blog.ryujinx.org/progress-report-march-2022/) was submitted on the Ryujinx website. I wanted to extract some of the highlights of this post.

To start things off, graphics are now more "stable" on OpenGL with Intel and AMD GPUs. Though games like *Pokémon Legends Arceus* displayed just fine with Ryujinx's Vulkan build, previously the game would look horrendous:

![pokemon legends arceus on amd/intel opengl before fix](/images/ryujinx_march/pla-exploded.jpg)

That's no longer the case:

![pokemon legends arceus on amd/intel opengl after fix](/images/ryujinx_march/pla-unexploded.jpg)

*Game Builder Garage* and *WarioWare: Get it Together!* had a few GPU regressions fixed. Several games now boot much faster due to expanded buffers, and *Super Mario Galaxy* now incorporates the starbit interactions.

Sometimes the viewport while recording a game looked a bit shuffled. This should no longer be the case. Texture corruption is no longer present in certain titles, including *Cartoon Network: Battle Crashers* and *Snack World*.

As for the **CPU**, several improvements were made to the recompiler. For **audio**, a bug was fixed in the renderer, therefore allowing games like *Mononoke Slashdown* and *Paper Mario: The Origami King* to load and no longer crash.

*Splatoon 2* and *Fire Emblem: Three Houses* had a slowdown during certain areas...when checking the time. This has now been fixed.

There's plenty of other small details in the [post](https://blog.ryujinx.org/progress-report-march-2022/); have a read if you want the full story including how the fixes were implemented.

*All images are credit from the Ryujinx team*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
