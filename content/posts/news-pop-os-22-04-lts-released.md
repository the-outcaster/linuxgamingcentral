+++
title = "Pop!_OS 22.04 LTS Released -- Switch to PipeWire, Hyrbid Light and Dark Backgrounds, Automatic Updates, and Plenty More!"
date = 2022-04-25T10:24:23-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/pop_os/22_04/cover.jpg"
tags = ["software update", "pop!_os", "system76"]
keywords = ["pop!_os", "system76", "22.04 lts"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[Pop!_OS](https://pop.system76.com) -- the Ubuntu-powered distro created by none other than the geniuses at System76 -- has just released **22.04 LTS** (long-term support), shortly after the release of Ubuntu 22.04. There's quite a few exciting things going on with this release, so let's go over the changes.

![pop!_os 22.04 lts driver upgrades](/images/pop_os/22_04/drivers.jpg)

# Software Upgrades
As far as base upgrades are concerned, the kernel is using [5.16.19](https://lkml.kernel.org/lkml/164942304624388@kroah.com/T/) (kind of surprised they didn't go with 5.17), Mesa drivers have been upgraded to [version 22](https://docs.mesa3d.org/relnotes/22.0.0.html), and the desktop environment is based off of [GNOME 42](https://release.gnome.org/42/) with System76's [COSMIC](https://blog.system76.com/post/648371526931038208/cosmic-to-arrive-in-june-release-of-popos-2104) UX spinoff.

# PulseAudio Upgraded to PipeWire
[PipeWire](https://pipewire.org/) is a much-needed upgrade to the old PulseAudio system, bringing with it lower latency, real-time multimedia processing, sandbox support, and plenty of other features, while still being backwards-compatible with PulseAudio. Pop!_OS 22.04 has **switched to this newer audio system.**

# Easy Tech Support with New Support Panel
Getting **support is now as simple as going to the bottom of the Settings menu** and selecting one of the options available. You can view the [support documentation](https://support.system76.com/) on System76's website, use the community [chat room](https://chat.pop-os.org/login) (there are S76 engineers in that room as well), submit a [support ticket](https://system76.com/my-account/support-tickets/new), or generate a log file, from which you can send to one of their "Happiness Technicians" to more effectively troubleshoot your issue.

![pop!_os 22.04 lts new support panel](/images/pop_os/22_04/support.jpg)

# Automatic Updates
One thing that bugged me in the past with Pop!_OS was constantly getting notifications from the Pop! Shop whenever there was a software upgrade available. Well, with the new introduction of **automatic updates**, that's no longer a thing. You can now schedule a day and time for the system to automatically update Debian, Flatpak, and even Nix packages without distracting you.

Note that this is *not* enabled by default. If you choose to update manually, **you can choose the frequency** with which you get notifications: daily, weekly, or monthly.

![pop!_os 22.04 lts updates](/images/pop_os/22_04/updates.jpg)

# Miscellaneous Improvements
Some improvements have been made to the **Pop!_Shop. In addition to UI enhancements and a overall snappier experience**, the NVIDIA drivers no longer have an "install" button if they're already present on the system. It's also possible to downgrade the driver version here; which is a huge plus in my book as half the time I try to downgrade the driver on Arch I end up breaking my system.

Supposedly **the [CPU scaling governor](https://github.com/pop-os/system76-scheduler) has been improved to give better performance**. The scheduler, as the press documentation brings out, "optimizes performance by directing resources to the window in focus." This means a "much smoother" experience while gaming in fullscreen, for example.

There's now support for **hybrid light and dark backgrounds**, depending on what workspace you're using. Not everything has to be put in light or dark mode. You can now have one workspace set in light mode and the other in dark.

![pop!_os 22.04 lts workspaces](/images/pop_os/22_04/workspaces.jpg)

Laptop privacy screens are now supported. This is in addition to better multi-monitor support, increased performance while viewing your workspaces, and what was previously a bugged layout on HiDPI displays is now fixed. There are some other minor adjustments as well, including the limitation of the file size for journald logs to 1 GB, the ability to resume upgrading a Debian package if it was disrupted for some reason, `.svg` file type icons, RDP is set as the default option for remote desktop support, and a new [user icon](https://github.com/pop-os/default-settings/commit/77e14a2847fada0e979b1bb519e4f291b7bb3246).

So here's a quick **TL;DR** of the changes:

- kernel 5.16.19, Mesa 22, GNOME 42 base with COSMIC UX
- switch to PipeWire
- easier tech support via the support panel
- automatic updates is now available as an option, without annoying you with upgrade notifications
- a better experience with the Pop!_Shop
- improved CPU scheduler with better performance
- light AND dark theme support between workspaces
- improved multi-monitor and HiDPI display support
- other minor adjustments and improvements

All of this in Pop!_OS 22.04! I'm tempted to actually wipe my Arch install with this. Download the new release from [pop.system76.com](https://pop.system76.com). But do note that **you may want to [back your system up](https://support.system76.com/articles/backup-files/) before upgrading** in the event of an "extremely rare" case of data loss.

![pop!_os 22.04 lts updates](/images/pop_os/22_04/upgrade.jpg)

*Images and screenshots provided by System76*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
