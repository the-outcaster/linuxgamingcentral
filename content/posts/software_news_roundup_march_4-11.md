+++
title = "Your Weekly Software Release News for March 4-11 (Heroic Now On Flathub!)"
date = 2022-03-11T10:06:12-05:00
author = "Mark Dougherty"
authorTwitter = "" #do not include @
cover = "https://www.srb2.org/wp-content/uploads/srb2-title.png"
tags = ["foss", "linux gaming updates"]
keywords = ["foss", "software releases"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I think I will set Friday as a day to cover the various software updates that have come to Linux (particularly gaming-related) during the week.

A noteworthy mention is **Heroic Games Launcher**. Not only has the launcher received gamepad support, but the app is now available on [Flathub](https://flathub.org/apps/details/com.heroicgameslauncher.hgl). This is big news for those of you who have a Steam Deck, as the Deck only has support for Flatpaks. Combined with the gamepad support, now you'll have almost the same seamless integration as Steam.

As for the latest version released, it's currently [2.2.6](https://github.com/Heroic-Games-Launcher/HeroicGamesLauncher/releases/tag/v2.2.6) that comes with a ton of hotfixes for the Flatpak. Liam from GamingOnLinux has a video guide on installing the Heroic app on the Deck; click the thumbnail to watch it.

[![Heroic on Deck](https://img.youtube.com/vi/HrTg0mDm2nA/0.jpg)](https://youtu.be/HrTg0mDm2nA "Playing EGS games on Deck")

Next up is **Discover**, a Discord overlay for Linux written in Python. Just a few hours ago [v0.4.3](https://github.com/trigg/Discover/releases/tag/v0.4.3) was released, and this version contains the following changes:
- Added a link to our Discord Channel for support and development chit chat.
- Added an "about" landing page on initial application launch
- Enforced --configuration flag when using Gamescope
- Enforced Nightmode
- Allow closing of overlay from about screen
- added --nolock option for containerised running
- Ignore floating mode in Gamescope for now
- Enforced 1280 x 800 resolution in Gamescope mode
- Omit encoding to avoid crashing some machines
- Caught a file not found error
- Removed text overlay in Gamescope... for now.
- Set sane default values
- Updated the README with more information about what the project is.
- Added a /s flag to the README

![discord overlay in action?](https://user-images.githubusercontent.com/535772/149630830-750f8af6-e935-44a6-ad1c-da1d204ee107.png)

AMD and Intel users will particularly benefit from the new **Mesa 22** drivers. This includes support for the new Vulkan 1.3 release, Alder Lake N support, adaptive-sync/VRR support for Intel's graphics drivers, better performance for Radeon VCE video encoding, support for new extensions, performance optimizations, and even more. Check [Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=Mesa-22.0-Released) for the summary of noteworthy features.

**VKD3D-Proton** was updated to version [2.6](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.6). This release has several fixes for such games as *Horizon Zero Dawn*, *Final Fantasy VII Remake*, *Warframe*, *Guardians of the Galaxy*, *Elden Ring*, and *Age of Empires: IV*. CPU overhead for "descriptor copy operations" has been "greatly" reduced. Loads times for *Monster Hunter: Rise* have been drastically reduced. *Guardians of the Galaxy* and *Elden Ring* should also be able to benefit from reduced load times. Some workarounds have been made for *Deathloop* on RADV, *Elden Ring*, *Horizon Zero Dawn* (glitched foliage), and "some questionable UE4 shaders."

The patch notes mention that starting with the next `vkd3d-proton` release, **it's going to need newer Vulkan extensions**. `vkd3d-proton` 2.6 should be available in Proton Experimental.

That same day, **DXVK** was also updated to [v1.10](https://github.com/doitsujin/dxvk/releases/tag/v1.10). This brings performance improvements, particularly for *Assassin's Creed: Origins*, *Elex II*, *God of War*, *GTA IV*, some of the *Resident Evil* titles, *Total War: Warhammer III*, and *Quantum Break*. Fixes were added for *ArmA 2* and *Black Mesa*. Some workarounds were made for *Age of Empires 2: Definitive Edition*, *Anno 1800*, *Final Fantasy XIV*, *Nier Replicant*, and *The Evil Within* -- these games were replaced with `d3d11.cachedDynamicResources` rather than `d3d11.apitraceMode`, "which provides a more granular way to specify resource types to allocate in cached system memory."

As with `vkd3d-proton` 2.6, this `dxvk` release should also be available in Proton Experimental.

**Proton Experimental** was [updated](https://github.com/ValveSoftware/Proton/wiki/Changelog/_compare/cf04f8d6059708450bbbc1f8b1d4293da363d931...24c430ae5584a0ed0fd79ad43ad6c1ab00bd9ee8) yesterday, which allows *A Way Out* to run. There's also the following:
- Fix garbled videos in *Rustler*.
- Fix *VR Chat* not handling suspend / resume well.
- Fix *Vampyr* and *The Beast Inside* displaying menus a few pixels wide on Steam Decks.
- Fix *Apex Legends* sometimes starting minimized on Steam Decks.
- Fix *Quake Live* being unable to connect to multiplayer matches.
- Fix *Killing Floor 2* not connecting to the item server.
- Fix Xbox login window lagging with updating window's content.
- Update dxvk-nvapi to [v0.5.3](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.5.3).

**Bottles** -- an application that allows you to easily manage wineprefixes -- has seen a few releases over the past week. The latest at the time of writing this -- [2022.2.28-trento-4](https://github.com/bottlesdevs/Bottles/releases/tag/2022.2.28-trento-4) -- contains the following bug fixes:
- Fixed a bug with Wine-GE runners, was using the wrong path for the binaries
- Fixed a regression with offline mode
- Fixed a bug with installers, was silently failing if checksum mismatch
- Fixed a regression with Bottles CLI, programs with a Windows path did not run

![bottles screenshot](https://raw.githubusercontent.com/bottlesdevs/Bottles/master/screenshot.png)

Liam has a [guide](https://www.gamingonlinux.com/2022/03/heres-how-to-get-the-ea-app-on-steam-deck-with-bottles/) if you want to install Origin on the Deck with Bottles.

**ProtonUp-Qt** -- basically what ProtonUp does, which fetches the latest version of Proton GE for you, except this provides a GUI -- was updated to [v2.6.0](https://github.com/DavidoTek/ProtonUp-Qt/releases/tag/v2.6.0). In it we see new language support, including German, Finnish, and Spanish translations, and there's also a game list dialog that's been added.

![ProtonUp-Qt GUI](https://user-images.githubusercontent.com/54072917/142935052-5d627e22-dc1a-4d31-9189-288b41022534.png)

**Blender** was updated to 3.1. There's *way* too many changes to highlight here; have a look at the [patch notes](https://wiki.blender.org/wiki/Reference/Release_Notes/3.1) if you'd like to learn more. Or click the thumbnail below.

[![blender 3.1](https://img.youtube.com/vi/BCi0QRM1ADY/0.jpg)](https://youtu.be/BCi0QRM1ADY "Blender 3.1 - What's New?")

As for open-source games, **fheroes2** (*Free Heroes of Might and Magic II*, an open-source re-implementation of the *HoMM2* engine) saw [v0.9.13](https://github.com/ihhub/fheroes2/releases/tag/0.9.13), which brings improved AI behavior, fixes for music and sound effects, a text support mode to help those who are visually-impaired to play the game, scalable scrollbars, Czech translation, over 50 bug fixes from the last release, and a few other features.

![fheroes2 screenshot](https://github.com/ihhub/fheroes2/raw/master/docs/images/screenshots/screenshot_battle.png?raw=true)

**Sonic Robo Blast 2 (SRB2)** -- a fan Sonic the Hedgehog game -- was updated to [v2.2.10](https://github.com/STJr/SRB2/releases/tag/SRB2_release_2.2.10). File limit has been increased, the tutorial was re-done for the new default controls, an improved input library, folders can now be loaded for easier add-on development, updated graphics, and plenty of bug fixes. The game is available as a Flatpak too, so you can easily install it on your Deck.

![SRB2 splash](https://www.srb2.org/wp-content/uploads/srb2-title.png)

For *new* FOSS projects, we now have [**GameStudio 2D**](https://github.com/ensisoft/gamestudio). As the name implies, it's a 2D game engine and editor for Linux, Windows, and even HTML5. There's a *ton* of documentation on the project's README if you want to get started.

![GameStudio 2D in action](https://github.com/ensisoft/gamestudio/raw/master/screens/bandit-play.gif)

Valve has [open-sourced](https://gitlab.steamos.cloud/devkit) their **SteamOS devkit client for the Steam Deck**.

![deck devkit](https://uploads.golmedia.net/uploads/articles/article_media/17884472051646412394gol1.jpg)

Not a software release, but today, [Arch has turned 20 years old](https://archlinux.org/retro/2002/). Amazing; I never knew it was around that long.

I think that's *most* of it. Probably some other stuff I failed to mention. But even this list is pretty massive for just a week's worth of updates.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
