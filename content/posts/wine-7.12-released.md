+++
title = "Wine 7.12 Released, Upgrades VKD3D to 1.4 and Adds Theming Support for Qt5 Apps"
date = 2022-07-01T23:19:32-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/7.12.jpeg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "crossover", "codeweavers", "proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 7.12 released earlier today. Here's the changelog:
- Theming support for Qt5 applications.
- Bundled vkd3d upgraded to version 1.4.
- Improved effect support in Direct2D.
- QWORD support in registry tools.
- Various bug fixes.

A total of 13 bugs were fixed, including:
- Star Citizen: No mic input audio (used for voip)
- StarCitizen launcher crashes on start with a winmm error
- Shogun Total War 2 crashes on start up. (Main Application.)
- Approach (Smart Suite) crashes when trying to print to cups-pdf
- Argentum 20 RPG Launcher has graphical glitches
- Incorrect display of selected buttons in Light theme.
- Wireshark shows black rectangle on various places if light theme is enabled
- MetaTrader4 stopped working properly with wine 7.10
- Rich edit control becomes unstable or trips assertion after ITextRange::SetFont is called
- Rich edit control becomes unstable or trips assertion after changing TextFont properties
- aria2 needs QueryContextAttributes(SECPKG_ATTR_CIPHER_INFO) to return a valid version
- The 32-bit evr:evr crashes almost systematically on the TestBot's Wine VMs
- The 32-bit mfplat:mfplat crashes on the TestBot debian11 VM

See the patch notes over on [WineHQ](https://www.winehq.org/announce/7.12).

*Cover image credit: foodandwine.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
