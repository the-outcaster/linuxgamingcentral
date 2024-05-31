+++
title = "Undervolting and Overclocking Your Deck: Tradeoffs"
date = 2023-04-07T19:53:33Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/oc_and_uv_graph.png"
tags = ["overclocking", "steam deck"]
keywords = ["steam deck undervolting", "steam deck overclocking", "steam deck increased TDP"]
description = "CryoByte33 has a nice tutorial going over how to do this, but be aware there are risks."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
CryoByte33 recently released a [video](https://www.youtube.com/watch?v=LNEI7BTc87Q) on how to undervolt or overclock the Deck, and the benefits versus disadvantages that come with each method. There's also a transcript of the video over on [Steam Deck HQ](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/).

The process involves getting [Smokeless_UMAF](https://github.com/DavidS95/Smokeless_UMAF), flashing the firmware to a USB drive, booting from said drive while it's connected to the Deck, and modifying the BIOS settings from there.

# Undervolt for Increased Battery Life
Why would you undervolt the Deck? Cryo explains:
> Undervolting can help maintain higher speeds for longer, which can improve performance. It usually even improves the battery life of the Deck!

Undervolting in Cryo's case with *Elden Ring* made the CPU two-to-three degrees Celcius cooler. GPU temp also went down by two-to-five degrees. And the performance was almost exactly the same without undervolting. Cryo notes "I was able to go from one hour and 31 minutes of battery life to one hour and 46 minutes...that's a boost of 16% to battery life, despite performance being nearly identical."

That being said, undervolting can carry a risk:
> If you lower the voltage too much your Deck may not be able to boot. Most people have been able to recover from this, but I'm aware of 1 case where an RMA needed to be done from pushing the Deck way too hard.

# Overclock for Increased Performance
You can increase your Deck's TDP higher than 15 W. This requires disabling the updated fan curve in SteamOS, changing the PPT values in Smokeless UMAF to 15000, and making use of the [PowerTools plugin](https://linuxgamingcentral.com/posts/preserve-battery-life-on-deck-with-powertools/). Don't set the TDP any higher than 20 W.

Seems like *Cyberpunk 2077* "had averages on low increase by 9% and averages on high increase by 5%, along with a substantial boost to lows and 97th percentile on the high preset." *Elden Ring* had 6% and 4% boost to averages.

But here's the side effect: the battery went from one hour 31 minutes to "roughly 59 minutes," a 35% reduction.

In addition to the TDP, you can also overclock the CPU/GPU. Again, don't push the numbers too high if you want to keep your Deck in good working condition; Cryo recommends a max CPU speed of 3800 MHz and a max GPU speed of 1800 MHz.

If you want, you can combine all three: undervolt, increased TDP, and overclocked CPU/GPU. If you can strike a good balance between the three, you can get some decent results between an increase in performance while keeping the battery life nearly the same:
> All of this was while maintaining an average battery life of 1 hour and 25 minutes while going full tilt, which is only a 7% decrease from the 1 hour and 31 minutes I get in an identical situation without either overclocking or undervolting.

See the [video](https://www.youtube.com/watch?v=LNEI7BTc87Q) or [post](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/) for more details. Of course, this doesn't go without saying **you're doing these changes at your own risk.**

*Cover image credit: CryoByte33*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
