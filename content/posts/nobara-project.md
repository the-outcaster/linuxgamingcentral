+++
title = "Nobara Project - All your Gaming Needs Fulfilled"
date = 2022-06-07T06:51:06-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fedora/cover.webp"
tags = ["project spotlight", "fedora", "nobara"]
keywords = ["nobara project", "fedora"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As reported recently by [Boiling Steam](https://boilingsteam.com/a-bunch-of-linux-gamers-are-trying-fedora-out-in-2022/), it appears Fedora is on the rise for Linux gamers, according to stats on ProtonDB. It grew from 3.7% of total reporters in 2019 to 10.2% in just a few years. That means a little over 200 users out of the 2,096 reporters are using it. Currently it's standing neck-and-neck with Pop!_OS, the latter of which is at 10.4%.

It's not really surprising to see. It seemed like GloriousEggroll, AKA Thomas Crider, started the trend as he was creating [his fork of Proton](https://linuxgamingcentral.com/posts/proton_ge_tutorial/). In an [interview](https://boilingsteam.com/learning-more-about-protonge-with-gloriouseggroll/) he had said:
> I didn’t start using Fedora until I landed my job with Red Hat in 2018, and once I got used to Fedora it’s been my daily driver ever since. (Sorry Arch, Fedora is just a wee bit more stable and polished).

[Other people](https://linuxgamingcentral.com/posts/fedora_the_new_ubuntu/) would pick up Fedora later on and realize the same benefits: Adam Adamou from OverActive Media, and Nick from The Linux Experiment. The general consensus is this: Fedora offers *cutting-edge* software as opposed to bleeding-edge. So, you get up-to-date packages, but they have been tested before they go out on the official repos. So while on Arch you can have the latest software, something might break.

The problem that Fedora has, however, is it tends to stick with FOSS as much as possible. Meaning getting anything proprietary, including NVIDIA drivers, can be a bit of a pain.

Enter the [Nobara Project](https://nobaraproject.org/), created by the same person who is responsible for GE-Proton. The project is aimed at providing gamers a better out-of-the-box experience with Fedora. Examples of packages that come with the Nobara Project include:
- NVIDIA drivers
- OBS Studio
- Wine dependencies (winetricks, gstreamer, etc.)
- third-party codecs
- Steam
- Lutris
- gamescope
- xone (kernel module for wireless Xbox controllers)
- goverlay
- mangohud
- vkbasalt
- LibreOffice
- printer drivers
- kdenlive
- Blender
- ProtonUp-Qt
- flathub repo enabled by default

While these packages can be installed on a vanilla Fedora computer, the goal here is to make a gamer's life with Linux more simple. No need to enter the terminal. Just get everything set up so the user can start gaming right away.

Additionally, the Nobara Project comes with a few tweaks. Just the kernel itself has been patched with futex2, fsync, winesync, "cherry-picked zen patches," OpenRGB, AMD CPCC, Steam Deck support, and a few other patches.

It certainly sounds like an interesting project. If Arch ever breaks on me I might just switch over to this.

There's two flavors that you can download. You can get either the GNOME edition or KDE. Both are currently based off of Fedora 36. Head over to the [official site](https://nobaraproject.org/) to learn more and try the distro out yourself!

*Cover image credit: Fedora official website*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
