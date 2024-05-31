+++
title = "An Interview with Alesh Slovak, ChimeraOS Developer"
date = 2022-04-17T20:55:04-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos_interview/cover.jpg"
tags = ["interview", "chimeraos"]
keywords = ["chimeraos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I love getting insight with developers as far as what it's like developing their project. I like the concept of having a distro that transforms a PC into a living room console, which, as Alesh Slovak (AKA [alkazar](https://github.com/alkazar)) explains in this interview, is exactly what ChimeraOS does. So let's take a deep dive into the mind of Alesh and see just what is cooking with this console-oriented distro. There's two things from this interview that I want you to pay particular attention to, and that is:
1. Alesh's impressions of the Deck. It's a lot different than what many other reviewers have highlighted.
2. Alesh's stance on native versus Proton gaming. Yes, there's a million different options out there and it's a long-standing debate, but Alesh's opinion is still noteworthy.

Understandably, some of you may be strapped on time or just want this interview wrapped up in a nutshell, so here's the **TL:DR** of the interview. I do recommend giving the whole interview a read though, I think you'll enjoy it (note: bold has been added by me).
- Alesh's favorite games are racing titles from Codemasters
- Alesh has been a full-time Linux user for 20 years
- The move to rename the project to "ChimeraOS" was a good one, and came from the merging of game store fronts as well as PC and console gaming
- There are usually three-to-four active developers who work on ChimeraOS
- ChimeraOS runs well on the Deck, albeit for missing audio
- Alesh is turned off by the discomfort of the ergonomics on the Deck
- Valve actually did acknowledge Alesh for his work on ChimeraOS and thanked him for it
- Don't use SteamOS 3 on a device other than the Deck
- Alesh says Proton is better in the long run over native games, due to the lack of developers' knowledge of Linux and the lack of interest in upkeeping maintenance on games
- Spread the word about ChimeraOS!
- Special thanks to Wouter, Samsagax, and Pastaq for contributing to the project
- With SteamOS 3, this has actually helped the growth of ChimeraOS

# So, for those who may not be aware, explain who you are and what led up to the creation of ChimeraOS.
I founded and work on [ChimeraOS](https://chimeraos.org), a project with the goal of bringing an out of the box console gaming experience to PC hardware.

I was a big fan of SteamOS 2 and used it on my living room PC. However, I became increasingly frustrated with SteamOS and eventually installed Arch Linux which I use on the desktop. Over time I molded my living room Arch install to better match the experience of SteamOS. Adding things like the specialized [SteamOS compositor](https://github.com/ChimeraOS/steamos-compositor-plus) and a custom-built [automatic update system](https://github.com/ChimeraOS/frzr).

I thought what I had built was quite useful and unique and I wanted to share it with others, thus ChimeraOS was born.

# What are some of your favorite games?
I really enjoy racing games, and in particular Codemasters games.

Some of my favorites are:
- *Wave Race 64*
- *Grid (2008)*
- *Dirt 2*
- *F1 2021*

# How long have you been using Linux? Are you a full-time Linux user or do you hop between Windows/Mac as well?
I have been a full time Linux user for 20 years. I purchased Half-Life 2 on release day (in a physical box!) and played it on Linux through Wine, it actually worked quite well!

I did dual boot Windows XP for a brief time just for gaming, but it didn't last long as I quickly grew tired of constantly rebooting. Before switching to Linux I was actually a Mac user and started my career as a Mac developer. I have never really used Windows as a daily driver.

# The project was initially named "GamerOS." How has the feedback from the community been after renaming the project to ChimeraOS?
After changing the name to ChimeraOS, the negative comments about the name completely stopped, so I think it worked out well! The negative comments were really getting to me so I think it was a good change, if for nothing else, my mental health.

# What led up to the name "Chimera"?
We spent probably at least a year discussing and coming up with various alternative names.

The "Chimera" name seemed apt on two fronts: the merging of PC and console gaming in general, and the merging of the various specific platforms we support, such as Steam, Epic, and GOG onto a single box.

![chimeraos logo](/images/chimeraos_32/cover.svg)

*Image credit: ChimeraOS website*

# How many people work on ChimeraOS currently?
There are about **3-4 active contributors including myself**, but we do also see some folks pop in for one-time things.

# Looks like you got yourself a Steam Deck. And [you've installed ChimeraOS on it](https://twitter.com/ChimeraOS_Linux/status/1506101751048454145). How has the experience been? Would you prefer to use Chimera over SteamOS 3.0?
Yes, I was lucky enough to have gotten into the queue early and scored a Steam Deck on the third week of deliveries. I did install ChimeraOS, but I wouldn't recommend it currently due to missing audio.

Otherwise it works great, and I think with some minor configuration changes you could even get almost all of the Steam Deck and SteamOS 3.0 functionality working.

# What are your thoughts on the Steam Deck as far as the software experience, the ergonomics, etc?
I have had the Steam Deck for a few weeks now, paid for with my own money, and **to be honest I am rather disappointed.** I love the Steam controller (I own three), but I find the Steam Deck's controller nearly impossible to use.

The analog sticks are incredibly slippery! I am not sure why no one has mentioned this in any reviews. It is almost impossible to keep my thumbs on them as they keep sliding on the smooth top surface and the outer ring with the only grip on it is incredibly narrow. I have to constantly reposition my thumbs which is tiring and distracting.

The trackpads are also impossible for me to use due to their positioning. I am contorting my hands and thumbs to get them in the right position to be able to use them.

The bumpers are difficult to depress as they are quite narrow on the edges, requiring me to stretch for them and thus getting my other fingers out of position to use other parts of the controller.

The grip buttons which are one of my favorite things about the Steam controller I can't seem to utilize at all. It seems impossible to get the right leverage to use them comfortably.

![chimeraos on deck](/images/chimeraos_interview/chimeraos_on_deck.jpeg)
*Image credit: ChimeraOS Twitter*

I am also really disappointed about the lack of dual stage analog triggers which was my absolute favorite thing about the Steam controller, but at least I knew that going in.

The software experience is quite good, but as others have noted a bit rough around the edges. Even simple things like navigating around the UI can be frustrating due to the many small issues. For example, going back to your library will drop you in a different location than expected, or all the games below the current row in the library will randomly disappear and you can't navigate down until you navigate up again first.

There are many games which are verified that don't work very well, especially when it comes to the controller. Steam seems to select random community controller profiles instead of the default recommended profiles. I am not sure if that is just because Steam is honoring my settings I have for my Steam controller though.

Although the Deck is definitely nicer to hold, overall, I strongly prefer my Aya Neo. The screen is also much sharper and nicer on the Neo than the Deck.
I am not sure why I am having such difficulty with the Deck's controller. I don't think my hands are large.

# Looks like Valve took a lot of hints from Chimera: the immutable file system, the use of Flatpaks for applications outside of games, and Arch as the base system. Did they ever acknowledge you at any point in time?
I was very surprised at all the similarities between ChimeraOS and SteamOS 3.0. However, the underlying technology and many of the choices they made are quite different. But sometimes I wonder if Gabe isn't reading my mind, because everything I have ever wanted from Valve they have magically delivered:
- Steam Linux support
- Big Picture Mode
- SteamOS
- Proton

I recall wishing Valve would work on all the above years before they became a reality. Maybe if I wish hard enough *Half-Life 3* will materialize as well?

I have had some private email exchanges with a Valve employee. They did thank me for my efforts and even kindly gifted me a Steam key for all the Valve games! That is very much appreciated. I do wish we could collaborate with Valve more closely as it can sometimes be frustrating when there are Steam client issues that are affecting us and our users and it seems to fall on deaf ears. It can also be difficult to plan since we never know what kind of curve balls will be thrown our way. I think a lot of the problems are because Big Picture Mode has been deprioritized and neglected and hopefully things get better once the transition to the new UI is complete.

# Would you recommend to users ChimeraOS over SteamOS 3.0, or vice versa, and why?
For now at least, **SteamOS 3.0 is best on the Steam Deck and ChimeraOS for anything else.**

ChimeraOS on the Steam Deck is missing audio, so will not be a good experience at this point.

SteamOS 3.0 is tailored to the Steam Deck so installing and using it on any other hardware will be a challenge.

![chimeraos on Aya Neo](/images/chimeraos_interview/chimeraos_on_ayaneo.jpeg)
*Image credit: ChimeraOS Twitter*

# How has the general feedback for ChimeraOS been? Are users liking it and staying with it, or do some use it for perhaps a few months then move on to another distro?
The feedback seems quite positive. I don't know about how much folks stick with it though.

# Valve's stance on "no porting required" for the Deck. What are your thoughts on that? Do you prefer native Linux titles over games translated via Proton, or not have any sort of preference?
I think Valve's approach makes sense. They already tried the native first approach with Steam Machines but quickly discovered the handful of Linux game porting experts don't scale well.

In an ideal world Linux native would be the preferred option. Unfortunately, there are two things lacking:
- Linux expertise among game developers
- The will to maintain games in the long run

Linux is a fast moving target and is always changing. Linux can do this because the ecosystem is primarily open-source and there is usually someone out there willing and able to do the maintainence work.

Proprietary software doesn't fit into this model well. Especially games, which are constantly discarded like yesterday's fashion. A game may be popular one week and the next week no one is playing and the developer abandons it. Over time these games will rot and stop working.

Because of this, in my opinion, **games that use Proton are actually better than native in the long run.** We have already seen this with many games that had Linux ports over the years now work much better with Proton [read: [Feral Interactive's stance on Steam Deck support](https://linuxgamingcentral.com/posts/feral_says_no/)]. There are relatively few games with excellent Linux ports that continue to be maintained.

By inserting Proton between the game and the OS, Valve can essentially continue the work of maintaining games on behalf of the game developers. They are probably the most financially incentivized party to do such cross-cutting work. This is really excellent, both for Linux gaming and for game preservation in the long term. In a decade or two, Linux will be the best place to play old Windows games, if it isn't already.

For example, one of my biggest sticking points has been controller support which is obviously important for ChimeraOS. A lot of Linux native games have very inconsistent and poor controller support. Even the games that do have good support, will they work with PS6 controllers in 10 years? Probably not. Controllers almost always work great through Proton because Valve continually maintains it and adds support for new controllers.

# How can the community help out with the growth of ChimeraOS?
The easiest way to help is probably to test games and submit your results via a PR or to our [Discord](https://discord.gg/fKsUbrt).

Also, spread the word! There seems to be a fairly low knowledge and understanding of ChimeraOS and its tools out there. We do some very unique things that seem to fly under the radar. Such as game tweaks and patches, integrated Proton GE, remote game installation and management, and even a [game compatibility page](https://chimeraos.org/games). It is very likely that **ChimeraOS has out of the box compatibility with the largest number of games of any Linux distro, including SteamOS 3.0.**

# Anything else you'd like to share with us?
I want to thank all the contributors over the last few years, I really couldn't have done it without everyone's help! Especially [**Wouter**](https://github.com/sharkwouter) and [**Samsagax**](https://github.com/Samsagax) who have put a ton of effort in! I also wanted to acknowledge and thank a new contributer, [**Pastaq**](https://github.com/pastaq), for really taking initiative and solving some problems around the Aya Neo.

I thought that perhaps the advent of the Steam Deck and SteamOS 3.0 could have been the end of any interest in ChimeraOS, but we seem to be gathering even more Steam lately (pun intended)!

There you have it! [ChimeraOS version 32](https://linuxgamingcentral.com/posts/chimeraos_32_released/) was released just a few days ago, give it a spin if you want a living room gaming PC. And like Alesh had mentioned, help spread the word!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
