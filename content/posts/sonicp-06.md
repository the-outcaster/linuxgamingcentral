+++
title = "Have You Played...Sonic P-06?"
date = 2023-05-11T05:55:58Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/p06/p06.webp"
tags = ["sonic", "remake"]
keywords = ["sonic the hedgehog", "sonic the hedgehog 2006", "sonic 06 remake", "project 06", "sonic p-06", "chaosx", "sonic p-06 on steam deck"]
description = "A fan-made remake of the infamous 2006 game...with many of its issues fixed!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Oh man. That dreaded Sonic game from 2006. The game that no one wants to remember for its graphical glitches, poor camera system, painstakingly long load times, the cringe moments where a princess might kiss a hedgehog, and a plethora of other issues.

But what if I told you there was an unofficial remake that addresses several of these bugs? No, the cringy cutscenes are still there. But the camera system is drastically improved, the graphics are better, and load times are faster. Sonic and Silver move faster; other characters have had their attributes altered for a better experience. 

Not only this, but the project aims to restore some of the content that was removed during the development of the original game. For instance, the player has the choice of using Sonic's animations from the 2005 Tokyo Games Show, or the ones that showed up in the final product. Players have the option to use PlayStation icons instead of Xbox. In-game cutscenes and hint icons can be disabled.

![Sonic P-06 Shadow](/images/p06/shadow.jpg)

This is thanks to Project '06, or [Sonic P-06](https://en.wikipedia.org/wiki/Sonic_P-06). The project is spearheaded by programmer ChaosX. This isn't a PC port of the original game; ChaosX, with the use of the Unity engine, made most of the resources in the remake from scratch, from the animations, textures, shaders, and so forth. Other contributors would later join the project to improve model compatibility with Unity, improving the collision detection system, the model rigging, etc.

While the remake is only available for Windows, it works fantastically on Linux/Steam Deck with the use of Wine and Proton. Keep in mind that **the entire game is not available to play at the moment**; new versions are being gradually released every few months that add more content, but currently, the story mode is not available. Only character-specific missions are available, although there is a "test area" in which you can switch between the nine playable characters. The latest update shipped with Silver's missions.

There's a [modding community](https://gamebanana.com/mods/games/7579) behind the game as well, so if you want to skip the intro, replace Sonic's model, or play an entirely different level, chances are there's a mod for it. 

# Optimal Settings on Deck
I have had the best experience using GE-Proton. [8-3](https://linuxgamingcentral.com/posts/ge-proton8-3/), specifically. If you use vanilla Proton, you're going to get that checkered background in the main menu (for missing media codecs). Using Wine fixes the video playback, but some text in the game's menus are rendered invisible. So GE-Proton8-3 is the version I'd recommend using.

Available resolutions are anywhere from 320 x 200 to 1280 x 800. Advanced graphics options such as draw distance, texture quality, and shadows can be adjusted anywhere from very low to very high. Display mode can be adjusted to fullscreen, fullscreen borderless, or windowed.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/p06/60fps_clip.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Even with the resolution set to 640 x 400 with FSR scaling enabled, the game struggles maintaining a smooth 60 FPS on the highest graphics settings, at least with Sonic's first level, Wave Ocean. Some areas will be 60, other areas can dip down to 45-50. Average power consumption is around 25 W. Temperature is around 78 degrees C.

I noticed when I lowered most of the graphics settings from "Very High" to "Medium," the framerate was a lot more consistent. Battery consumption also went down to around 18-20 W. However, I still don't recommend setting a TDP limit or GPU clock speed limit here, as the framerate can still dip in the busier areas in the game.

**A more optimal build would be using the Golden 40 standard.** I have been able to get away with a 6 W TDP limit, and a GPU clock speed limit of 600 MHz, on the highest graphics settings, and still maintain a relatively stable 40 FPS. You may want to be a little more generous though and increase the TDP to 7 W and GPU speed to 700 MHz. Battery consumption is *halved* at just 12 W, and the CPU/GPU temp is significantly lower as well at 55 degrees C.

YouTube footage available [here](https://www.youtube.com/watch?v=rcBw-EQfC4s).

# A Game Worth Revisiting
Sonic P-06 is the much-needed makeover that *Sonic 06* needed, and at 40 FPS it plays very well on Deck. GE-Proton8-3 is recommended for video playback.

![Sonic P-06 Rouge](/images/p06/rouge.jpg)

To get Sonic P-06, download it from [Google Drive](https://drive.google.com/file/d/1uyDINQBG4mTD1zLb4vj718bENUvr5RT2/view) in Desktop Mode, extract the zip file, right-click the "Sonic the Hedgehog.exe" file, and select "Add to Steam". From there you can use the SteamGridDB plugin in Game Mode to add custom artwork. Force the game to use GE-Proton8-3.

Can't wait for further updates to this remake!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
