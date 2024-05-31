+++
title = "Denuvo: \"There is No Perceptible Impact on Gameplay Because of the Way We Do Things.\""
date = 2023-07-10T15:02:55Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/denuvo/motoracer4.webp"
tags = ["news", "denuvo"]
keywords = ["denuvo", "denuvo drm", "drm", "irdeto", "steeve huin", "drm performance", "drm anti-cheat"]
description = "Plus: a new anti-cheat coming soon."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Steeve Huin, COO of Video Games at Irdeto -- the company behind the infamous Denuvo DRM -- reached out to [Ars Technica](https://arstechnica.com/gaming/2023/07/denuvo-wants-to-convince-you-its-drm-isnt-evil/) in a poor attempt to try and defend the company's anti-tamper technology.

Denuvo affects some of your favorite titles: [*Street Fighter 6*](https://linuxgamingcentral.com/posts/sf6-gets-denuvo/), *Sonic Frontiers*, *Monster Hunter*, etc. You can't even mod some games without the risk of getting a temporary ban from being able to play the game. You can't even [play certain games on Alder Lake processors](https://www.pcgamer.com/intel-alder-lake-drm-game-list-workaround/). Sometimes [you can't even launch a game if the Denuvo domain goes offline](https://www.pcgamer.com/a-great-day-for-drm-as-denuvo-lapse-renders-tons-of-games-temporarily-unplayable/).

Here's what Huin had to say regarding Denuvo:
> Anti-piracy technologies is to the benefit of the game publishers, [but also] is of benefit to the players in that it protects the [publisher's] investment and it means the publishers can then invest in the next game. But people typically don't think enough of that.

In addition to thinking that Denuvo is "of benefit," he also believes that it doesn't harm gaming performance at all:
> Gamers [almost] never get access to the same version of [a game] protected and unprotected. There might be over the lifetime of the game a protected and unprotected version, but these are not comparable because these are different builds over six months, many bug fixes, etc., which could make it better or worse.

There seem to be some mixed results regarding this. Ars benchmarked [*Batman: Arkham Knight*](https://arstechnica.com/gaming/2019/09/ars-analysis-denuvo-drm-doesnt-slow-down-batman-arkham-knight/) and noticed there was no difference between Epic's Denuvo-free copy and Steam's Denuvo-laden version as far as performance and loading times. On the other hand, Katsuhiro Harada, director of *Tekken 7*, reported that the game's "encryption program" (anti-tamper third-party middleware) resulted in ["frame rate drops."](https://twitter.com/Harada_TEKKEN/status/984791954872569857) Benchmarks from [Overlord Gaming](https://www.youtube.com/watch?v=n_DD-txK9_Q) also suggest that several of the titles they tested -- from the *Dishonored* series, *Deus Ex: Human Revolution*, *Rime*, and a few others -- saw quite a drop in loading times *and* performance dips when the Denuvo is removed.

It's a good thing Huin acknowledges that most people aren't going to believe a word he says: "Our voice is unfortunately not sufficient to convince people because we're not trusted in their mind as a starting point in that debate."

Irdeto will supposedly be offering a program in the next few months where "trusted media outlets" will be given two copies of a game: one with Denuvo, and one without it. Huin wants people to see for themselves "that the performance is comparable." Seeing as the copy is coming directly from Irdeto, however, I doubt if the DRM-free copy is something to be trusted.

But it gets worse. Irdeto is also rolling out their anti-cheat mechanism called ["Unbotify"](https://irdeto.com/news/denuvo-unveils-unbotify-technology-for-bot-detection/). Huin says this will try "to separate humans from non-humans playing in a game." I can see this as a big obstacle for Proton developers. How are they going to add compatibility to a game for Linux desktop/Steam Deck if the anti-cheat prevents Proton from being able to play said game?

If there's one good thing I can see out of this, it would be that Denuvo is mostly going to be attached to only the bigger AAA hits. Even if independent developers could afford the anti-tamper technology, I think they're smart enough to not ruin their game by putting it in.

I'd like to know what you think though. Do you think Denuvo is a good anti-piracy strategy? Or does it only *encourage* piracy? Do you think this "Unbotify" anti-cheat will prevent games from being able to be played through Proton?

*Cover image credit: Overlord Gaming*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
