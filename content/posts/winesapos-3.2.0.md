+++
title = "WinesapOS -- The Ultimate Portable Linux Gaming Distro"
date = 2022-11-24T11:45:13-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/cover2.jpg"
tags = ["news", "distro update", "software update", "winesapos"]
keywords = ["winesapos", "linux gaming distro", "linux gaming", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[WinesapOS](https://linuxgamingcentral.com/tags/winesapos/) has come a long way. Going from being able to play *Halo* with a friend on Mac, it has now evolved to become much more. It's now become this thing where you can install the distro on a flash drive or MicroSD card for the Steam Deck, and enjoy an awesome gaming experience, with all the software packages you could possibly need provided right out of the gate. No need to install it to your internal drive. It's a truly marvelous experience.

Luke Short, creator of the distro, just went over in a [blog post](https://lukeshort.cloud/blog/linux/#2022-11-24) the history of the project, and how it has had a "small cult following." He also goes over the increased reliability of the distro obtaining software packages via wget, for folks with unreliable Internet; the quicker build times; and the superb swiftness of the [Intel Optane SSDs](https://linuxgamingcentral.com/posts/intel-optane-905p-ssd-first-impressions/).

But there's more than just the blog post. Luke simultaneously released the stable version of WinesapOS 3.2.0. It contains over four months' worth of changes since the previous 3.1.1 release. Key features with this update include:
- **minimal image** -- this has provided a huge advantage for those who want a more minimal version of WinesapOS, while also slimming the file size down significantly. The minimal image is 7 GB -- versus the 29 GB size of the performance and secure images
- **improved Mac support** -- quieter fans and Wi-Fi support for older Macs that don't have the T2 chip
- **improved controller support** -- support for Xbox/Xbox 360 gamepads, as well as various third-party controllers
- **screen rotation support** -- particularly useful for handhelds like the Steam Deck, where it has that annoying portrait orientation
- **support for VirtualBox, VMWare Fusion, and VMWare Workstation**, with guest tools provided "for the best integration and experience possible"
- **increased stability** -- more stable Arch packages, support for "a wide range of hardware," and automated testing via GitHub Actions

Some other minor updates:
- GE-Proton has been upgraded from 7-20 to [7-35](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-35)
- Wine-GE-Proton has been upgraded from 7-16 to [7-31](https://github.com/GloriousEggroll/wine-ge-custom/releases/tag/GE-Proton7-31)
- Pamac has been replaced with bauh, which is evidently "a more stable package manager for non-Manjaro Linux distributions"
- Steam Deck client login bug has been fixed
- ReplaySorcery and vkBasalt have been added for use with GOverlay
- progress bar added for first-time setup and upgrades
- Flatseal and GParted has been added
- PolyMC has been replaced with [Prism Launcher](https://linuxgamingcentral.com/posts/prism-launcher/)
- a number of other smaller adjustments

What can we look forward to with the next update? "Major upgrades!" Such as looking into how to upgrade older versions of WinesapOS, such as 2.2.0, to 3.x. Luke and Thijzer want all of their users "to experience SteamOS 3 on the desktop." And then implementing the Deck game mode session "for a more console-like experience."

See the patch notes and download the distro on [GitHub](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.2.0). I highly recommend giving it a try!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
