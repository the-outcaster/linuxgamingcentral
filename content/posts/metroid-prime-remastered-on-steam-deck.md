+++
title = "Metroid Prime Remastered: Steam Deck Report"
date = 2023-02-09T03:40:28Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/mpr_on_deck/official/cover.jpg"
tags = ["metroid", "steam deck", "emulation", "nintendo switch"]
keywords = ["metroid prime remastered", "metroid prime remastered on steam deck"]
description = "Update: no more crashing with the latest Ryujinx update!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*UPDATE: Ryujinx just got an update. Game no longer crashes before the parasite queen boss. I'm not sure if the map crash got fixed though. Make sure you're running the latest version of Ryujinx!*

*UPDATE 2 (2/9/2023): to improve performance with Yuzu, simply change the emulator's settings from handheld mode to docked. Problem solved. Footage available [here](https://youtu.be/AWvjK2L2paQ).*

*UPDATE 3 (2/10/2023): interested in a head-to-head comparison between both emulators? Well, [here you go](https://youtu.be/8Olrz3jRsTc).*

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/mpr_on_deck/yuzu_clip.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I did some testing of *Metroid Prime Remastered* -- the *official* one, which dropped just a few hours ago -- on Deck. With Yuzu, the game ran a beautiful 60 FPS...until the camera enters first-person mode. At that point, the FPS drops to exactly half at 30 FPS and struggles to go beyond that. Lowering the resolution didn't help. And while 30 FPS may still sound like an acceptable framerate, the problem is the game becomes incredibly sluggish.

Thankfully, we have more than just Yuzu when it comes to Nintendo Switch emulation. I also tried Ryujinx. Game ran *mostly* 60 FPS for the most part, even after entering first-person mode. But the caveat is Samus and her space ship are missing some textures. Not only this, but I can confirm two parts in the game where the emulator freezes:
1. When you try downloading the map for Frigate Orpheon
2. Opening the door to the parasite queen's room

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/mpr_on_deck/clip.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I have confirmed with other players that they too experienced this issue. Finally, the mouse cursor constantly needs to be moving around. If the cursor disappears -- which it will after a few seconds of inactivity -- the screen goes black. The workaround that I've used is to configure Steam Input to press Left Mouse click with any button that I press, so that the cursor constantly stays on screen. Or you'll need to keep the game running in a window.

If you want, you can lower the TDP to 9 W and the GPU clock to around 500 MHz. With Ryujinx, the framerate still remains a relatively smooth 60 FPS, but there will be random tanking of the framerate, and you'll need to temporarily disable the GPU clock limiter and then re-enable it to get the FPS back up. So it might be better just to not touch the power settings for now.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/mpr_on_deck/camera.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I'm sure it won't be long before either the Yuzu or Ryujinx developers look into this, but for now, this is what you'll need to be aware of. I have a [recording](https://www.youtube.com/watch?v=eEZTJ57Jqkg) on YouTube if you'd like to see the game in action, but beware the sound is a little off.

I'm going to test some more, particularly on my desktop, and see what happens.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
