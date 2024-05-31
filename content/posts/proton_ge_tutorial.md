+++
title = "Proton GE: What it is, Why it Should be Used, and How to Install"
date = 2022-03-21T08:55:20-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://cdn.cpnscdn.com/static.coupons.com/ext/kitchme/images/recipes/1200x800/chinese-egg-rolls_6281.jpg"
tags = ["guide", "proton ge"]
keywords = ["proton ge", "tutorial", "guide", "protonup-qt"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[Proton GE](https://github.com/GloriousEggroll/proton-ge-custom). You might have heard that name tossed around somewhere, maybe seen some benchmarks done with it, but don't know what it does. Well, this article will explain just that and the advantages it has over vanilla Proton. It also explains how to easily install it on your system and make use of it.

# What is it?
The "GE" in Proton GE stands for "Glorious Eggroll." Per the interview from [Boiling Steam](https://boilingsteam.com/learning-more-about-protonge-with-gloriouseggroll/), the name came about from the developer playing "off the card of being Asian and really liking eggrolls, and being a generally lighthearted person." The developer himself is an engineer at Red Hat.

Proton GE is essentially a bleeding-edge version of Proton. It includes the latest commits from such tools as [`wine-mono`](https://github.com/madewokherd/wine-mono), [`dxvk`](https://github.com/doitsujin/dxvk), [`vkd3d-proton`](https://github.com/HansKristian-Work/vkd3d-proton), [`dxvk-nvapi`](https://github.com/jp7677/dxvk-nvapi), and other pieces of software that make up Proton. Proton GE also includes [features and bug fixes](https://github.com/GloriousEggroll/proton-ge-custom#overview) that vanilla Proton does *not* have.

# Why use it?
Proton GE allows the user to make use of AMD's FSR feature to get better performance on lower resolutions while still retaining much of the same quality, and it also adds media foundation patches for better video playback support. Nowadays the regular version of Proton has incorporated media playback *for the most part*, but there's still the occasional splash screen or video on the title screen that shows up like this:

![color bar](https://images.huffingtonpost.com/2015-12-13-1450042661-3826208-ws_Color_Bars_2560x1440.jpg)
*Image credit: HuffPost*

Proton GE fixes that. It also allows certain games to run (or at least fix certain issues) that vanilla Proton can't, such as *Mortal Kombat 11*, *Killer Instinct*, *Cities XXL*, and others. This is in addition to a plethora of other features and bug fixes.

# How to install and use it
It's really not that difficult. First, make sure you have your Vulkan GPU drivers installed on your system. Check the documentation on the [Lutris GitHub](https://github.com/lutris/docs/blob/master/InstallingDrivers.md) to find instructions specific to your distribution and GPU vendor. For example, if you're using AMD or Intel on an Ubuntu-based distro, you would run this via the terminal:

`sudo add-apt-repository ppa:kisak/kisak-mesa && sudo dpkg --add-architecture i386 && sudo apt update && sudo apt upgrade && sudo apt install libgl1-mesa-dri:i386 mesa-vulkan-drivers mesa-vulkan-drivers:i386`

Chances are, if you've gamed on your desktop before, these drivers will already be installed, but it's a good idea to ensure your graphics drivers are up-to-date.

Now, there's a couple of different ways to download and install the latest version of Proton GE. The old-fashioned method would have you download the tarball from the [Releases](https://github.com/GloriousEggroll/proton-ge-custom/releases) section, extracting the contents to `~/.steam/root/compatibilitytools.d/`, then restarting the Steam client. That's certainly one way to do it, but the problem with that is it can be a bit cumbersome doing that over and over again whenever there's a new release. After a new release, hotfixes will generally get added a day or two later and that process will repeat a few times.

So we've got *tons* of ways to handle the download and automatic installation of Proton GE to make our lives easier. Here are a few tools that you can use:
- [Proton Community Updater](https://github.com/Termuellinator/Proton-Community-Updater)
- [Bash script by sirkhancision](https://github.com/sirkhancision/update-proton-ge)
- [Another bash script by jerluc](https://github.com/jerluc/proton-ge-downloader)
- [Yet another bash script by Ryan Walder](https://gitlab.com/ryanwalder/proton-ge-update)
- [ProtonUp - Python script](https://github.com/AUNaseef/protonup)

Among *many* others. Most of the aforementioned tools use the command line. Which is great if you want Proton GE installed with just a few keywords. But if you prefer a GUI, I highly recommend [ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt). That's what I'll be covering in this tutorial.

ProtonUp-Qt is available as an AppImage. Download [the latest release](https://github.com/DavidoTek/ProtonUp-Qt/releases), mark it as executable, then run it. Note that Steam Deck users can make use of this tool as well by downloading the Flatpak version from [Flathub](https://flathub.org/apps/details/net.davidotek.pupgui2). ProtonUp-Qt even has gamepad support, so no need to use the touchscreen or use the on-screen keyboard!

![protonup-qt main menu](/images/protonup-qt/menu.jpg)

ProtonUp-Qt supports light and dark themes. I personally prefer the dark theme so the app is easier on my eyes, but if you want to use the light theme to make the text easier to read, that's definitely an option. Just go to the "About" screen and change themes from there with the dropdown menu. Here you can also check to see if you have the latest version of the software.

![protonup-qt about](/images/protonup-qt/about.jpg)

You can see from the main menu I already have GE-Proton7-9 installed on my system. However, there's a new version available: [GE-Proton7-10](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-10). Let's walk through the process of obtaining the latest version.

First, ensure the `compatibilitytools.d` directory is properly set. In most cases it should be `~/.steam/root/compatibilitytools.d`. You probably won't even need to touch this, but if you do, just click the three-dotted button to the right of the dropdown menu and you can set the directory there. Click "Save" when done.

![protonup-qt custom install directory](/images/protonup-qt/custom_install_dir.jpg)

Back in the main menu, select "Add version" to install a new version of Proton GE. From here you can select what compatibility tool you want to install besides Proton GE: [Boxtron](https://github.com/dreamer/boxtron), [Luxtorpeda](https://github.com/dreamer/luxtorpeda), and [Roberta](https://github.com/dreamer/roberta). For simplicity's sake, we'll just cover Proton GE for this tutorial. Click the dropdown menu under "Version" to see the *long* list of Proton GE releases. By default the latest version should already be selected.

![protonup-qt choose compatibility tool](/images/protonup-qt/install_compat_tool.jpg)

If you click "Info" you'll be taken to that version's patch notes. Otherwise, click "Install" to download Proton GE and extract the tarball into the `compatibilitytools.d` directory. Now this version should be available from the main menu.

![protonup-qt downloading proton ge](/images/protonup-qt/downloading_proton_ge.jpg)

If Steam is running on your system, restart the client. Steam should now pick up the new version of Proton GE. From here you can enable the use of Proton GE globally by going to *Steam > Settings > Steam Play*. Check the box for "Enable Steam Play for all other titles" and select Proton GE from the dropdown menu. Click "OK" to save the changes, then restart the Steam client once more. All titles running through Proton will now use Proton GE.

![steam selecting proton version globally](/images/protonup-qt/enable_proton_ge_in_steam_global.jpg)

On the other hand, if you only want a specific set of games to use Proton GE, just right-click the game from your Steam library, click "Properties..." and on the *Compatibility* tab, check the box for "Force the use of a specific Steam Play compatibility tool" and select Proton GE from the dropdown menu. No restart of the Steam client required here.

![steam selecting proton version for a specific game](/images/protonup-qt/specific_game.jpg)

Back to ProtonUp-Qt, you can remove specific versions of Proton GE at will by selecting them from the main menu and clicking "Remove selected." You can double-click an item from the list (or click "Show info") and see what games from your Steam library are using that version of Proton GE. Double-click a game and you will be brought to the Steam store page for it. Click "Batch update" to switch the game list to use a different compatibility layer or version of Proton GE.

![protonup-qt batch conversion](/images/protonup-qt/about_compat_tool.jpg)

From the main menu you can also see all the games installed in your Steam library by clicking "Show game list." Now you can take a glance at what versions of Proton or Proton GE your games are using (unless they're native), and from the dropdown menu you can easily switch what version of Proton you want the game to use. It's a neat alternative in case you don't want to use Steam's interface to do the same thing.

![protonup-qt game list](/images/protonup-qt/game_list.jpg)

If you want to **make use of FSR**, regardless of what GPU vendor you have, go to the Steam launch parameters for your game and add this:

`WINE_FULLSCREEN_FSR=1 %command%`

Then adjust the resolution when in-game until you can strike a good balance between performance and graphics quality. For instance, if you have a 1080p screen, you could downscale the game to 720p and still (probably) retain most of the same quality, albeit for textures that are far away. This is incredibly useful in a day and age where GPUs cost a small fortune, while still making good use out of your older GPU/CPU.

ProtonUp-Qt works with more than just Steam. You can also download and install [Wine-GE](https://github.com/GloriousEggroll/wine-ge-custom) for Lutris, and install custom versions of Wine and Proton GE for the [Heroic Games Launcher](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher). That's outside the scope of this guide though.

# What to be aware of when using Proton GE
The developer of Proton GE is not affliated with Valve. The compatibility layer is developed in his spare time. He is not under obligation to fulfill anyone's specific requests. So here's a couple of things to keep in mind:
- Proton GE is built specifically for Steam games. If you want to use Proton GE outside of Steam (for example, for Lutris), use [Wine GE](https://github.com/gloriouseggroll/wine-ge-custom) instead
- Proton GE-specific bugs should be reported on the project's [Discord channel](https://discord.gg/6y3BdzC), not on Valve's issue tracker
- Support from the developer is not available for those who use the Flatpak or AUR versions of Proton GE (although you could probably get unofficial support from the maintainers of those versions)
- If you like what the developer does, you can support him via [Patreon](https://www.patreon.com/gloriouseggroll)

That should wrap this guide up! Any questions, let me know in the comments or [get in touch](https://linuxgamingcentral.com/contact).

*Cover image credit: KitchMe*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
