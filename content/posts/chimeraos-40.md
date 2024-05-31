+++
title = "ChimeraOS 40 Adds Support for Super Game Boy and Atari 7800, Better Steam Deck Support"
date = 2023-03-30T03:14:32Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/distro_reviews/chimeraos/sonic_3_air.jpg"
tags = ["news", "software update", "distro update", "chimeraos"]
keywords = ["chimeraos", "chimeraos 40", "chimeraos steam deck", "chimeraos aya neo"]
description = "Aya Neo 2/Geek also get full controller support."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Sweet new update out for the lovely [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos) distribution. Here we've got out-of-the-box audio support for the Steam Deck, full gamepad support for Aya Neo 2/Aya Neo Geek, the ability to use Xorg in Desktop Mode, automatic wake on USB, automatic disk mounting, and a few other changes.

Main software updates are as follows:
- kernel upgraded from 6.1.11 to [6.1.21](https://lwn.net/Articles/926872/)
- Mesa upgraded from 22.3.4 to [23](https://docs.mesa3d.org/relnotes/23.0.0.html). Gamescope has supposedly been patched with ANV compatibility for Intel users
- NVIDIA driver upgraded from 525.89.02 to [530.41.03](https://www.nvidia.com/download/driverResults.aspx/200481/en-us/)

New features:
- support for [Super Game Boy](https://en.wikipedia.org/wiki/Super_Game_Boy) and [Atari 7800](https://en.wikipedia.org/wiki/Atari_7800) have been added via the Chimera web app
- Aya Neo 2 and Aya Neo Geek now have full gamepad support
- in Desktop Mode, you can now use Xorg
- GOG games can have their executable file overridden. And apparently *WarCraft II* works now

Fixes:
- Steam Deck should now properly boot and have working audio
- disks should now be automatically mounted in Desktop Mode
- session changes persist after reboot
- game config tweaks should now properly be applied on first boot

Other changes:
- PS2 titles now use the PCSX2 core  -- **BIOS now required**
- network timeouts have been reduced in the game config downloader "to avoid connection hangs in poor network conditions"
- wake on USB automatically enabled when a gamepad is connected

But here's an important tidbit: the patch notes urge the user to **"upgrade to ChimeraOS 40 as soon as possible."** Previously, ChimeraOS used the syslinux bootloader. Kernel 6.2 seems to have deprecated syslinux (although, this change might not have been intentional). Therefore, in order for ChimeraOS to move to this kernel, the distro had to switch to systemd-boot. Version 40 has the migration framework in place, so if the user doesn't upgrade to this release, their system will be borked if they try to upgrade to 41, because the migration work isn't in place with any version prior to 40.

Also, note that with the change to systemd-boot, **BIOS/legacy installs will no longer work.**

See the patch notes on [GitHub](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-40-2023-03-29). And be sure to check out the [review](https://linuxgamingcentral.com/posts/chimeraos-review/) I wrote earlier this month.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
