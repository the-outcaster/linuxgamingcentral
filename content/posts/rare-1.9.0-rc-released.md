+++
title = "Rare (Epic Games Store Client) 1.9.0 RC 1 Released, Adds Plenty of Bug Fixes"
date = 2022-08-30T22:08:12-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/rare/cover.jpg"
tags = ["news", "software update", "rare"]
keywords = ["rare", "epic games store launcher"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
While [Heroic Games Launcher](https://linuxgamingcentral.com/posts/heroic-games-launcher-2.4.0-released/) is a great Epic Games Store client for Linux, there's another: [Rare](https://github.com/Dummerle/Rare). Unlike Heroic, Rare is written in Python and does *not* use Electron as its base, thus saving your computer precious RAM.
Quite a few new things released in this update, including a Settings for Epic Games Overlay, plenty of UI fixes, general bug fixes and typos corrected, and *plenty* of other features. Changelog is as follows:

- Add Settings for Epic Games Overlay by @Dummerle in #156
- Clarify about submodules when running from source by @MultisampledNight in #159
- Implement logging in via webengine by @invertedEcho in #160
- Got color schemes working by @KovvalskiX in #161
- Unify strings formatting by @invertedEcho in #158
- Remove leftover + from f-string refactor which breaks Proton settings saving by @MultisampledNight in #162
- UI fixups for InstallDialog and LegendarySettings by @loathingKernel in #166
- Add "Categories=Game;" in desktop entries by @ZhaoZuohong in #169
- Implement global objects as functions that return a single instance by @loathingKernel in #175
- RareStyle: Update QProgressBar and QScrollBar by @loathingKernel in #185
- SideTabWidget: Add master widget with a title and a scrollarea by @loathingKernel in #187
- Wrappers: Make widgets and the scrollarea smaller by @loathingKernel in #188
- Implement environment variables by @invertedEcho in #180
- Change some settings by @Dummerle in #189
- A bunch of minor UI fixes by @loathingKernel in #194
- Use QStandardPaths everywhere instead of guessing desktop and applications path by @MultisampledNight in #195
- Implement moving game installations by @invertedEcho in #193
- Fix uninstall for third party launcher games by @invertedEcho in #200
- Focus on what makes Rare a good choice by @loathingKernel in #201
- Add a bunch of accumulated fixes. by @loathingKernel in #203
- Fix typo by @invertedEcho in #204
- Add max shared memory override and download reordering options by @loathingKernel in #207
- Update move game to support moving across different drives by @invertedEcho in #199
- Add game helper to launch games in a detached process by @Dummerle in #202
- Split resources into base and themes to make diffs lighter by @loathingKernel in #212
- Implement image manager by @loathingKernel in #211
- Add ImageWidget and LibraryWidget from #196 by @loathingKernel in #213
- LibraryLayout from #196 by @loathingKernel in #214
- Small enhancements in moving game by @invertedEcho in #215
- ImageManager: Handle broken image.cache by @loathingKernel in #216
- Fix typo and add flatpak to README.md by @invertedEcho in #217
- Add SlidingStackedWidget from #196 by @loathingKernel in #218
- Bug fixes for merged features by @loathingKernel in #220
- Some more fixups by @loathingKernel in #221
- Don't double delete the game dir by @invertedEcho in #223
- Fix get_rare_executable func for macOS by @invertedEcho in #224
- Fixups by @loathingKernel in #225
- Fixups by @loathingKernel in #228
- ImageManager: Also test if 'game.metadata' has 'keyImages' by @loathingKernel in #230
- Implement shim legendary classes with overloaded/modified functions by @loathingKernel in #197
- Install advanced options by @Dummerle in #233
- InstallDialog: Adjust collapsible widget by @loathingKernel in #234
- Lgndr: Temporary fix for DLManager monkeypatching in Windows by @loathingKernel in #235

Hopefully when the release becomes official the patch notes will be a little more organized by category.

You can get the AppImage on [GitHub](https://github.com/Dummerle/Rare/releases/tag/1.9.0-rc.1). You can also get Rare on [Flathub](https://flathub.org/apps/details/io.github.dummerle.rare) for you Steam Deck owners out there; just be aware the Flatpak is using version 1.8.9 at the time of writing this.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
