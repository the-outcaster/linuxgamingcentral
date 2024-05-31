+++
title = "Relax. A Game That Loses Native Linux/Steam Deck Support Doesn't Mean the End of the World"
date = 2023-06-12T12:48:53Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/opinions/games_losing_native_support/cover.jpg"
tags = ["opinion", "native"]
keywords = ["native linux games", "proton", "payday 2 losing linux support", "rocket league losing linux support", "proton vs native", "steam deck"]
description = "There are actually a few reasons why a native Linux game might be a bad idea in the long run."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A few months ago I had an opinion as to [why developers should target Linux](https://linuxgamingcentral.com/posts/you-should-make-your-game-native/) as an available platform when they export their games. My reasons were as follows: less overhead, better performance, increased battery life, and easier debugging. I still am for that argument. But only *if* the developer has the knowledge and is comfortable doing so. I'm not going to nudge any developer to natively support Linux if they don't want to, nor am I going to get upset if they decide later on to drop native support altogether.

Overkill made an [announcement](https://store.steampowered.com/news/app/218620/view/3667665767271115728?l=english) a few days ago that Linux support for *Payday 2* has come to an end:
> Linux users will not receive this update or any following updates coming to PC. In addition, Linux players will be unable to matchmake with other PC clients following this update. We tried to find a solution, but ultimately found it unfeasible due to the Linux version being on an older version of the *PAYDAY 2* engine.

Some have [speculated](https://steamcommunity.com/id/jaco909/recommended/218620/) that this largely has to do with the game [coming to the Epic Games Store](https://ww./w.paydaythegame.com/news/payday2/2023/06/epic-store-launch/) and not actually the engine being "an older version." At any rate, guess what? Proton is here to save the day. A game that loses native support does *not* mean that you can't play it on Linux or on your Steam Deck.

![Payday 2 community announcement](/images/opinions/games_losing_native_support/payday2.webp)
*Image credit: Overkill*

Reminds me of that whole debacle when Psyonix [dropped native support for *Rocket League*](https://www.rockpapershotgun.com/rocket-league-ending-mac-and-linux-support-because-they-represent-less-than-0-3-of-active-players) a few years ago. Admitedly, many players, including myself, were frustrated. The developers, however, came forward and became fully transparent as to why they dropped support:
> We'll be updating our Windows version from 32-bit to 64-bit later this year, as well as updating to DirectX 11 from DirectX 9. Unfortunately, our macOS and Linux native clients depend on our DX9 implementation for their OpenGL renderer to function. When we stop supporting DX9, those clients stop working.

"Significant additional time and resources" would have to be spent continuing support for Linux and Mac OS because of this, and this couldn't be justified with how tiny of an audience both Mac OS and Linux users are. Combined, we make up *less than 5%* of users on Steam. On Linux alone we barely reach 1%, and while that percentage may have perked up a little bit thanks to the Steam Deck, we're still just a tiny, *tiny* fraction of the whole PC gaming market.

But guess what? Yeah, you guessed right -- *Proton*. Proton still allows the game to be just as playable as it was when it was native. You can still run over other cars, and smash that ball right into the goal on both your Linux desktop and your Steam Deck, all without having to resort to Windows or a virtual machine. On top of this Psyonix/Valve were offering refunds to all players who were hoping to play the game natively on Linux or Mac, even if they have surpassed the two hour playing window or have had it longer than two weeks.

![Rocket League](/images/opinions/games_losing_native_support/rocket_league.jpg)
*Image credit: Psyonix*

If people get up and arms and start raising pitchforks when a company decides to drop Linux support, we're showing hostility towards the developers. And that hostility is only going to push developers away from wanting to ever support Linux again.

Just think about it. Say a developer sells 1,000 copies of his game. 1% of those buyers are playing it on Linux -- that would mean only 10 people. A few years down the road the dev says it's no longer worth maintaining the native Linux version, since it's a hassle trying to do so, and Proton is already available which can do the work for him and allow him to better focus his priorities on the game itself, not on supporting different platforms.

Can you really blame that developer if he decides to drop Linux support?

Linux gamers are a niche, vocal minority. And, very likely we always will be. Again, the Deck may have increased our numbers a bit. But as time goes on I'm starting to realize the nightmare that a lot of devs have when they try to maintain two separate versions of their game. It's a lot of work for supporting just 1% of their fans -- and for us just to turn our backs on them when they decide to drop native support is only going to leave a sour taste in their mouth.

![Steam stats by OS](/images/opinions/games_losing_native_support/steam_os_stats.webp)

# 1. Workload
Gardiner Bryant just released a [video](https://www.youtube.com/watch?v=DsYE-rNvP2A) considering four reasons why we actually shouldn't even *want* native games on Linux/Steam Deck:
> The first thing is **workload.** Now, game developers have an enormous task ahead of them -- I should know, my company has had a game in development for years. Developers not only have to establish the rules, create the art, and build a working version of a game, but they also have to port it to multiple platforms -- you know, you start with PC and maybe Mac and then you put it to the Switch, Xbox, and PlayStation. But then there's also smartphones. They've got to ensure that all of these disparate versions remain up-to-date, compatible with each other, and they have the latest changes intact. And this can honestly feel like a sisyphean task with that enormous workload. It's no wonder that adding yet another platform can be out of the question for many developers.

He also mentions "many of the most common tools for developers out there include minimal support for Linux, especially in the AAA space, if any at all," and this makes the "cost versus benefit analysis even less appealing."

# 2. Lack of Knowledge
As of May 2023, there are only [1.47%](https://store.steampowered.com/hwsurvey/?platform=combined) of us who are using Linux/Steam Deck on Steam. Since Linux desktop adoption is so small, so is the developer talent that is familiar with how Linux works. Most game devs are not familiar with Linux system APIs, or how to optimize their games for Linux. Proton alleviates that. Devs can just focus on their game working on Windows, without having to spend the time learning how a niche operating system works, and little to no work has to be done to let the same version become playable on Linux/Steam Deck.

![Steam Deck - no porting required](/images/steam_deck/no_porting_required.webp)

"No porting required."

# 3. Backend Trouble
OpenGL and Vulkan are cross-platform compatible between Windows and Linux. This means that, when developing a game, there's no need to "translate" these APIs between each platform. But many games these days use DirectX -- an API meant for Windows -- and converting those calls into OpenGL or Vulkan is no easy feat. Therefore, if a dev is making a game and wants it available on Linux, they're either going to have to use OpenGL/Vulkan, or have Proton translate the calls the game is using into a language Linux can understand. Gardiner states that the former "is not a profitable thing to do on the face of it."

Using Proton takes much of the hassle out if the game is using DirectX.

# 4. Native Games May No Longer Work Over Time
Games that you own on Steam that once worked natively on Linux may no longer work anymore. The Steam Linux Runtime (SLR) does alleviate some of the hassle that comes with having Linux libraries that your system can work with, but even that "isn't perfect."

Over time, your modern Linux system is no longer compatible with the libraries that are required by the game to run. This is due to Linux developers having poor maintainence of legacy software. Microsoft pays attention to backwards compatibility, and this is carried over into Proton. Therefore, even older versions of Proton will continue to work with "modern versions of Linux," and they will continue to allow your older games to be played.

![Supraland](/images/opinions/games_losing_native_support/supraland.jpg)
*Image credit: Supra Games*

So think back to that example of *Payday 2*. Would you rather have the devs be upfront and state that they are no longer supporting Linux, or would you rather wait another couple of years, find out the game no longer runs on your system because of outdated libraries, then ask for a refund out of anger because of the silence?

# Native Will Make Sense...One Day
If there will ever be enough Steam Decks sold, and enough PCs at Best Buy with Linux pre-installed are bought, then natively supporting Linux will be financially viable. More and more developers will have experience with the APIs Linux uses, more documention will be available, ports will be more optimized. There will be guaranteed compatibility 10 years from now. Companies like [Feral Interactive](https://linuxgamingcentral.com/posts/feral_says_no/) and Aspyr might actually resume their "porting" business.

In the meantime, though, we have Proton. Proton has been one of the best things Valve/CodeWeavers have brought to us. The number of games that are available to play in my library are *significantly* improved thanks to this. The Steam Deck would have had the same fate as the Steam Machines if it didn't ship with Proton.

I'd like to know what you think though. Has Proton been the good "middle-ground" while we're waiting for Linux to become more mainstream, if that ever becomes a reality?

*Cover image credit: Overkill*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
