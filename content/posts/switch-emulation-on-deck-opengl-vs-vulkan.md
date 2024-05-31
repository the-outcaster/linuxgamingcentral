+++
title = "Switch Emulation on Deck -- OpenGL VS. Vulkan Tested"
date = 2022-08-03T12:15:50-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/dread.jpg"
tags = ["steam deck", "emulation", "nintendo switch", "ryujinx", "comparison"]
keywords = ["steam deck", "ryujinx", "emulation", "nintendo switch"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Since [Vulkan has been merged into the mainline Ryujinx build](https://linuxgamingcentral.com/posts/vulkan-now-merged-with-ryujinx-main-build/) a few days ago, curiosity got to the better of me and I wanted to do a comparison between this and the older OpenGL API. Vulkan, particularly on AMD -- and therefore the Steam Deck -- supposedly has a *huge* number of benefits over OpenGL, including faster shader compilation. I tested the following games:
- *Metroid Dread* (please be aware there are spoilers here!)
- *Mario Strikers: Battle League*
- *Kirby and the Forgotten Land*
- *Super Smash Bros. Ultimate*

And ran each game with OpenGL and Vulkan. You can see the results on [YouTube](https://youtu.be/JxbYIKYWSbU). Vulkan -- for the most part -- does handle Switch emulation on Deck remarkably better than OpenGL. You'll especially notice this on games with lots of shaders -- such as *Smash Ultimate*. The game loads much faster, even though there still is a little bit of stuttering (I should note I ran each game only once; shader compilation times get shorter and shorter with subsequent playthroughs). On the other hand, games like *Metroid Dread* barely saw a difference. In fact, OpenGL rendered the ending cutscene better. For the most part though, I *highly* recommend sticking with Vulkan. Performance is much smoother.

Congrats to the Ryujinx team for such a huge accomplishment. There will soon be a LDN build too (basically a netplay build), which will incorporate Vulkan support. And stay tuned for a guide on Switch emulation on Deck!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
