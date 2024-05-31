+++
title = "You NEED Intel's Optane SSD in Your Life"
date = 2022-10-26T21:39:09-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/intel_905p/cover.jpg"
tags = ["intel", "hardware preview", "ssd"]
keywords = ["intel", "intel optane", "905p", "solid state drive", "ssd"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Intel recently sent me their [Optane 905P solid state drive](https://www.intel.com/content/www/us/en/products/docs/memory-storage/solid-state-drives/enthusiast-ssds/optane-ssd-905p-brief.html), consisting of 480 GB of storage. They're the fastest, yet also the most expensive, SSDs that you can buy. Unfortunately Intel will no longer be manufacturing these drives (presumably since they couldn't compete in the SSD market at their price point), but I happen to have the right friends who pointed me in the right direction. Rather than sending the remaining drives into the landfill, I happened to be one of the lucky few who managed to snag one as part of a review unit.

![Intel Optane 905p](/images/intel_905p/drive.jpg)

To be clear, Intel is NOT sponsoring the review. I can prove that by saying how much I think their integrated graphics *suck*. I wasn't surprised to hear that [their ARC GPUs are a mess on Linux](https://www.reddit.com/r/linux_gaming/comments/yaao2x/intel_arc_a750_on_ubuntu_2210_review_and_testing/) right now.

But their SSDs were actually something they did right, at least as far as the speed goes. Like, Sonic the Hedgehog speed. I can tell just by [how quickly *Horizon: Zero Dawn* gets in-game](https://mastodon.social/@linuxgamingcentral/109237624292684299). 14 seconds on the 905P, 29 seconds on Steam Deck!

![Intel Optane 905p features](/images/intel_905p/features.jpg)

With `archinstall`, it took five minutes and eight seconds to install Arch Linux, with NVIDIA drivers and some other extra packages (such as the Cinnamon desktop environment). Now keep in mind Arch has to download some packages from the Internet, so if I had Gigabit Ethernet, it probably would have taken even less time (I have a 60 MB/s connection).

![Arch install time on Intel Optane 905p](/images/intel_905p/archinstall.jpg)

About four seconds to get into the login screen when the computer is turned on:

![Getting to login screen on Intel Optane 905p](/images/intel_905p/boot_time.jpg)

Another two seconds to get the desktop up and running:

![Getting to desktop on Intel Optane 905p](/images/intel_905p/getting_to_desktop.jpg)

Three-and-a-half minutes to transfer 250 GB worth of games, from one PCIe 3.0 x 4 SSD (formatted as btrfs) to the 905P (also btrfs):

![File transfer on Intel Optane 905p](/images/intel_905p/file_transfer.jpg)

There are some other benchmarks that I could show you, such as kernel compilation time, video export time, etc. This also begs the question, "Yeah, you got these numbers, and they might be impressive, but what do they even compare to?" That, my friend, is what the *full* review will be for. Right now, I just wanted to whet your appetite as to the potential this thing offers. Needless to say, I think I will be quite comfortable living with this SSD for the rest of my life.

Special thanks to [Luke Short](https://linuxgamingcentral.com/posts/winesapos-3.2.0-beta/) -- creator of WinesapOS -- for helping me get in touch with Intel. He might just have a [review](https://twitter.com/LukeShortCloud/status/1584610246340726789) of his own, as well. In the meantime I have an [unboxing video](https://www.youtube.com/watch?v=z7FWvvrnHKQ). I would say you should buy the SSDs while they're on sale, but unsurprisingly, they're now out of stock.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
