+++
title = "Halo Infinite Making Strides with GE-Proton"
date = 2022-06-27T15:54:53-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/codeweavers/halo.jpg"
tags = ["news", "halo"]
keywords = ["halo infinite", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Looks like we're finally able to run *Halo Infinite* on Linux by means of GE-Proton7-22. Take it with a grain of salt though as this is in the early stages. The game refuses to run on my desktop with an NVIDIA GPU but it looks like it's running pretty well on my Deck, albeit with some missing textures.

![halo infinite on deck](/images/halo_infinite/on_deck.jpeg)

Someone on the [GitHub issue tracker](https://github.com/ValveSoftware/Proton/issues/5030#issuecomment-1167843907) mentioned using a custom-patched Mesa library in order to get the weapons and players to properly render...and it looks like the [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project/) already has this patched version of Mesa. Looks like I'll be installing this on an SD card and testing that way.

Although, interestingly enough someone else on the issue tracker has been able to run the game on a RTX 3070, I wonder what they had to do to get it working.

![halo infinite on rtx 3070](/images/halo_infinite/screenshot.jpg)
*Image credit: kodatarule on GitHub*

In any case, make sure you either rename or delete the video files found inside the `videos` folder in the game's installation directory; the game won't be able to play the videos back and will just return to Steam.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
