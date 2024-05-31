+++
title = "Vanilla OS - Containerize Your System Like Nobody's Business"
date = 2023-01-08T13:21:19Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/vanilla_os/cover.webp"
tags = ["news", "distro spotlight", "vanilla os", "ubuntu"]
keywords = ["vanilla os", "bottles", "ubuntu"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Vanilla OS, per the description on the [official website](https://vanillaos.org/), is "an Ubuntu Linux-based Point Release distribution that receives updates at the right time, neither before nor after, without sacrificing security and functionality." It's "your faithful colleague by day" and "your teammate by night." The developer, [Mirko Brombin](https://github.com/mirkobrombin/), is also the developer of the [Bottles](https://linuxgamingcentral.com/tags/bottles) application.

It uses GNOME as the desktop environment -- "a stock, clean version with as few changes as possible" -- and as far as the gaming aspect is concerned, you don't need to worry "about setting up your devices." Vanilla OS uses the latest stable kernel, and includes an integrated driver manager. 

![Vanilla OS desktop](/images/vanilla_os/vanilla-os-gnome.png)

You have the ability to choose which package format to use when installing software, be it Snap, Flatpak, or AppImage, and the distro "will take care of the rest." You can also install packages via apx, the distro's unique package manager. Per the description on the [blog post](https://vanillaos.org/2022/12/29/vanilla-os-22-10-kinetic.html):
> Apx introduces a whole new paradigm in package management. The idea is to use your system only as a box for storing your files, leaving it clean of packages and limiting the risk of breaking due to incompatible, poorly constructed or conflicting packages.

The really neat thing about this is not only can it install Ubuntu-based packages, but it can also install Arch and Fedora packages by passing the appropriate flag!

There's also their ABRoot technology system, where if making a change to the system fails, it won't apply said change:
> Let’s say you want to install a new package. ABRoot will check which partition is the present root partition (i.e A), then it will mount an overlay on top of it and perform the transaction. If the transaction succeeds, the overlay will be merged with the future root partition (i.e B). On your next boot, the system will automatically switch to the new root partition (B). In case of failure, the overlay will be discarded and the system will boot normally, without any changes to either partition.

Similar to how SteamOS works, core parts of Vanilla OS are immutable, preventing "unwanted changes and corruption from third-party applications or a faulty update." Components are only updated via "controlled and atomic transactions," which is in reference to ABRoot. These transactions are not applied if they fail. The `$HOME` directory, however, is writable.

But the features don't end there. Vanilla System Operator (VSO) will occasionally check for updates. If the system isn't under heavy use, and the battery isn't low, the updates will be downloaded and installed in the background. These updates will then be applied on the next reboot. This was designed "to take away an annoying task from the user, who simply wants to do their own thing." Finally, Vanilla OS has its own unique installer "to provide a user experience built for you."

![Vanilla System Operator](/images/vanilla_os/vanilla-os-updates.png)

Not too long ago, the Vanilla OS team [released their first stable ISO](https://vanillaos.org/2022/12/29/vanilla-os-22-10-kinetic.html) to the public, based on Ubuntu 22.10 with GNOME 43.

The immutability aspect, combined with the fact that I can install packages from three different distributions on one distro, makes this something I'm certainly going to try. I will do so after I write my impressions with [Nobara Project](https://linuxgamingcentral.com/posts/nobara-37/).

Source code is available on [GitHub](https://github.com/Vanilla-OS). Documentation is available [here](https://documentation.vanillaos.org/). DistroTube has a [video](https://www.youtube.com/watch?v=yajUbh0H6-s) briefly going over the installation and basic use of the distro if you'd like to check it out.

*All images used in this article are credit of the Vanilla OS team.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
