+++
title = "Use Native Linux Game Engines with Luxtorpeda"
date = 2022-07-11T15:00:43-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/oceans_heart.webp"
tags = ["guide", "steam deck", "luxtorpeda", "native"]
keywords = ["steam deck", "luxtorpeda"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) is a Steam Play compatibility tool for allowing a certain set of games on Steam (mostly pertinent to older titles) to run using a native Linux engine, rather than having to use Proton for a Windows-only game. For instance, *Ocean's Heart* has a Windows-only icon on the [Steam store page](https://store.steampowered.com/app/1393750/Oceans_Heart/). But with Luxtorpeda, we can force the game to use the native Linux version of [Solarus](https://gitlab.com/solarus-games/solarus), the engine that powers the game.

So why would we use something like Luxtorpeda? It's because the Linux engines are more up-to-date and dramatically improve the overall compatibility of the game. Older games are able to more easily work on modern platforms, such as the Steam Deck, thanks to newer features.

![Ocean's Heart running natively on Deck](/images/steam_deck/screenshots/luxtorpeda/oceans_heart.jpeg)

Be aware that Luxtorpeda does *not* work with every game. There's a list of compatibile titles [here](https://luxtorpeda-dev.github.io/). Currently there's over 140 titles that work with Luxtorpeda, ranging from *Aliens versus Predator Classic*, some of the older *Elder Scrolls* games, *Beneath a Steel Sky*, *Cave Story+*, *DOOM 3*, *Duke Nukem 3D*, *Ion Fury*, *Quake*, *Star Wars: KOTOR*, *Thimbleweed Park*, the classic *Tomb Raider* series, *Wolfenstein 3D*, and *plenty* of others. More will get added over time. If you want to help contribute for another game to work, you can either create an [issue](https://github.com/luxtorpeda-dev/packages/issues) on the project's GitHub page, or try [making the package yourself](https://github.com/luxtorpeda-dev/packages/blob/master/docs/Creating_a_Package.md).

Though this tutorial is primarily aimed for Steam Deck owners, the process is fairly similar to those on desktop.

## How to Install and Use Luxtorpeda on Deck
The easiest way we can make use of Luxtorpeda on Deck is by using a tool called [ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt). ProtonUp-Qt not only includes the easy installation of Luxtorpeda; it can also download and install other Steam Play compatibility tools, such as GE-Proton, Boxtron, and Proton Tkg. And even better is the fact that the application is available on Flathub, making installation on Deck fairly trivial. Simply head over to the Discover app while in Desktop Mode, search for ProtonUp-Qt, and install it. Alternatively you can install the app via the command line with this:

`flatpak install flathub net.davidotek.pupgui2`

After the app has been installed, look for it in the panel on the lower-left of the desktop. The installation directory should already be set in the window that opens; if it's not set, click the three-dotted button and set the path from there. By default it would be `/home/deck/.local/share/Steam/compatibilitytools.d/`. Click "Add version" in the main window, and in the new window that opens, select "Luxtorpeda" from the dropdown menu for Compatibility tool. Leave "Version" set at it's default choice (at the time of writing this Luxtorpeda is version 55). Simply click "Install," let the compatibility tool download, and it will be extracted into the `compatibilitytools.d/` directory. 

![installing luxtorpeda via protonup-qt](/images/steam_deck/screenshots/luxtorpeda/adding_luxtorpeda.jpeg)

Now go back to Gaming Mode, and Luxtorpeda should now be available as an option when forcing a game to use a specific Steam Play tool. In the case with *Ocean's Heart*, I would go to my Steam library, look for the game, press Start, then go to Properties. Under the Compatibility tab on the left, check the box for "Force the use of a specific Steam Play compatibility tool." In the dropdown menu that now appears below it, select "Luxtorpeda" from the list. 

![forcing luxtorpeda as a compatibility tool](/images/steam_deck/screenshots/luxtorpeda/forcing_luxtorpeda_on_steam.jpeg)

The game may take a few seconds to update, as it needs to download the appropriate engine for the game. You should now be able to play the game with a native Linux engine! It's as easy as that. Gamepad buttons should work out-of-the-box with Steam Input.

Note that some games may prompt you for what engine you want to use, as they are compatibile with multiple engines. In the case with *Sega Genesis Classics*, if you try to run the game with Luxtorpeda, you will be prompted for what game you want to run. You can navigate across the options with the D-pad, then press A to run the game/engine. You can also press Y to set that engine as the default, thus eliminating the prompt every time you run the game. If you want the prompt again, you can simply delete the `default_engine_choice.txt` file found in `~/.config/luxtorpeda/<app id>/` while in Desktop Mode.

![sega genesis classics engine selection](/images/steam_deck/screenshots/luxtorpeda/engine_selection.jpeg)

If you'd like to learn more about the project, you can view the README file on the project's [GitHub](https://github.com/luxtorpeda-dev/luxtorpeda), or you can read the article over on [GamingOnLinux](https://www.gamingonlinux.com/2022/03/steam-deck-using-luxtorpeda-for-morrowind-warzone-2100-and-x-com/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
