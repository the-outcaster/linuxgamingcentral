+++
title = "Distro Spotlight: WinesapOS"
date = 2022-03-31T13:44:24-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://user-images.githubusercontent.com/10150374/157773891-3823ffb7-8ea9-4528-9988-563da174cd5a.jpg"
tags = ["app spotlight", "distro"]
keywords = ["winesapos", "steamos 3.0", "steam deck", "luke short", "distro", "distribution"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Ever wanted to use SteamOS 3.0 on a device outside of the Steam Deck? Well, [winesapOS](https://github.com/LukeShortCloud/winesapOS) makes that possible. The name of the project is derived from [Wine](https://www.winehq.org/), the compatibility layer that allows Windows software to run on Linux, and also how the developers "develop on Macs and ship drivers for them." The distro was created by [Luke Short](https://lukeshort.cloud/), a sales engineer at VMware and technical writer for Android Police. 

Here's a nice bonus: **no installation required**. You can use the distro right off your flash drive.

![winesapos desktop](https://user-images.githubusercontent.com/10150374/157773891-3823ffb7-8ea9-4528-9988-563da174cd5a.jpg)
*Inage credit: WinesapOS GitHub page*

It also comes with quite a few software packages to get you quickly set up:
- BalenaEtcher
- Bottles
- Discord
- Firefox ESR
- Chrome
- KeePassXC
- LibreOffice
- OBS Studio
- VLC
- ZeroTier GUI
- among *many* others

As well as gaming packages:
- Steam
- Heroic Games Launcher
- Lutris
- Wine/Proton GE
- GameMode
- Gamescope
- MangoHUD
- GOverlay
- ProtonUp-Qt
- still others

It has the [Steam Big Picture GRUB theme](https://github.com/LegendaryBibo/Steam-Big-Picture-Grub-Theme):

![steam bpm grub theme](https://camo.githubusercontent.com/5c110f58c3208e45b2afd1f4fbb01ea9c4572c7d51009294152be7fb780fb828/687474703a2f2f692e696d6775722e636f6d2f7951434f6a6e522e706e67)
*Image credit: Steam Big Picture GRUB theme GitHub*

The Steam client uses the Deck UI and the KDE desktop uses Valve's Vapor theme. There's also monthly Btrfs backups, and it has support for many file systems. Updates are *not* automatic, and there's auto-cpufreq for power management. Macs are partially supported.

The winesapOS image is pretty big at 30 GB, so you'll want a flash drive that has 32 GB minimum. Minimum computer requirements are 4 GB of RAM with a dual-core AMD/Intel processor.

There are a few differences between winesapOS and SteamOS 3.0. First of all, winesapOS supports all three GPU vendors. SteamOS 3.0, to my knowledge, only works with AMD. winesapOS's file system is both encrypted and writable, with support for Btrfs snapshots. Snaps are available to install. In addition to Valve's Neptune kernel (5.13), winesapOS also supports the LTS kernel (5.15). So it does have a few advantages over vanilla SteamOS 3.0.

I may have a review at some point of this distro. It looks interesting. I tried to install it on my GPD Win 3, but I don't think the distro plays nicely with Intel. But give [the distro](https://github.com/LukeShortCloud/winesapOS) a shot if you want the SteamOS 3.0 experience anywhere, with the added benefit of portability!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
