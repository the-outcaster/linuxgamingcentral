+++
title = "Metroid Prime Trilogy on Deck: A Match Made in Heaven"
date = 2022-06-22T13:17:47-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/photos/prime/cover.jpg"
tags = ["metroid", "emulation", "steam deck"]
keywords = ["metroid prime trilogy", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I wanted to briefly talk about the trilogy of *Metroid Prime* games running on the Deck. In a nutshell: it works pretty great. Not flawless by any means but you'd be surprised at how well the controls work.

All you have to do to get up and running is to run the [EmuDeck script](https://www.emudeck.com/#download) on your Steam Deck. Then copy your Trilogy ISO to `/home/deck/Emulation/roms/primehacks/`. Exit Steam in Desktop Mode, and add artwork with Steam ROM Manager. You should be able to launch PrimeHack and the ISO directly from Steam in Game Mode.

For those of you who aren't aware, [PrimeHack](https://forums.dolphin-emu.org/Thread-fork-primehack-fps-controls-and-more-for-metroid-prime) is a fork of the Dolphin emulator that enables keyboard and mouse controls for the *Prime* games, as well as an adjustable FoV slider and a wide assortment of other enhancements. And fortunately for us, PrimeHack is available natively on Linux. Even better is the fact that EmuDeck also supports PrimeHack and configures most of the controls for us. Only problem here is PrimeHack doesn't support 16:10, so you're going to get black bars at the top and bottom of the screen.

![prime 1 on deck](/images/steam_deck/photos/prime/prime.jpg)

Kind of amazing to think about how the Wii's controls were "converted" to fit well with the Deck. The right trigger acts as the shoot button. The right thumbstick/trackpad act as the cursor movement. If you want you can enable more fine-tuned aiming by going to Steam Input settings and enabling the Deck's gyro with the touch of the right thumbstick or trackpad. You can further enable the back buttons so you don't have to move your thumb away from the trackpad when you're jumping or shooting a missle. Needless to say, all these controls work *really* well on the Deck.

If you don't have the Trilogy ISO, you can still make use of PrimeHack's controls with the original *Prime* 1 and 2 for the GameCube. Controls will for the most part be identical to the Trilogy, but I've discovered with the original *Metroid Prime* that the gyro was *way* too sensitive, so I lowered that in the Steam Input settings.

One other thing: chances are you've played all three games dozens of times already. Want to change up the experience? Try [RandoVania](https://github.com/randovania/randovania). All the items get randomly shuffled, forcing you to explore the game in different ways. Plus you can skip most of the cutscenes. Note that this only works with the GameCube versions of *Prime* 1 and 2; *Prime 3* support is experimental and the Trilogy ISO didn't work when I tried patching it.

![prime 1 on deck while aiming at a creature](/images/steam_deck/photos/prime/aiming.jpg)

Battery consumption is similar to *Melee*; 7, 8, sometimes 9 watts. Expect at least four hours of battery life. Performance isn't exactly perfect though; some areas of the game render slower than 60 FPS.

I tried using the [Metroid Prime Remastered](https://linuxgamingcentral.com/posts/mpr/) mod on the Deck. Do yourself a favor and don't try it. MPR is a fork of PrimeHack and is only available on Windows. Trying to get the emulator to work with Wine was a royal pain in the arse, and even when I thought I finally figured it out the controls simply did *not* work.

At any rate, if you've got a legal copy of *Metroid Prime Trilogy*, give it a spin on your Deck. The controls are *amazing.* I'll probably have a video on it soon, provided Nintendo doesn't go after me. In the meantime there's some footage by @Rinzheim on [Twitter](https://twitter.com/Rinzheim/status/1515321060991901697).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
