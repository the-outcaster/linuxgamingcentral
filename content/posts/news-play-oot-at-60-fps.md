+++
title = "Play *Zelda: Ocarina of Time* at 60 FPS, Natively on Linux"
date = 2022-05-15T21:52:21-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ship_of_harkinian/cover.jpg"
tags = ["news", "pc port", "zelda"]
keywords = ["zelda", "ocarina of time", "linux", "ship of harkinian"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A project by the name of [Ship of Harkinian](https://github.com/HarbourMasters/Shipwright/) (or Shipwright) converts your copy of *Zelda: Ocarina of Time* to a reverse-engineered PC port. I'm counting the days before Nintendo shuts the project down, but for the time being, with the PC port we can achieve:
- experimental 60 FPS support
- widescreen support
- tunic color customization
- cheats
- minimal HUD
- individual volume levels for music, sound effects, fanfare, etc.
- vibration 
- gyroscope support when aiming (it's somewhat ineffective though)
- adjustable internal resolution and MSAA
- adjustable text speed
- faster push block
- and a whole lot more!

![castle garden](/images/ship_of_harkinian/3.jpg)

Last Friday the Ship of Harkinian YouTube channel uploaded a new [video](https://youtu.be/4W1ZyCGCVuE) that goes over some of the new features that have come to the PC port. Save states and mods are now supported, as well as a few other things, but importantly, it's now possible to compile and run the game on Linux hardware. I ran a [test](https://youtu.be/ho-7-Kwr0n0) earlier today on Arch and it's totally do-able.

I have to say, the 60 FPS experience is a bit jarring at first. We're so used to seeing the game run at 20 FPS that it takes a bit of time getting used to the faster animations. I will say though, after adjusting to it, gameplay is *so* much smoother than it was before.

![pushing a block](/images/ship_of_harkinian/2.jpg)

Their binary downloads are locked behind their [Discord channel](https://discord.com/invite/BtBmd55HVH), but you can compile from source on their GitHub. Instructions can be found [here](https://github.com/HarbourMasters/Shipwright/blob/develop/BUILDING.md). Building the project requires a Docker container, and the ROM that you own needs to be very specific. It has to be the ROM extracted from the PAL version of the GameCube disc.

It probably won't be long before we see HD graphics and skippable cutscenes. I'm particularly looking forward to the latter. Then again, this is all in the hopes the project remains alive without the Big N's interjection.

![what a hot beat!](/images/ship_of_harkinian/4.jpg)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
