+++
title = "HoloISO - An Unofficial SteamOS 3 Image"
date = 2022-05-02T12:05:29-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/holoiso/cover.jpg"
tags = ["news", "distro spotlight"]
keywords = ["steam deck", "steamos", "holoiso"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
About a month ago I had talked about a portable Linux distro that gives a SteamOS 3-like experience: [winesapOS](https://linuxgamingcentral.com/posts/winesapos/). Well, as is the traditional case with open-source forks in the Linux landscape of things, we've got another one: [HoloISO](https://github.com/bhaiest/holoiso). I'd still recommend the former over the latter, as winesapOS can be used on any device without installing, and comes with a bunch of extra gaming-related packages, but if you're looking for something a little more minimal, you might want to give HoloISO a try.

Per the GitHub's README, the project "attempts to bring Steam Deck's Holo OS into a generic, installable format!" The first [beta](https://github.com/bhaiest/holoiso/releases/tag/beta0) went out a little less than 24 hours ago (you can also build the ISO from source). Simply download the ISO, flash the image to a USB stick, boot to said device on your computer, connect to the Internet with [`iwctl`](https://man.archlinux.org/man/iwctl.1) if you're using Wi-Fi, run `holoinstall`, select the partition/disk to install to, and let the installation do its' thing. Keep in mind **your device needs to be using an AMD GPU**, with UEFI enabled and secure boot disabled. The flash drive needs to be at least 4 GB.

I tried to install it on my GPD Win 3, but you know all things Intel; the installation went through but for the life of me I couldn't get the display to work in landscape mode. Might be worth a shot though if you have a Aya Neo or Onexplayer that has an AMD APU.

*Cover image credit: HoloISO GitHub*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
