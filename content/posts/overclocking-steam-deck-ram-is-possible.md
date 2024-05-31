+++
title = "You Can Overclock Your Deck's RAM Speed"
date = 2023-02-18T04:03:03Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/overclocking_ram/deck_overclocked_ram.webp"
tags = ["news", "steam deck", "steam deck memory"]
keywords = ["steam deck", "steam deck ram", "steam deck memory", "increase steam deck memory speed"]
description = "But notice I didn't say you SHOULD do it."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Reddit user Me2151 figured out [how to overclock the Deck's RAM](https://www.reddit.com/r/SteamDeck/comments/1144w09/guide_for_ram_overclock/) from the default 2750 MHz (5500 MT/s) to 3200 MHz (6400 MT/s). Basically, all it took was downloading and flashing an advanced BIOS utility to a flash drive, booting to said drive via a USB-C dock, and configuring the DRAM timing configuration.

However, there's a strong warning:
> This guide uses a tool that CAN brick your Deck if used incorrectly. I am not responsible for any damage caused by this guide nor is Valve. If you choose to use this tool and brick your Deck do not expect Valve to repair for free as this would most likely void your warranty. There ARE ways to unbrick your Deck however you need the knowledge and tools(ch421a programmer) yourself. I will not help you.

I *really* don't think it's worth risking your Deck's PCB getting bricked. If you do manage to successfully overclock the RAM, though, it seems there are small performance improvements:

![Fire Strike benchmarks between 5500 MT/s and 6400 MT/s](/images/steam_deck/overclocking_ram/fire_strike.webp)

![Benchmarks between 5500 MT/s and 6400 MT/s](/images/steam_deck/overclocking_ram/benchmark.webp)

Funny enough, yesterday I was able to see the [GitHub page](https://github.com/DavidS95/Smokeless_UMAF) for the BIOS utility. Going to that same page now, though, you'll get a server error. Probably didn't take long for people to complain about broken Steam Decks, enough to the point where the developer decided to remove the project (that's just my guess).

You also have to consider the battery as well. It's short enough as it is; overclocking the RAM will likely cause it to be consumed even faster. But, if you're feeling brave enough, and maybe you have a spare Deck that you can experiment with, you can [follow their guide](https://www.reddit.com/r/SteamDeck/comments/1144w09/guide_for_ram_overclock/).

*All images are credit of u/Me2151*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
