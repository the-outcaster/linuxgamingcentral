+++
title = "Wine 9.0 Released, Adds Experimental Wayland Support and ARM64 Support"
date = 2024-01-16T22:16:48Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/9.0.webp"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "wine 9.0", "wine wayland", "wine arm64"]
description = "There's also \"better graphics performance\" and \"better memory allocation performance.\""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After five release candidate stages, a year of development effort, and "over 7,000 individual changes," Wine 9.0 is now released as stable. Some new features with this release:
- WoW64 support
- experimental Wayland support -- basic window management, multiple monitors, high-DPI scaling, relative motion events, and Vulkan support
- Windows binaries can now be run on ARM64!
- dark theme support via WinRT theming
- support up to Vulkan 1.3.272
- "better graphics performance" via GdiPlus function optimizations
- lower power consumption "in programs which do not occupy the command stream's entire available bandwidth"
- D3D10 effects "support many more instructions"
- better compatibility with older games that use DirectInput action maps
- "better memory allocation performance" via Low Fragmentation Heap (LFH)
- updates to bundled libraries, including VKD3D (1.10) and Faudio (23.12)
- among many, *many* other improvements

Keep in mind in regards to Wayland, it isn't enabled by default. Users will have to run the following:

`wine reg.exe add HKCU\\Software\\Wine\\Drivers /v Graphics /d x11,wayland`

Then make sure the `DISPLAY` environment variable is unset.

It will probably take a few months before Valve re-bases Proton on this new release, but no doubt it will be an update to look forward to!

See the full patch notes on [WineHQ](https://gitlab.winehq.org/wine/wine/-/releases/wine-9.0).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
