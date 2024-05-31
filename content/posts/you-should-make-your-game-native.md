+++
title = "You Should Still Consider Making Your Game Available on Linux"
date = 2023-04-26T18:22:06Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/tux.jpg"
tags = ["opinion", "steam deck", "native"]
keywords = ["native linux games", "linux game benefits", "proton vs. native", "steam machines", "tim besset valve"]
description = "Let's see how this discussion pans out..."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I feel like I'm entering hot water when I bring up a subject like this.

And I'm not going to re-hash what everyone else has said regarding Proton VS. native, except for maybe the fact that, if it weren't for Proton and the aggressive updates that have been pushing out for it, the Steam Deck would likely have been dead on arrival, much like the Steam Machines were.

Proton has been absolutely *great* to have, I'm not going to lie to you. Ever since it came out in 2018 I have had absolutely no reason to touch Windows ever again. And as most game developers are more familiar with Windows development, Proton takes the guessing game out. No longer do they have to learn what it takes to make their game work natively on Linux. "No porting required," as Valve infamously said when they first advertised the Steam Deck.

Now here, of course, is the *but*. There were some things that Valve contractor Tim Besset had mentioned in my [interview with him](https://linuxgamingcentral.com/posts/interview-with-tim-besset-valve-contractor/) that got me thinking.
> What I love about Proton is the options that it gives developers for bringing their game to the Steam Deck. Trying to ship a Linux port when you lack the resources, time and know-how is not a good place to be for a developer. So we remove that pain. **Now we see developers who want to ship native for the right reasons - they squeeze an extra few percent of performance and battery life**, their codebase gets battle-tested against multiple compilers and runtime environments, etc.

When I asked if he could expound a little further, he mentioned that "there is a bit of overhead with Proton." I imagine he was referring to the CPU department. This overhead, though it may be getting less over time with the advancements made to Proton, will cause your Deck's battery to deplete slightly faster. The overhead can also cause performance issues.

When the game is native to Linux/SteamOS, this overhead doesn't exist. As Tim brought out, this brings "an extra few percent of performance and battery life." It may only be a few percent...but I'll take that for what it's worth.

![No porting required](/images/steam_deck/no_porting_required.webp)

Debugging your game will also be easier:
> A native build will be slightly easier to debug and fine tune performance for. We support remote debugging with Proton and Visual Studio, but if you have a native binary it’s still a little easier to work that way.

Though I'm not a game developer, I think it may also be of help when your game is using some sort of anti-cheat service. A game that uses Easy Anti-Cheat, for instance, [may be a little less of a headache to properly support if the game is native](https://boilingsteam.com/enabling-eac-support-on-linux-now-easier/), rather than supporting EAC through Proton. Feel free to correct me if I'm wrong about this, though.

And if your game is developed with Godot, Unreal, or Unity, chances are you only need to do a one-click export, depending on your shaders or if its using middleware:
> For the most part it seems [these engines] are truly ‘one-click export’ to produce a solid native build that works with Steam for Linux. Provided...that you haven’t pulled in middlewares that do not support Linux as a target. With UE you may have a few surprises if you’ve never tested your setup with Vulkan and may need to tweak a few of your shaders but that’s about it.

So, a native game brings the following benefits:
- no overhead; better performance and longer lasting battery
- easier debugging
- easier to set up anti-cheat (though again, I could be wrong on that; if you're a dev I'd love to hear your thoughts on this)

Now hear me out. I am by no means forcing game devs to use Linux if they don't want to. Proton takes much of the needed guesswork out. Chances are a game will "just work" out-of-the-box with Proton. So, if a dev doesn't want to take the time to learn the nuances of Linux -- especially since we are such a niche audience -- fine.

What are your thoughts? Are you fine with Proton, or do you think supporting Linux natively for that "extra few percent of performance and battery life" is worth it?

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
