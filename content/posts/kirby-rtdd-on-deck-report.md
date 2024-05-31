+++
title = "Kirby's Return to Dreamland Deluxe Looking Great on Deck!"
date = 2023-02-23T20:17:42Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/kirby/cover.jpeg"
tags = ["news", "steam deck", "emulation", "steam deck emulation", "nintendo switch", "kirby"]
keywords = ["kirby's return to dreamland deluxe on steam deck", "kirby's return to dreamland deluxe", "kirby's return to dreamland deluxe emulation", "kirby's return to dreamland"]
description = "Can even lower the framerate without sluggish gameplay!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After doing some brief testing with *Kirby's Return to Dreamland Deluxe* on Deck, I'm happy to report that I've had no issues, at least as far as Yuzu is concerned. No texture issues, framerate is a rock solid 60 FPS. Footage available [here](https://youtu.be/HAGxzsQb5_c).

![Kirby on Deck performance settings](/images/steam_deck/kirby/perf_settings.jpeg)

You should still get a decent framerate with the TDP limit set to 6 W, and the GPU clock set to 600 MHz. If you have [PowerTools](https://linuxgamingcentral.com/posts/preserve-battery-life-on-deck-with-powertools/) installed, I highly recommend disabling SMT.

![Kirby on Deck PowerTools settings](/images/steam_deck/kirby/powertools.jpeg)

Unlike [*Metroid Prime Remastered*](https://linuxgamingcentral.com/posts/metroid-prime-remastered-on-steam-deck/), the game actually doesn't become sluggish if you lower the framerate or refresh rate. If you decide to force 40 Hz, you can set the TDP limit down to 4 W and the GPU to 300 MHz. You *might* even be able to get away with less than 4 CPU threads, or lower the max CPU frequency. At 30 FPS, you can reduce the number of CPU threads to 2, set max CPU frequency to 2500 MHz, TDP limit to 4 W, and GPU to 200 MHz. Turn on half-rate shading and you've got yourself a gaming session that will likely last five or six hours.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/kirby_on_deck/kirby.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
