+++
title = "Bottles 51 Gets Revamped Bottle Dialog, Adds Toast for 'Run Executable'"
date = 2023-02-20T19:15:04Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/bottles/2022.11.14.png"
tags = ["news", "software update", "bottles"]
keywords = ["bottles", "bottles 51", "bottles 51.0"]
description = "This, along with several bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Lots of bug fixes with this release of Bottles. Not too much going on in the features department, although the New Bottle dialog got revamped.

Patch notes are as follows:

**Frontend**
- frontend: Replace emote-love with library icon by @TheEvilSkeleton in #2502
- frontend: Remove Create a Bottle description by @TheEvilSkeleton in #2541
- frontend: Ability to name the Bottle with special characters + duplicate bug fix by @Kinsteen in #2538
- frontend: Fix various library crashes and empty library items by @Kinsteen in #2539
- frontend: Gracefully handle ridiculous names by @jannuary in #2673
- frontend: Add toast for "Run Executable" by @TheEvilSkeleton in #2614

**Fixes**
- fix: Fix GTK critical error at startup by @Kinsteen in #2560
- fix/urgent: downloads not working if no terminal attached by @Kinsteen in #2564
- fix: remove add to library button if already in library by @Kinsteen in #2561
- fix incorrect text codec detection by @StoneMoe in #2585
- fix: Fix patool double extracting when not needed by @Kinsteen in #2591
- fix: Invert get_file() and get_path() by @TheEvilSkeleton in #2625
- fix: Error when adding shortcut to Steam by @Kinsteen in #2589
- fix: Create bottle crashing if no Nvidia GPU and NVAPI installs by @Kinsteen in #2607
- fix: Properly set paths for launch options dialog by @TheEvilSkeleton in #2695
- fix terminal download progress crash by @StoneMoe in #2662
- fix inconsistent return type for WineCommand by @StoneMoe in #2658

**Other**
- Translations update from Hosted Weblate by @weblate in #2533, #2545, #2577, #2586, #2610, #2611
- Update translation files by @flipflop97 in #2656
- misc: Use media types instead of patterns by @TheEvilSkeleton in #2467
- misc: Update issue forms by @TheEvilSkeleton in #2550
- misc: Add information using bottles-cli by @TheEvilSkeleton in #2643
- code: Add Pylint GitHub Actions against PRs by @Kinsteen in #2556
- code: better Pylint by @Kinsteen in #2590
- flatpak: Remove Pillow by @jannuary in #2672
- Network issue template by @StoneMoe in #2588
- Migrate Config from dict to object by @StoneMoe in #2464
- Add GitHub Action close issues if people are using a too old version by @Kinsteen in #2598
- Remake New Bottle dialog by @TheEvilSkeleton in #2505
- Make sure ListView gets updated properly when deleting a bottle by @cyberphantom52 in #2596
- Don't enable Steam Runtime when switching to wine-ge-proton by @SuperSamus in #2593

See the patch notes on [GitHub](https://github.com/bottlesdevs/Bottles/releases/tag/51.0).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
