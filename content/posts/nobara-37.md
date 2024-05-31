+++
title = "Nobara Project 37 Adds GameScope HDR Patches, Upgrades GLIBC While Retaining EAC Fixes"
date = 2023-01-08T11:25:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nobara/version_37.webp"
tags = ["news", "software update", "distro update", "nobara", "fedora"]
keywords = ["fedora", "nobara project"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Fedora fork [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project/) kicks off the new year by releasing version 37. Packages have been rebased on top of [Fedora 37](https://fedoramagazine.org/announcing-fedora-37/). Nobara 37 is mostly concerned with package updates:
- kernel updated to [6.0.16](https://lwn.net/Articles/918807/), all previous patches included, gamescope HDR patches added
- glibc updated to [2.36](https://sourceware.org/pipermail/libc-alpha/2022-August/141193.html) (still includes all previous fixes)
- gamescope updated to latest git
- mangohud updated to [0.6.8](https://github.com/flightlessmango/MangoHud/releases/tag/v0.6.8)
- goverlay updated to [0.9.1](https://github.com/benjamimgois/goverlay/releases/tag/0.9.1) -- this contains a fix for the "interface scaling problem" on HiDPI displays
- blender updated to [3.4.1](https://www.blender.org/download/releases/3-4/)
- rocm opencl/HIP packages updated to [5.4.1](https://github.com/RadeonOpenCompute/ROCm-OpenCL-Runtime/releases/tag/rocm-5.4.1)
- steamtinkerlaunch updated to [12.0](https://linuxgamingcentral.com/posts/steamtinkerlaunch-v12/) and re-added to baseos
- vkbasalt updated to [0.3.2.8](https://github.com/DadSchoorse/vkBasalt/releases/tag/v0.3.2.8) -- this fixes a regression with multiple effects enabled
- supergfxctl updated to [5.0.1](https://gitlab.com/asus-linux/supergfxctl/-/releases/5.0.1) (removes broken/invalid “dedicated” mode)
- asusctl updated to [4.5.8](https://gitlab.com/asus-linux/asusctl/-/releases/4.5.8)
- auto-cpufreq updated to [1.9.7](https://github.com/AdnanHodzic/auto-cpufreq/releases/tag/v1.9.7) and fixed issue with it not auto-enabling by default after install -- auto-cpufreq is an automatic CPU speed and power optimizer for laptops
- linux-firmware updated to [2022-12-14](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/)
- lutris updated to [0.5.11](https://github.com/lutris/lutris/releases/tag/v0.5.11)
- protonup-qt updated to [2.7.6](https://github.com/DavidoTek/ProtonUp-Qt/releases/tag/v2.7.6)
- llvm updated to [15](https://releases.llvm.org/15.0.0/docs/ReleaseNotes.html)
- mesa updated to [22.3.2](https://docs.mesa3d.org/relnotes/22.3.2.html)
- mesa-vulkan-drivers (git) updated to 2022-12-26
- wine-staging updated to [8.0-rc2](https://linuxgamingcentral.com/posts/wine-8.0-rc2/)
- nvidia drivers updated to [525.78.01](https://www.nvidia.com/download/driverResults.aspx/198284/en-us/) -- adds support for the 4070 Ti

Other changes include:
- apparmor dnsmasq profile updated to allow waydroid -- [Waydroid](https://waydro.id/) allows Wayland users to run Android
- [python-rivalcfg](https://pypi.org/project/rivalcfg/) (for steelseries accessories) added to baseos
- firefox builds moved from appstream to baseos

Interestingly enough some packages aren't fully up-to-date -- for instance, ProtonUp-Qt is not using version [2.7.7](https://linuxgamingcentral.com/posts/protonup-qt-2.7.7/), and Lutris is not using version [0.5.12](https://github.com/lutris/lutris/releases/tag/v0.5.12).

Important to note is that even though GLIBC got upgraded to 2.36, it contains the backport that allows certain games with EAC to run, like *Divine Knockout* (see my [GLIBC-EAC post](https://linuxgamingcentral.com/posts/glibc-eac/) for more info).

Full changelog is available on the [official website](https://nobaraproject.org/2023/01/06/jan-7-2023/). I've been using Nobara Project personally for the past two or three weeks...and I've been impressed so far! Expect an impressions article soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
