+++
title = "Cemu 2.0-21 Gets Vulkan on Wayland Support, AppImage Fixes"
date = 2022-12-14T09:03:08-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/cemu/cover.jpg"
tags = ["news", "cemu", "software update", "emulation", "wii u"]
keywords = ["cemu", "wii u emulation"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Cemu got a pretty sweet update: it now supports Vulkan for Wayland. The AppImage got "minor" fixes; it fixes an incorrect recursive copy and adds a metainfo file. Screenshots should now work across all three operating systems. Some other commits made it in:
- fix MSVC workflow
- automatically scale imgui text based on display pixel density
- correctly create screenshot directory if it does not exist, and better screenshot error handling
- PPCAssembler: Fix incorrect cast sign of branch distance calculate 
- make codebase more CPU-agnostic + MacOS disclaimer
- Linux/MacOS: Use faster clock_gettime() for tick_cached()
- add check for backwards delete
- fix SDL controller reversed y axis in UI

See the [commit history](https://github.com/cemu-project/Cemu/compare/v2.0-19...main) for more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
