+++
title = "WinesapOS Updated to 3.1.0 (Alpha), Adds Better Intel and NVIDIA Support"
date = 2022-05-09T22:15:32-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/cover.jpg"
tags = ["news", "software update"]
keywords = ["steam deck", "steamos", "winesapos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[WinesapOS](https://linuxgamingcentral.com/posts/winesapos/) has been updated to [3.1.0-alpha.0](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.1.0-alpha.0). Primary new features to this update include better Intel and NVIDIA graphics driver support, the winesapOS repo has been added, and most of the pre-installed applications now come as Flatpaks.

Previously, since the Neptune kernel doesn't support NVIDIA graphics, users who used GPUs from said company would get a black screen on boot. Now NVIDIA users can select `Arch Linux, with Linux linux-lts (fallback initramfs)` and still be able to use winesapOS. The LTS kernel is now used by default for better hardware support. The winesapOS repo adds pre-built AUR packages from the likes of `linux-steamos`, `mesa-steamos`, and `lib32-mesa-steamos`.

Be aware that you may need to log in twice, due to an issue with KDE Plasma 5.23. Some other known issues are listed as well with their workarounds.

I tried to install this on my GPD Win 3 but unfortunately I still don't seem to be having success. It will go to the GRUB menu and no matter what option I pick the screen remains black. I'm getting in touch with the creator, Luke Short, about this and hopefully we'll be able to figure it out.

Download winesapOS from [GitHub](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.1.0-alpha.0). If you're looking for a more minimal install, try [HoloISO](https://linuxgamingcentral.com/posts/news-holoiso/).

*Cover image credit: WinesapOS GitHub*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
