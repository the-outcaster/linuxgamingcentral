+++
title = "External GPU on Steam Deck? It's Possible!"
date = 2022-03-31T12:06:10-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://img.youtube.com/vi/RdgslRR6S2w/0.jpg"
tags = ["steam deck", "egpu"]
keywords = ["steam deck", "external gpu", "windows", "egpu"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[UFD Tech](https://www.youtube.com/channel/UC4Z8mPYjn6Dhr6n531YDh0Q) recently put out a video that answers the question: can you use the Steam Deck with an external GPU? The short answer is yes. The extended answer is:
- this was only tested on Windows
- any GPU from NVIDIA didn't work
- AMD GPUs work but they are bottlenecked by the speed of the M.2 slot on the Deck

{{< youtube "RdgslRR6S2w" >}}

The process is simple: just take a M.2 cable that goes into the M.2 slot on the back of the Deck (you'll have to have the OS installed on a MicroSD card or external drive), insert the eGPU in the slot on the other side of the cable, get the connectors needed for the GPU by connecting a power supply, get the Deck hooked up to a monitor if you wish, then turn the device on. From the cable UFD Tech used, there's no way to close the back of the Deck, so it's a little bit of a clumsy mess.

![m.2 to eGPU adapter](/images/egpu_on_deck/cable.webp)

With an RX 6600 XT connected, *Elden Ring* was unfortunately bottlenecked by the eGPU. It couldn't go any higher than 60 FPS. This is because of the speed and power limitations of the M.2 slot on the Deck. *Cyberpunk 2077*, however, seemed to fair better and played the game more decently at Medium settings.

So there you have it. You can use an external AMD GPU on Windows on the Deck, with a few hardware limitations. I imagine it's the same story with Linux.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
