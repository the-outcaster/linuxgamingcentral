+++
title = "ChimeraOS 33 Out Now, Adds Deck UI Bug Fixes"
date = 2022-05-23T21:54:25-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos_32/cover.svg"
tags = ["news", "software update", "chimeraos"]
keywords = ["chimeraos", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[ChimeraOS](https://chimeraos.org) version 33 has landed hot off the press today. The following software packages have been upgraded:
- kernel 5.17.9
- Mesa [22.0.4](https://docs.mesa3d.org/relnotes/22.0.4.html)
- Nvidia [515.43.04](https://forums.developer.nvidia.com/t/linux-solaris-and-freebsd-driver-515-43-04-beta/214143) (keep in mind this driver is in beta)
- [Chimera 0.14.6](https://github.com/ChimeraOS/chimera) (the web app that allows you to remotely install software to ChimeraOS)
- [steamos-compositor-plus 1.9.4](https://github.com/ChimeraOS/steamos-compositor-plus)
- RetroArch [1.10.3](https://retroarchofficial.itch.io/retroarch/devlog/370428/retroarch-1103-release)

This release also brings plenty of bug fixes, particularly when using the Steam Deck UI:
- fixed the session being reverted to Big Picture Mode after a recent Steam update
- fixed non-Steam games failing to launch
- fixed performance overlay
- fixed frame limiter
- fixed night mode
- fixed brightness controls
- fixed ChimeraOS release version not displaying
- fixed some minor graphical glitches

Keep in mind the Deck UI doesn't work on NVIDIA. You may also need to clear your customizations and re-run `chimera-session gamepadui` if you have manually switched to the new UI in a previous version, or have custom environment variables defined. There's a couple of other notes as well; have a look at the [patch notes](https://steamcommunity.com/groups/chimeraos/announcements/detail/3184619990168668901) for more info. Also, be sure to check out the [interview](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/) I had with the founder of the project last month.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
