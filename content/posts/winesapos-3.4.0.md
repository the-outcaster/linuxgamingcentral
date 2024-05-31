+++
title = "WinesapOS 3.4.0 Adds Game Mode, Improved Compatibility with SteamOS Applications"
date = 2024-01-01T20:32:26Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/legion_go/winesapos/cover.jpg"
tags = ["news", "distro update", "software update", "winesapos"]
keywords = ["winesapos", "steamos", "legion go"]
description = "The distro seems to work fine on the Legion Go, based on my testing so far."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[winesapOS](https://linuxgamingcentral.com/tags/winesapos) -- the portable gaming distro that requires no installation, spearheaded by none other than the fantastic [Luke Short](https://linuxgamingcentral.com/posts/interview-with-luke-short-creator-of-winesapos/) -- got a huge update with version 3.4.0.

Some highlights with this release:
- Game Mode is now supported, making it a little easier to turn your handheld -- such as the Legion Go -- into a gaming console
- Arc GPUs are now supported via the `linux-t2` kernel
- applications designed specifically for SteamOS should now have better compatibility
- JFS and Bcachefs filesystems are now supported
- you can use ZRAM as opposed to swap when setting the distro up for the first time
- Intel Mac support
- Wayland support (Xorg is still used by default though)
- recovery console should the distro not launch LightDM properly

As far as Game Mode support, note that, as with other distros like ChimeraOS, [support for devices outside of the Steam Deck are limited](https://github.com/LukeShortCloud/winesapOS/tree/3.4.0?tab=readme-ov-file#steam-deck-game-mode). NVIDIA is not supported. Adjusting the TDP or GPU clock speed limits via the QAM will likely not work.

SteamOS packages are now deprecated. Per Luke's comment on [GitHub](https://github.com/LukeShortCloud/winesapOS/issues/561#issuecomment-1835365823):
> It is very time consuming and complicated to keep rebasing these packages. I have been the only maintainer of it for the past 1.5 years. Most of the changes in those projects are already upstream now. Using vanilla Arch Linux or Manjaro packages has proven to be a much more stable and smoother experience for winesapOS.

And here's a nice one: winesapOS is now available as a single download file. You no longer have to download multiple zip files to get one of the images. The downloads are now hosted on [Luke's server](https://winesapos.lukeshort.cloud/repo/iso/winesapos-3.4.0/) (or [archive.org](https://archive.org/download/winesapos-340)). Just download a single zip file -- whether you want the minimal, performance, or secure image -- extract it, then flash it.

This distro keeps getting better and better with every update. I do hope some other content creators besides myself will talk about this wonderful distro that barely gets any advertising.

See the full patch notes -- as well as what to be aware of when trying winesapOS on Steam Deck -- on [GitHub](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.4.0).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
