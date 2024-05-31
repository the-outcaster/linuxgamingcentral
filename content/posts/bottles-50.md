+++
title = "Bottles 50 Adds GameScope Improvements, Enables VKD3D in the Gaming Environment"
date = 2023-01-16T03:38:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/bottles/screenshot.png"
tags = ["news", "software update", "bottles"]
keywords = ["bottles", "wine", "bottles application"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As is typical around the 14th of each month, Bottles gets a new release. Seems like they're adopting a new naming scheme. Instead of going by year/month/day, it's now just one number. I'm guessing "50" indicates that this is the 50th update.

Beside that, here's the changes:

**Features**
- support userdir/ placeholder for installers checks
- enable VKD3D in the Gaming environment
- async fetch of components, installers and dependencies

**Frontend**
- GameScope improvements
- updated link for connection checking
- improve sentence in installers
- smoother UI with async code
- make app name untranslatable, disambiguate Bottles & bottles
- remove FileChooser class
- port primary menu to MenuModel

**Backend**
- improve health check
- add `import_bundle` on dependency installation

**Fixes**
- fix typos in strings and update translations
- dependency replace_font step
- create_bottle_from_config() nvapi check
- ComponentManager.install() deadlock
- wrong exception catching using pycurl
- slow replace_font
- replace spin-lock with threading.Lock
- being able to use local repos with pycurl
- onboard dialog shows "All ready" when not ready
- Bottles crash if bad encoding in Steam file
- components not updating when install in UI
- FSR-related issues
- wrong call to update_programs()
- hint texts
- add dest to cabextract on local files
- wrong combo selected for VKD3D
- broken back button if DXVK and VKD3D are disabled
- nvngx.dll not copied under Flatpak, UI consistency
- add runner libs to fix embedded GStreamer not finding them

**Other**
- translations update
- remove JSON manifest
- improve check_runners() log
- updated and improved packaging
- contributing info updated
- don't override `GST_PLUGIN_SYSTEM_PATH` if runner doesn't bundle GStreamer
- dynamic length of progress bar according to terminal size
- Addresses bug from patoolib
- make VKD3D not enable-able without DXVK

Not too long afterwards [50.1](https://github.com/bottlesdevs/Bottles/releases/tag/50.1) released with a fix for the library not getting updated when renaming a bottle, as well as a critical error when not using a NVIDIA GPU.

Special thanks to **StoneMoe, koplo199, underlinejakez, SuperSamus, dkeruza-neo, TheEvilSkeleton, kbdharun, weblate, francescomasala, Kinsteen, and jannuary** for making this release possible!

See the patch notes on [GitHub](https://github.com/bottlesdevs/Bottles/releases/tag/50).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
