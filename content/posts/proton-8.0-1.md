+++
title = "Proton 8.0-1 Released, Adds Compatibility to Dozens of New Titles, Improves Sleep/Resume Functionality on Deck"
date = 2023-04-17T23:46:59Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton/8.0-1.jpg"
tags = ["news", "software update", "proton"]
keywords = ["proton", "proton 8.0-1", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "wine 8.0", "forspoken", "dead space remake", "steam deck", "gnome 43", "final fantasy xiv"]
description = "Plus 17 bug fixes!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Well, we were kind of hit with this *massive* update to Proton out of nowhere. To my knowledge there was never a release candidate or Proton Next build for 8.0-1. But it's great news nonetheless, as we're getting quite the feature list with today's update.

Included in the update are 18 newly playable titles, from *Forspoken* to *Dead Space (2023)*, NVAPI support "for many games," improved multi-touch support, improved sleep/resume functionality on Steam Deck, fixes for the 2K and *Final Fantasy XIV* launchers, alt-tabbing fixes with GNOME 43, and so much more. Also, Proton 8.0-1 upgrades Wine to [8.0](https://linuxgamingcentral.com/posts/wine-8.0-released/), which in of itself is a huge upgrade from Wine 7 -- improved controller hotplugging support, better steering wheel support with improved force feedback, and improved Direct3D performance!

The following titles are now playable:
- [*Forspoken*](https://store.steampowered.com/app/1680880/Forspoken/)
- [*Samurai Maiden*](https://store.steampowered.com/app/1952250/SAMURAI_MAIDEN/)
- [*Dead Space (2023)*](https://store.steampowered.com/app/1693980/Dead_Space/)
- [*Creativerse*](https://store.steampowered.com/app/280790/Creativerse/)
- [*Nioh 2 - The Complete Edition*](https://store.steampowered.com/app/1325200/Nioh_2__The_Complete_Edition/)
- [*One Piece: Pirate Warriors 4*](https://store.steampowered.com/app/1089090/ONE_PIECE_PIRATE_WARRIORS_4/)
- [*Atelier Meruru*](https://store.steampowered.com/app/936190/Atelier_Meruru_The_Apprentice_of_Arland_DX/)
- [*Atelier Lydie & Suelle The Alchemists and the Mysterious Paintings*](https://store.steampowered.com/app/1502990/Atelier_Lydie__Suelle_The_Alchemists_and_the_Mysterious_Paintings_DX/)
- [*Atelier Sophie: The Alchemist of the Mysterious Book DX*](https://store.steampowered.com/app/527270/Atelier_Sophie_The_Alchemist_of_the_Mysterious_Book/)
- [*Blue Reflection*](https://store.steampowered.com/app/658260/BLUE_REFLECTION/)
- [*Atelier Rorona The Alchemist of Arland DX*](https://store.steampowered.com/app/936160/Atelier_Rorona_The_Alchemist_of_Arland_DX/)
- [*Disney Dreamlight Valley*](https://store.steampowered.com/app/1401590/Disney_Dreamlight_Valley/)
- [*ROMANCE OF THE THREE KINGDOMS XIV*](https://store.steampowered.com/app/872410/ROMANCE_OF_THE_THREE_KINGDOMS_XIV/)
- [*ToGather:Island*](https://store.steampowered.com/app/1181440/ToGatherIsland/)
- [*WARRIORS OROCHI 3 Ultimate Definitive Edition*](https://store.steampowered.com/app/1879330/WARRIORS_OROCHI_3_Ultimate_Definitive_Edition/)
- [*Exceed - Gun Bullet Children*](https://store.steampowered.com/app/207370/eXceed__Gun_Bullet_Children/)
- [*Gungrave G.O.R.E.*](https://store.steampowered.com/app/1630110/Gungrave_GORE/)
- [*Chex Quest HD*](https://store.steampowered.com/app/804270/Chex_Quest_HD/)

Improvements:
- Improved CJK font support in many games including *NOBUNAGA'S AMBITION: Souzou* with Power Up Kit, *Stardom 3* and *Sword and Fairy 3*.
- Improved sleep/resume functionality on Steam Deck for *Tiny Tina's Wonderland*.
- Improved multi-touch support.
- Improved force feedback compatibility for *BeamNG* and *Forza Horizon 5*.
- Improved multiplayer support in *Company of Heroes III*.
- Improved fullscreen support for *The Last Blade 2*.
- Enabled NVAPI for many games.

Bug fixes:
- Fixed 2K launcher failure caused by launcher update.
- Fixed Arabic fonts in *FIFA 21* and *22*.
- Fixed native scrollbar being always visible in *Final Fantasy XIV* Online launcher.
- Fixed *A Plague Tale: Innocence* and *A Plague Tale: Requiem* showing on-screen keyboard when starting the game on the Steam Deck.
- Fixed rendering issues during cutscenes in *Tom Clancy's Splinter Cell*.
- Fixed Japanese keyboard input in *Final Fantasy XIV Online*.
- Fixed *Football Manager 2023* crashing when trying to return from a player profile.
- Fixed experimental regression: *Fall in Labyrinth* started crashing on some setups.
- Fixed *Life is Strange Remastered* crashing at the end of chapter 2.
- Fixed Alt+Tab not working on Gnome 43.
- Fixed regression with *Mortal Combat X* performance.
- Fixed OpenGL launch option for *Youropa*.
- Fixed raytracing in *Crysis Remastered*.
- Fixed regression: *Minecraft Dungeons* was hanging when disconnecting from multiplayer game.
- Fixed *Immortals Fenyx Rising* missing/out-of-order audio lines in cutscenes.
- Fixed *The Witcher 3: Wild Hunt* launcher flickering on Wayland.
- Fixed Story Mode not working in *Dead or Alive 6*.

Updates:
- Updated wine to [8.0](https://linuxgamingcentral.com/posts/wine-8.0-released/).
- Updated dxvk to [v2.1](https://linuxgamingcentral.com/posts/dxvk-2.1-released/)-4-gcaf31033.
- Updated vkd3d-proton to [v2.8](https://linuxgamingcentral.com/posts/vkd3d-proton-2.8/)-84-g08909d98.
- Updated dxvk-nvapi to [v0.6.2](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.6.2).
- Updated wine-mono to [7.4.1](https://github.com/madewokherd/wine-mono/releases/tag/wine-mono-7.4.1).

Please be aware, however, that **your GPU will need to support [Vulkan 1.3](https://www.khronos.org/blog/vulkan-1.3-and-roadmap-2022).**

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/releases/tag/proton-8.0-1c). An update should be available for Proton in your Steam library. After downloading the update, restart the Steam client to start using it.

*Cover image credit: Luminous Productions/Square Enix*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
