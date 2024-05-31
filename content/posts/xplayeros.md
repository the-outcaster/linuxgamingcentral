+++
title = "xPlayerOS - Automated Script for Onexplayer Handhelds"
date = 2022-03-08T07:50:47-05:00
author = "Mark Dougherty"
authorTwitter = "" #do not include @
cover = ""
tags = ["xplayeros", "oxp", "onexplayer", "intel"]
keywords = ["onexplayer", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
One of the contributers for the [ChimeraOS](https://chimeraos.org) distribution got in touch with me yesterday and sent a link to his GitHub project: [xPlayerOS](https://github.com/ruineka/xPlayerOS). This is a couple of bash scripts to help those who have an [Intel-based Onexplayer](https://onexplayerstore.com/products/new-onexplayer-mini-intel-i7-1195g7) handheld get everything they need to get set up and running on Linux. The README mentions the script was specifically tested on Pop!_OS 21.10, but it should theoretically work across any Ubuntu-based distro, and maybe even Debian.

When running the `xPlayerOS_Installer.sh` script, the user has the option of adding the new Steam interface designed for the Steam Deck, gamescope, and mangohud. These are in addition to getting patched Mesa drivers to fix graphical issues on Intel and get the Onexplayer's buttons to actually work (because apparently they don't work otherwise). Just clone the repository, mark the script as executable, run it through a terminal, and you're good to go.

![oxp steam deck ui](https://user-images.githubusercontent.com/101111355/157039190-efc12f3d-d2e2-49bc-bb5a-f2d899589c65.jpg)

The `SteamOSUI_ENABLE.sh` script will transform Pop! OS (or whatever distro you're running) into a console-like experience. It just boots to Steam with the new Steam Deck interface. However, it's not recommended, as the writer of the script says he experienced touchscreen issues, and is unable to use the desktop. Once this script is run and you no longer wish to use it, simply run the `SteamOSUI_DISABLE.sh` script.

Pretty neat to see the community getting together to make gaming on Linux (specifically handhelds in this case) easier. I haven't tested the script myself but I'm thinking it might work on the [GPD Win 3](https://boilingsteam.com/gpd-win-3-the-tide-me-over-for-the-steam-deck/) as well, since it's basically using the same processor as the OXP (i7-1165G7 vs. i7-1195G7). And the beauty of open-source is, if the script doesn't work or you want to make enhancements to it, you can just grab the scripts, fork them, then create a pull request.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
