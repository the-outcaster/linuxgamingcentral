+++
title = "DualSense Edge Gamepad Getting Early Linux Support"
date = 2022-10-24T11:21:56-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/dualsense_edge/cover.jpg"
tags = ["news", "sony", "controller", "gamepad", "dualsense"]
keywords = ["sony", "dualsense", "dualsense edge", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As if it wasn't enough of a surprise that [Sony created an official driver for the DualSense on Linux](https://www.phoronix.com/news/Sony-HID-PlayStation-PS5) a few years ago, they've now upped their game and have [added initial support for their upcoming DualSense Edge](https://www.phoronix.com/news/Sony-DualSense-Edge-Linux) -- basically Sony's answer to the Xbox Elite gamepad. The funny thing is the controller won't even be on shelves until early next year. But by sending the patch in this early, hopefully it will be merged into the Linux kernel by the time you get your hands on one.

You can see the patch [here](https://git.kernel.org/pub/scm/linux/kernel/git/hid/hid.git/commit/?h=for-next&id=b8a968efab301743fd659b5649c5d7d3e30e63a6). Right now it's very basic -- it just adds the new device IDs. Meaning there won't be support for reprogrammable buttons and "other customizations." Even so, this should make the gamepad "working to the level of the DualSense controller." This has been submitted for kernel 6.2, which will be opening up at the end of the year. As time goes on, hopefully patches will be added to make the more sophisticated features of the gamepad work.

As I don't have any contacts with Sony, I doubt if I will get a review sample of the controller. I'll try though. Not sure if it justifies the $200 price tag...

Thanks to [Phoronix](https://www.phoronix.com/news/Sony-DualSense-Edge-Linux) reporting on this. And thanks certainly goes out to Roderick Collenbrander, who's responsible for the development of the driver.

*Cover image credit: Sony*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
