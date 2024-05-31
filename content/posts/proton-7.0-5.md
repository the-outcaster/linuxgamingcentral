+++
title = "Proton 7.0-5 Has Now Become Stable, Adds Support for 14 New Titles and Tons of Fixes"
date = 2022-12-06T22:25:18-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/proton/7.0-5.jpg"
tags = ["news", "software update", "proton"]
keywords = ["proton 7.0-5", "proton", "wine", "steam play", "dxvk", "vkd3d-proton", "valve", "codeweavers"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Congratulations to Valve, and especially CodeWeavers, who have tirelessly put forth the effort to make gaming on Linux and the Steam Deck easier and easier as the weeks and months go by. Proton 7.0-5 went from being a [release candidate](https://linuxgamingcentral.com/posts/proton-7.0-5-rc/) back in October, to [Proton Next](https://linuxgamingcentral.com/posts/valve-introduces-proton-next/) a month later, and now we've hit the stable release.

What's changed since Proton Next? Well, nothing, really. All of the same games are playable. The same bug fixes are in as well. Just think of the stable release as being more, well, *stable*. You could check the [GitHub thread](https://github.com/ValveSoftware/Proton/issues/6240) for the RC and see whatever other issues got fixed.

As a reminder, the following games are now playable:
- [*Airborne Kingdom*](https://store.steampowered.com/app/982290/Airborne_Kingdom/)
- [*Aspire: Ina's Tale*](https://store.steampowered.com/app/1720090/Aspire_Inas_Tale/)
- [*Battle Realms: Zen Edition*](https://store.steampowered.com/app/1025600/Battle_Realms_Zen_Edition/)
- [*Bulletstorm: Full Clip Edition*](https://store.steampowered.com/app/501590/Bulletstorm_Full_Clip_Edition/)
- [*Darkstar One*](https://store.steampowered.com/app/12330/Darkstar_One/)
- [*Deathsmiles II*](https://store.steampowered.com/app/1884300/Deathsmiles_III/)
- [*Indiana Jones and the Emperor's Tomb*](https://store.steampowered.com/app/560430/Indiana_Jones_and_the_Emperors_Tomb/)
- [*Nancy Drew: Legend of the Crystal Skull*](https://store.steampowered.com/app/31860/Nancy_Drew_Legend_of_the_Crystal_Skull/)
- [*Pico Park Classic Edition*](https://store.steampowered.com/app/461040/PICO_PARKClassic_Edition/)
- [*Primal Carnage: Extinction*](https://store.steampowered.com/app/321360/Primal_Carnage_Extinction/)
- [*Re-Volt*](https://store.steampowered.com/app/287310/ReVolt/)
- [*Rift*](https://store.steampowered.com/app/39120/RIFT/)
- [*Six Ages: Ride Like the Wind*](https://store.steampowered.com/app/881420/Six_Ages_Ride_Like_the_Wind/)
- [*Unravel 2*](https://store.steampowered.com/app/1225570/Unravel_Two/)

Fixes have been added for plenty of games, including *Batman: Arkham City*, *Marvel's Spider-Man Remastered*, *Return to Monkey Island*, *VRChat*, *CoD: Black Ops II*, *RDR2*, *Tekken 7*, *Armello*, and plenty of others. HOTAS has been fixed with *Elite Dangerous*, and *GTA V* has an improved "situation with not loading textures."
- fix *Batman: Arkham City GOTY* launching in the background on Steam Deck when set to fullscreen
- fix *Marvel's Spider-Man Remastered* displaying dialog about outdated drivers on AMD systems
- fix *Final Fantasy IV (3D Remake)* having no audio
- fix *Return to Monkey Island* not reacting to mouse clicks after a recent game update
- fix upsidedown videos in *VRChat* and many other games
- fix *Call of Duty Black Ops II Zombies and Multiplayer* hanging on exit
- fix *Bail or Jail* crashing when opening the Terms of Serivce
- fix *Red Dead Redemption 2* crashing after a recent game update
- fix *Final Fantasy XIV Online* launcher functionality after game update
- fix cutscene stutter in *Disgaea 5*
- fix Thrustmaster HOTAS having non-functional dial in *Elite Dangerous*
- fix *Planet Zoo* randomly crashing
- fix *SCP: Secret Labratory* not being playable after a recent game update (again)
- fix *Tekken 7* crashing at launch
- fix *Armello* hanging on exit
- fix *Sword Art Online: Hollow Realization* freezing after the tutorial
- fix *Space Engineers* intro video not playing correctly
- fix *Dragon's Dogma: Dark Arisen* videos not playing correctly
- improve *GTA V* situation with not loading textures

Network video support was added for [*VRChat*](https://store.steampowered.com/app/438100/VRChat/), and DXVK has been updated to [1.10.3](https://github.com/doitsujin/dxvk/releases/tag/v1.10.3)-28-ge3daa699. Note that this release did *not* upgrade to the newer DXVK [2.0](https://linuxgamingcentral.com/posts/dxvk-2.0/) since that requires newer GPU drivers; Proton 7.0 will continue to use DXVK 1.10.x until the next major release of Proton to maintain compatibility with older GPU drivers.

An update should be available in your Steam client. Simply update Proton (enable "Tools" in the list view in the top-left corner of your library to see it) and it should replace 7.0-4 with 7.0-5. Restart Steam and you should be all set. Note that Proton Next is no longer an available option, as it has been replaced with this stable release.

![Proton 7.0-5 in Steam](/images/proton/7.0-5_in_list.png)

See the patch notes on [GitHub](https://github.com/ValveSoftware/Proton/wiki/Changelog#70-5).

*Cover image credit: People Can Fly/Gearbox*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
