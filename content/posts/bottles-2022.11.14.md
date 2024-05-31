+++
title = "Bottles 2022.11.14 Adds Quality-of-Life Improvements, Fixes DLSS"
date = 2022-11-14T15:33:42-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/bottles/2022.11.14.png"
tags = ["news", "software update", "bottles"]
keywords = ["bottles", "wine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Today's update to Bottles -- an easy way of running Windows-based applications on Linux -- fixes GameScope, DLSS, updates translations, rewrites the vkBasalt frontend, and adds other QoL improvements. Patch notes are as follows:

Backend:
- Fix Gamescope arguments by @jntesteves
- Fix DLSS by @cyberphantom52
- Don't use d3d10 & d3d10_1 dll's from dxvk by @Blisto91

Frontend:
- Improve bottle details view by @cyberphantom52
- Redesign details view by @cyberphantom52
- Add grade tooltips by @TheEvilSkeleton
- QoL improvements by @TheEvilSkeleton
- Rewrite vkBasalt frontend by @TheEvilSkeleton
- Minor consistency fixes by @TheEvilSkeleton
- Minor improvements for drive selection by @TheEvilSkeleton

Fixes:
- cli: Fix ignored name when adding program via CLI by @zphensley42
- NVAPI hotfix by @cyberphantom52
- Header Capitalization and localization fixes by @A6GibKm
- Fix installer completion by @jntesteves
- Fix deadlock of Popen.wait by @davidmartos96

Miscellaneous:
- translation updates by @weblate
- Use metainfo by @TheEvilSkeleton
- Add accel for window.close and chain up vfunc by @A6GibKm
- about: Add libraries to acknowledgements and remove slashes by @TheEvilSkeleton
- Settings Rework by @jannuary

Patch notes can also be read on [GitHub](https://github.com/bottlesdevs/Bottles/releases/tag/2022.11.14). The Bottles team recommends installing the [Flatpak](https://flathub.org/apps/details/com.usebottles.bottles) version for the best compatibility.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
