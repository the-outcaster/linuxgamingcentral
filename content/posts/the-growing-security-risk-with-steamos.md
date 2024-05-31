+++
title = "SteamOS: A Growing Security Risk"
date = 2022-07-22T13:19:28-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steamos/cover.jpg"
tags = ["steamos", "steam deck", "opinion"]
keywords = ["steamos", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you thought I was critical enough of Valve in my [Steam Deck review](https://linuxgamingcentral.com/posts/steam-deck-review/), well, you might want to strap on your seat belt, because I'm not done yet. (That being said, I did make a few [clarifications](https://linuxgamingcentral.com/posts/clearing-up-some-misconceptions-about-lgc/) earlier this week about some wrong assumptions that I had made, so please give that a read if you haven't already.)

The Steam Deck UI is tightly integrated into SteamOS, giving the Deck a console-like experience with gamepad navigation across different menus, not only giving PC gaming a breath of fresh air, but also -- thanks to Valve's efforts -- getting Linux into the hands of more and more people. Updates to the device have been very frequent -- just about every week there's at least one update to the Steam Deck client. Valve has aggressively been listening to customer feedback and addressing concerns that they have.

However, despite the frequency of the updates, there's the elephant in the room that Valve has yet to address: the underlying operating system that powers the Steam Deck, SteamOS. SteamOS suffers from outdated software packages, namely, Firefox, glibc, the Plasma desktop, the kernel, and Mesa drivers.

The stock version of [**Firefox**](https://linuxgamingcentral.com/posts/firefox-outdated-on-steamos/) supplied with SteamOS, even with the 3.3 beta, is at version 96.0.3. This build is almost *six months* old at the time of writing this.

![vanilla firefox on steamos](/images/steamos/firefox.jpg)

Firefox 96 is known to be vulnerable to at least four critical security flaws, and potentially dozens of others. For instance, [it has an exploitable sandbox escape via the WebGPU IPC framework](https://www.mozilla.org/en-US/security/advisories/mfsa2022-09/) and also [could allow attackers elevated privileges if they're able to corrupt the methods of an Array object in JavaScript](https://www.mozilla.org/en-US/security/advisories/mfsa2022-19/).

Valve had confirmed to [GamingOnLinux](https://www.gamingonlinux.com/2022/07/you-should-avoid-the-stock-firefox-install-on-steam-deck-as-its-badly-outdated/) that they're "aware of the issue and will soon be shipping an update to the SteamOS Beta to address it" and that the stock version of Firefox will be replaced with the Flatpak version. However, that was over two weeks ago and we haven't heard anything from Valve since.

For those who aren't aware, [**glibc**](https://en.wikipedia.org/wiki/Glibc), or the GNU C Library, provides all the core libraries for GNU/Linux. Such libraries include APIs for things like opening, reading, or writing into a file on the system, as well as supply functionality to such things as printf, crypt, login, exit, and much more. The latest stable release at the time of recording this is [2.35](https://sourceware.org/pipermail/libc-alpha/2022-February/136040.html). The Deck is using [2.33](https://sourceware.org/pipermail/libc-alpha/2021-February/122207.html). This version is nearly 18 months old!

![glibc on steamos](/images/steamos/glibc.jpg)

The **kernel** is lagging behind at version 5.13. We're almost approaching 5.19. Even Ubuntu 22.04 uses a more up-to-date kernel at 5.15. There's been a vast amount of security updates since kernel 5.13. For instance, [kernel 5.17 replaced the kernel's random number generator from SHA1 to BLAKE2](https://www.makeuseof.com/linux-kernel-517-released-with-security-fixes/), which supposedly has tighter security and faster performance.

How about **Plasma**? SteamOS is using [5.23.5](https://kde.org/announcements/plasma/5/5.23.5/). This package is over six months old. Plasma [5.25.3](https://kde.org/announcements/plasma/5/5.25.3/) came out last week. Plasma 5.25 would be of great benefit to the Steam Deck in particular, because [it adds a Touch Mode if a keyboard isn't connected](https://linuxgamingcentral.com/posts/kde-plasma-5.25/), making desktop icons larger and therefore easier to work with. Security may not be as much of a concern here, but the features would be a welcome change nonetheless.

![kde plasma on steamos](/images/steamos/plasma.jpg)

Finally, consider the fact that the Deck is using **Mesa** [22.0.2](https://docs.mesa3d.org/relnotes/22.0.2.html) (on the SteamOS 3.3 beta). While this version isn't as old as some of the other software packages on SteamOS, it's still three months behind the current [22.1.3](https://docs.mesa3d.org/relnotes/22.1.3.html). Updates since then include *plenty* of bug fixes and new features, including Vulkan 1.3 support on lavapipe.

![mesa on steamos](/images/steam_deck/screenshots/mesa.jpeg)

This is just a small sampling of some of the more important packages on SteamOS that are in dire need of an upgrade. Apparently SteamOS hasn't been synced with the Arch repos [since January 27th](https://www.reddit.com/r/SteamDeck/comments/vszcq8/comment/if6zdip/) (though I can't confirm the legitimacy of this user). It's been kind for Valve to offer a desktop mode for the Deck, but it's something that they really need to keep up-do-date, even if the Deck's file system is immutable.

On a side note, there's also the fact that [you can't share, delete, or edit custom controller layouts](https://www.reddit.com/r/SteamDeck/comments/vszcq8/comment/if6zdip/). This has been reported back in April, and Valve has yet to respond. The number of games getting the Steam Deck verified/playable status has been [slowing down](https://boilingsteam.com/steam-deck-the-ratio-of-verified-titles-is-falling-whats-happening/) in recent months, though this could be perhaps because Valve is actually being more thorough with their verfication process. Finally, Valve really needs to get the [Steam Deck recovery image](https://help.steampowered.com/en/faqs/view/1B71-EDF2-EB6D-2BB3) available to platforms outside of the Steam Deck, and not leave it up to the community to add the tweaks for them.

# So, What Can We Do About This?
Well, it's kind of man-in-the-middle here, as even though technically you can install other distros on the Deck, a lot of them have that annoying problem of having the screen in portrait mode. Most of them don't have audio support, either, and getting the [Steam Deck UI to work](https://linuxgamingcentral.com/posts/steamdeck_ui/) can be a bit of a hassle. Even if you do get the Steam Deck UI to work, you probably won't be able to apply performance tweaks like maximum FPS, refresh rate, etc. (Believe me, [I know this](https://twitter.com/linuxgamingctr/status/1541801564700024833) from using the [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project/).) You really *should* be using the default SteamOS -- as Valve recommends -- for the best results, but now you're at their mercy when it comes to software updates. It's a bit of a frustrating pickle to be in.

![guix on steam deck](/images/steam_deck/photos/guix.jpg)
*Image credit: [podiki](https://mastodon.online/@podiki/107992944926127219)*

If you do want to use another distro though, I'd recommend either Nobara Project or [WinesapOS](https://linuxgamingcentral.com/posts/winesapos-3.1.1-released/). You can install these on a MicroSD card and boot that way, without harming your vanilla SteamOS install. Both distros feature much more up-to-date software. But they suffer some of the issues I explained earlier. [ChimeraOS](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/) could potentially become another option in the future, as the developers are actually considering [adding a desktop](https://strawpoll.com/polls/jVyGJ7bYPZ7).

As for Firefox, use the Flatpak version and avoid the stock version. Or better yet, you may want to avoid using Desktop Mode altogether, as a lot of the other packages can't be upgraded without unlocking the file system. Don't attempt to do so though; you could break your system (happened to me when I tried to install `mesa-git`).

Hopefully it won't be much longer before SteamOS gets updated. But be aware that for the time being, you should really be careful about using Desktop Mode.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
