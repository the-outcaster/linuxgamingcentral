+++
title = "The State of Ryujinx, the Nintendo Switch Emulator (February 2022 Edition)"
date = 2022-03-13T21:56:57-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://blog.ryujinx.org/content/images/2022/03/joysticks2-2.png"
tags = ["ryujinx", "emulation"]
keywords = ["switch emulator", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The [Ryujinx](https://ryujinx.org) team has assured us that, despite February being a short 28 days, they paid back an "avalanche of improvements, fixes, additions and ongoing project work."

First thing's up is [**Vulkan progress**](https://boilingsteam.com/ryujinx-great-strides-with-vulkan/). Check out the video below for a comparison of single-threaded SPIR-V (the shader language for Vulkan) on *Super Mario Odyssey* vs. multi-threaded:

{{< youtube "C3R-SlijVSc" >}}

Implementing this obviously wasn't easy, but looking at the results, it seems the effort really paid off. I don't know what the hardware of this particular machine was; I'm guessing it's using AMD on Windows.

Take another example here with *Super Smash Bros. Ultimate*, a game that uses *a ton* of shaders:

{{< youtube "XaTAD8zwZVQ" >}}

The multi-threaded version still has a few slowdowns here and there, but it's far more impressive than OpenGL's GLSL shader language. And that's with eight characters on the screen at once! It takes a whole 25 seconds for the GLSL version just to get to the "GO!" part.

Keep in mind the Vulkan API is not available on the main branch just yet; you have to get the [pull request](https://github.com/Ryujinx/Ryujinx/pull/2518) from GitHub, as there's still quite a few bugs that need to get ironed out before it reaches mainline.

Amazing progress, really is.

Speaking of *Smash Ultimate*, stuttering has been drastically reduced for particular areas, such as getting into the main menu and the character selection screen.

Next up is **GPU fixes**. *Game Builder Garage*'s graphical problems went from this:

![gbg graphical glitch ryujinx](https://blog.ryujinx.org/content/images/size/w1000/2022/03/game-builder-before-2-1.png)

To this:

![gbg glitch fixed](https://blog.ryujinx.org/content/images/size/w1000/2022/03/game-builder-after-2-1.png)

With just *two* lines of code.

Several other game-specific graphical glitches were fixed, ranging from the caves in *Pokémon Legends: Arceus*, outlines in geometry in *Pokémon Sword/Shield*, black water in *Paper Mario: The Origami King*, blue emblems on ships in *Monster Hunter: Rise*, jellyfish in *NEO: The World Ends with You*, a few Unreal Engine-powered games, and water in *Fatal Frame: Maiden of Black Water*. A fix was finally added for *Miitopia* so players can play through the game in its entirety without experiencing the crash found when trying to open a particular door. Another fix was set in stone for *River City Girls Zero* after a specific cutscene.

Some **audio fixes** were applied to such titles as *Nintendo Switch Sports* and *Zelda: Skyward Sword HD*.

Other fixes/improvements include:
- a better handling of stick drift by implementing a new deadzone algorithm
- support for more instructions for Ryujinx's dynamic recompiler (ARMeilleure) -- which means a better probability that a new game will work right on day one
- backend optimizations
- faster compilation for Windows builds
- a stable, non-flickering menu
- the initial layout for Skyline and Acropolis modding frameworks
- Linux-specific bug fixes

See, there really was a lot of features and bug fixes packed for the month of February. I'm personally excited about the Vulkan progress; it's looking promising. Waiting for shaders to compile on OpenGL is quite painful. AMD users will especially benefit from the Vulkan backend.

Read more about the February 2022 progress report on Ryujinx's [blog post](https://blog.ryujinx.org/progress-report-february-2022/). Also, look forward to an emulation guide from me within the next few weeks.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
