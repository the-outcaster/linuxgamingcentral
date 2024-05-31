+++
title = "Your Steam Deck's TDP Isn't Accurate"
date = 2022-11-15T14:14:02-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/tdp_inaccuracy/cover.jpg"
tags = ["news", "steam deck"]
keywords = ["steam deck", "tdp", "the phawx"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Something interesting that I came across yesterday. YouTuber The Phawx recently posted a [video](https://www.youtube.com/watch?v=fZ7T3mDPtZY) going over the Deck's TDP. Turns out it's not completely accurate. By comparing the Deck with the GPD Win Max 2 (prototype), he discovered both devices are in "absolute lockstep" -- if the Deck's TDP is set to 15 watts, for example, it will actually use 28 watts. If it's set to five watts, it will actually use 12.5 W at full brightness. At medium brightness, it will use 11.5 W.

LPDDR5 is not the problem -- even with the GPD Win Max 2 having slightly faster RAM than the Deck, it turns out that isn't the factor when it comes to power differences. The Phawx explains in the video why that's the case.

The Phawx uses the GPD Win Max 2 *production* model. At 15 W TDP, it's using about 3 W less at 25 W at full brightness. So what changed?

Well, let's have a look at the Deck's sensor data. The Phawx set the TDP cap to 15 W. But if you notice in the video, the actual wattage used is wildly fluctuating. Sometimes it's using less than 15 W, other times it's going over. This has to do with "how AMD has different modes to calculate TDP."

![Steam Deck sensor data with 15 TDP cap](/images/steam_deck/tdp_inaccuracy/steam_deck_sensor_monitoring.jpg)

The Phawx collects tens of thousands of samples of the wattage use. This graph puts it together nicely. So when the Deck is set to 15 W, it's actually using that number only 11% of the time. It's using 19 W 9.2% of the time. It uses 11 W 7.2% of the time. You get the idea. 50% of the time, the Deck is using *more* than 15 W. The other half of the time, it's using *less*. So the TDP *is* technically using 15 watts on average, but still flucuates all over the place. It's the same story for the Win Max 2 prototype.

![Wattage use with 15 W TDP on Steam Deck](/images/steam_deck/tdp_inaccuracy/graph.jpg)

Now let's compare it to the *production* model of the GPD Win Max 2. The fluctuation is a lot more stable here -- at 15 W TDP, the Win Max 2 is using 15 W about 15% of the time, and 14 W 17% of the time. Combine these together, the Win Max 2 uses 14 and 15 W over 30% of the time. About 75% of the time, it's using 15 W or less. Only 25% of the time does it use *more* than 15 W. The data still fluctuates a lot here, but the production model is *far* more accurate to the TDP limit than either the prototype or the Deck.

![Wattage use with 15 W TDP on GPD Win Max 2 production](/images/steam_deck/tdp_inaccuracy/gpd_win_max_2_production_graph.jpg)

The difference in wattage used between the production Win Max 2 and the prototype/Deck is because AMD uses two different profiles to determine TDP. Because of these profiles, the prototype scores some higher numbers when benchmarking Unigine than the production model, since it uses higher wattage on average.

![Unigine benchmarks at different wattages on GPD Win Max 2 production](/images/steam_deck/tdp_inaccuracy/bar_graph_tdp_usage_and_performance.jpg)

What should Valve do about this? "Absolutely nothing," The Phawx responds. 15 W TDP is in reality 19 W "to what we're all used to," meaning you're getting "more bang for your buck." You're getting more power with AMD's profile on Deck.

I don't know if I made any sense here, but you can watch The Phawx's [video](https://www.youtube.com/watch?v=fZ7T3mDPtZY) for more details.

**TL;DR** when setting the TDP limit on your Deck, the wattage used actually fluctuates a lot.

*All images used in this article are credit of The Phawx.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
