+++
title = "Broken Shoulder Buttons on Deck? Fix them with an Xbox One Controller!"
date = 2022-08-05T23:11:35-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/tronicsfix/replacing_shoulder_piece.jpg"
tags = ["steam deck", "repair"]
keywords = ["steam deck", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I love TronicsFix's videos. Seeing him tear down various electronics and observing how he fixes most of them almost feels...therapeutic. And now that I watched his [Steam Deck video](https://youtu.be/plba1p5oLg0), I now know what to do if either the touchscreen or the shoulder buttons go bonkers.

In the video he buys a broken Steam Deck for $529. He doesn't mention what SKU it was, but I assume it was the 256 GB model. He finds two problems:
1. Touchscreen isn't working
2. Both the left and right shoulder buttons are not being picked up in-game when pressed

![Steam Deck shoulder PCB](/images/tronicsfix/left_shoulder_deck_pcb.jpg)

The first problem is an easy fix. Just go to the BIOS, enable battery storage mode, turn on the Deck with the AC adapter connected. That's literally all it took to get the touchscreen working again.

The second issue is a little more tricky. The sockets for the shoulder buttons were disjointed; therefore when the shoulder button is pressed, it won't hit the button on the socket itself. Steve tried replacing the three-pronged socket with another one from a Joycon, to no avail. But surprisingly, he was able to take the socket out of a Xbox One controller PCB, solder it onto the Deck daughterboard, and it worked just fine for both bumpers!

![Xbox One controller PCB](/images/tronicsfix/xbox_one_pcb.jpg)

You might say to yourself, "But why not just order the daughterboard from [iFixit](https://www.ifixit.com/Parts/Steam_Deck) and call it a day?" Well, two reasons for that. First, the part isn't in stock right now. Second, even if it was, it's going to cost you far less if you have an Xbox One controller lying around that you aren't using. Some soldering skills are required, but it seems like a simple fix.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
