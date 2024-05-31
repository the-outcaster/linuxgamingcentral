+++
title = "Easily Install Super Mario 64 (PC Port) and Ship of Harkinian on Steam Deck with These Scripts"
date = 2023-12-22T20:15:39Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/sm64/cover.jpg"
tags = ["script", "super mario 64", "zelda", "ship of harkinian", "steam deck"]
keywords = ["super mario 64 pc port", "zelda ocarina of time", "ship of harkinian", "ship of harkinian on steam deck", "super mario 64 on steam deck", "steam deck"]
description = "All you need are your legally-dumped ROMs."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Over the past several days I've actually had some fun writing up some bash scripts. In addition to making it very easy to [overclock the GameCube controller adapter](https://github.com/linuxgamingcentral/gcadapter-oc-kmod-deck), I've also made it easy to install the [PC port of *Super Mario 64*](https://github.com/linuxgamingcentral/sm64-steam-deck-builder) as well as [Ship of Harkinian](https://github.com/linuxgamingcentral/ship-of-harkinian-updater) on Deck.

# Super Mario 64 PC Port (ROM required)
Let's start with the *Super Mario 64* script. In addition to the original PC port, you can download several forks that enhance the overall gameplay. For example, with SM64Plus, there's an improved camera, more responsive controls, more movesets, 60 FPS support, as well as the ability to continue a level after getting a star. Render96 will essentially turn the game into an HD remake, improving the detail on Mario's model as well as the in-game textures.

To get the script running on Deck, go to the [GitHub page](https://github.com/linuxgamingcentral/sm64-steam-deck-builder) in Desktop Mode with your web browser. Just like you would with Decky Loader or CryoUtilities, just right-click the download link, click "Save link as..." then save it to your desktop. Double-click the file to download and run the script.

![SM64 Steam Deck builder - main menu](/images/steam_deck_oled/sm64/sm64.png)

Forks can also be seamlessly updated and uninstalled, and you can adjust the various options that come with each one with a text editor. Eventually I want to make an easy-to-use GUI to edit the config options, but for now, the script will just open the configuration file with your default text editor. Save files can be backed up, and high-resolution textures can also be downloaded and installed.

There is an option with each fork to add said fork as a non-Steam shortcut, but this is a bit buggy right now. You may have to just manually add the executable to Steam in the meantime.

All you need to get the script running is to have your legally-dumped ROM inside of your `home` folder. Name it to `baserom.us.z64` (or change the "us" part to "jp" or "eu" if the ROM is from a different region). The script will look for this file. If it can't detect the ROM, the script will exit.

Please note that, since each fork has to be compiled manually, you'll need to install the appropriate developer tools. Just head into the Options menu and select "DEPENDENCIES" to install the Arch dependencies for Steam Deck. You'll need to enter your sudo password for this. After this option is run, you shouldn't need to run it again, until Valve ships a new update to SteamOS.

# Ship of Harkinian (ROM required)
The Ship of Harkinian Updater works similarly to the *Super Mario 64* script. Go to the [GitHub page](https://github.com/linuxgamingcentral/ship-of-harkinian-updater), right-click the download link, and save the link to your desktop.

![Ship of Harkinian Updater - main menu](/images/steam_deck_oled/sm64/soh.png)

SoH can be downloaded, updated, and uninstalled. The changelog can also be viewed with your web browser, and you can visit my [ROM dumping guide](https://linuxgamingcentral.com/posts/ship-of-harkinian-steam-deck-guide/) if you need to get that set up. Steam Deck-specific mods can be downloaded, such as the Steam Deck UI and boot logo, and you can also download high-res textures or the textures from the 3DS version.

Put your legally-dumped ROM inside of `~/Applications/ship-of-harkinian/` and name it to `zelda64.z64`. If the script can't find this, it will prompt you to select it with a file browser.

Give each script a try and tell me what you think!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
