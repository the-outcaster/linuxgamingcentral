+++
title = "ChimeraOS 43 Adds Support for ASUS ROG Ally, Decreases Game Loading Times"
date = 2023-07-06T13:39:13Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/distro_reviews/chimeraos/cover.jpg"
tags = ["news", "software update", "distro update", "chimeraos", "asus rog ally"]
keywords = ["chimeraos", "chimeraos 43", "asus rog ally", "rog ally linux", "opengamepadui", "aokzoe", "onexplayer"]
description = "Plus a custom kernel and many fixes for OpenGamepadUI!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A juicy new update is out for the excellent console-oriented distro [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos/). This new release has been nearly two months in the making, but it has been well worth the wait.

Some backend work has been put in to make the support of new handhelds more streamlined:
> One of our long term frustrations has been balancing the need for general support while many new devices, especially handhelds, require per device configuration changes. Going forward it will be much easier to enable device specific patches during installations and upgrades.

They're also working on their own kernel now to avoid having to fix issues with the mainline kernel:
> The kernel is still based on the Arch kernel and will enable us to apply upstream patches that affect gaming performance, add gaming features, or fix hardware problems much sooner. It will also ensure we have more control over the kernel that is shipped, which will make the development cycle more predictable. The goal is to stay as close to Arch mainline as possible while avoiding regressions to currently supported hardware.

One big feature that has come to this update is **initial support for the [ROG Ally](https://linuxgamingcentral.com/tags/asus-rog-ally/).** There's audio support, Wi-Fi support, Bluetooth, and partial TDP control via OpenGamepadUI. Do note that suspend functionality is not supported yet; the ChimeraOS team recommends disabling auto-suspend. This makes ChimeraOS the first distro to support said device. Big thanks to Luke Jones and Matthew Anderson for their hard work in making this possible! See the article from [Ars Technica](https://arstechnica.com/gadgets/2023/06/the-linux-coders-turning-the-rog-ally-and-other-handhelds-into-steam-deck-clones/) for more details.

OpenGamepadUI gets a new "CardUI" and along with this comes support for more handhelds and "numerous bug fixes that improve the user experience." Lutris and Yuzu have been added to the plugin store.

The AOKZOE A1 Pro gets fan control support, games should now boot up faster (while some other titles that previously didn't launch should now boot), four new handhelds get gamepad support, update channels can now be seamlessly switched via Steam, Intel OXP devices have better compatibility, a screen rotation quirk was added for the AOKZOE A1 Pro and AYN Loki Max, a few bugs have been fixed, and some other additions have made it in.

Software upgrades are as follows:
- the kernel has been upgraded to [6.3.9](https://cdn.kernel.org/pub/linux/kernel/v6.x/ChangeLog-6.3.9)
- [OpenGamepadUI](https://linuxgamingcentral.com/posts/open-gamepadui/) [0.15.5](https://github.com/ShadowBlip/OpenGamepadUI/releases/tag/v0.15.5) -- fixes detection for the OneXPlayer
- Mesa to [23.1.3](https://docs.mesa3d.org/relnotes/23.1.3.html)

See the full patch notes on [GitHub](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-43-2023-07-06).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
