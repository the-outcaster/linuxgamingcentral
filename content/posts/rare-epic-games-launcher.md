+++
title = "Need An Alternative to Heroic Games Launcher? Try Rare"
date = 2023-03-21T16:28:58Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/rare/alternative_to/cover.webp"
tags = ["rare", "epic games store"]
keywords = ["rare epic games store launcher", "rare", "alternative to heroic games launcher", "epic games store"]
description = "And no, I'm not referring to the way your steak gets cooked."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
It seems whenever Epic Games Store launchers on Linux are mentioned, the attention always goes to [Heroic Games Launcher](https://linuxgamingcentral.com/tags/heroic-games-launcher/). Not that I have anything against Heroic; I personally think it's a great EGS launcher for Linux and Steam Deck that is constantly getting updated. But perhaps you'd like to use an alternative. That's where [Rare](https://linuxgamingcentral.com/tags/rare/) comes in.

To be honest, I'm not really fond of the name. When you try to look up "rare" on Google or DuckDuckGo, you'll either come across the company behind the *Banjo Kazooie* series, or the temperature of what a steak is cooked. And if you try to make the search more specific, to something like "rare epic games store," Google thinks you're looking for an EGS client that's, well, *rare*. This is probably the reason why this EGS alternative is never talked about, since nobody can get a direct search result for it.

Aside from that, Rare is pretty good. Per the description on the [GitHub page](https://github.com/Dummerle/Rare), it's a "graphical interface for Legendary, a command line alternative to Epic Games launcher, **based on PyQt5.**" That last part in particular is interesting. Under the "Why Rare?" section, one of the points mentioned is it "tries to be as lightweight as we can make it while still offering a feature-full experience."

![Rare game details](/images/rare/alternative_to/game_details.webp)

That's one of the benefits Rare provides. See, Heroic uses Electron. And every time I hear someone use the word "Electron," it makes everyone else cringe. Electron, in case you're not aware, is [very demanding on the user's hardware](https://en.wikipedia.org/wiki/Electron_(software_framework)#Reception). Developers love it, users hate it. But since 99% of the code for Rare is written in Python, it's not using Electron at all. It is therefore much lighter on the user's resources. Perhaps for Steam Deck users, this *could* translate to a longer-lasting battery with the client running in the background - but that's just a hypothesis.

With Rare you can also link your Ubisoft Connect account -- although, this hasn't been working for me with the latest beta.

You can browse the EGS within the app, although currently I'm only able to see the free-to-claim games. None of the filters seem to work -- selecting any of them on the right will just make the search results list empty. The Store tab is marked as beta though, so it's to be expected.

![Rare EGS store](/images/rare/alternative_to/store.webp)

Other than that Rare functions the same way as Heroic. You got your game library that you can download and manage. There's game verification, different Proton versions to use, whether or not to use Offline mode, launch parameters, and a plethora of other options. From your game library you have the choice of seeing your games as thumbnails, or as a list with more details.

Just a few days ago the [first beta for version 1.10](https://github.com/Dummerle/Rare/releases/tag/1.9.90) was released. This updates the design for the library and syncs saves in the launch helper.

Rare is available on [Flathub](https://flathub.org/apps/details/io.github.dummerle.rare), so Steam Deck users can rejoice that it's available for them. As far as I know, however, there's no integrated gamepad support within the app, so you'll have to make use of the touchscreen for now. Rare is also available as an AppImage, .deb, Mac, and Windows.

![Rare game properties](/images/rare/alternative_to/game_properties.webp)

So, it might not be as feature-full as Heroic is for the time being, but I definitely like the fact it isn't using Electron. Integration with Ubisoft Connect -- at least if it worked -- is also pretty neat. Give it a try!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
