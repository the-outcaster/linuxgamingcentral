+++
title = "Switch Emulation on Deck: Ryujinx VS. Yuzu Tested"
date = 2022-08-07T22:43:52-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/mk8.jpg"
tags = ["steam deck", "nintendo switch", "emulation", "comparison"]
keywords = ["ryujinx", "yuzu", "steam deck", "emulation", "nintendo switch"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
EmuDeck version [0.17.6](https://github.com/dragoonDorise/EmuDeck/releases) just came out a few days ago. For those who aren't aware, EmuDeck makes it incredibly easy to get emulation of retro to more modern titles set up on the Steam Deck. And what's nice is combined with the [Steam ROM Manager](https://github.com/SteamGridDB/steam-rom-manager), roms can get added to the Steam Deck UI with nice cover art, and you can launch the game directly through this interface.

At any rate, the latest update adds support for the [Anbernic Win600](https://anbernic.com/products/new-anbernic-win600) and some other goodies. One feature in particular is that it adds support for the Ryujinx Switch emulator, in addition to Yuzu.

So, I went to work doing a comparison of emulating a handful of Nintendo Switch games on Deck with both Ryujinx and Yuzu, using the emulator settings set by EmuDeck. The following games were tested and compared:
- *Mario Kart 8*
- *Super Smash Bros. Ultimate*
- *Hyrule Warriors: Age of Calamity*

You can see the results [here](https://youtu.be/RcziIKr4cSw). A couple of notes:
- you might have noticed the quality on Yuzu isn't as great compared to Ryujinx. This is because Yuzu has 0.5x scaling while using the emulator's built-in FSR filter. This also explains why performance is better on Yuzu than Ryujinx. To my knowledge Ryujinx doesn't have a built-in FSR feature (though you probably could use it from the Quick Access menu)
- *Mario Kart 8* and *Smash Ultimate* were tested with Vulkan. *Age of Calamity* would not run at all on Ryujinx with Vulkan. As a result I had to use OpenGL for both emulators in order to make the comparison more fair
- games were recorded in Game Mode with the [Crankshaft plugin](https://linuxgamingcentral.com/posts/you-do-not-need-a-capture-card-for-deck/)

Yuzu does better in most cases. *Age of Calamity* is probably the most taxing game on the Nintendo Switch and poor Ryujinx couldn't handle much of anything better than 13-14 FPS. I even made sure the shaders were cached by playing the game a bit before recording. That being said, this was tested with OpenGL; Vulkan would be a *significant* improvement, especially on a device like the Steam Deck. It's just too bad that I couldn't use it on this game for the time being.

I should note that if you want to play Switch games on Deck with Ryujinx, you'll have to launch Ryujinx from the Deck UI and launch your game from there. The ROMs in the Deck UI will use Yuzu.

For more on Switch emulation on Deck, check out the comparison that I did with [OpenGL vs. Vulkan on Ryujinx](https://linuxgamingcentral.com/posts/switch-emulation-on-deck-opengl-vs-vulkan/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
