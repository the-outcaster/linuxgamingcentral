+++
title = "Need to 'Unsnap' Your System? Try Unsnap"
date = 2022-04-05T14:32:51-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/unsnap/cover.png"
tags = ["snaps", "ubuntu"]
keywords = ["canonical", "alan pope", "snaps"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Ubuntu has [a lot of hate](https://thelinuxexp.com/Ubuntu-hate/). Snaps are part of the reason for the distaste of the distro.

Well, if you happen to be using Ubuntu, you no longer have to use them, thanks to [unsnap](https://github.com/popey/unsnap). Unsnap runs a script that not only removes all Snaps from your system, but also installs the Flatpak version of the application if it's available.

![unsnap in use](/images/unsnap/screenshot.png)
*Image credit: Popey's GitHub Repo*

For the time being the script only works on Ubuntu, and is **in pre-alpha stage**, but other distros could be supported via contributions. Pop!_OS and Linux Mint already have the snap daemon removed, but someone could install `snapd` later on. Other distros also support snaps, including Manjaro and elementaryOS.

What's interesting is this was created by the very person who used to work for Canonical: [Alan Pope](https://mastodon.social/@popey), also known as "Popey." He left a while back [due to desktop issues getting ignored, despite his efforts to help out](https://www.reddit.com/r/linux/comments/orz1lr/alan_pope_left_canonical_because_of_snaps/).

Give the script a go if you're running an Ubuntu system and don't want any Snaps. Or have a look at the code and see what you can do to make the script more stable or support more distros!

*Cover image credit: Popey's GitHub Repo*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
