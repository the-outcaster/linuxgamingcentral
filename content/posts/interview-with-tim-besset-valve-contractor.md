+++
title = "An Interview with Timothée Besset, Valve Contractor"
date = 2023-04-13T16:08:01Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/ttimo/cover.webp"
tags = ["interview", "valve", "ttimo"]
keywords = ["ttimo", "tim besset", "timothee besset", "quake 3", "valve contractor", "valve interview", "steam deck developer experience", "steam for linux", "steam linux runtime", "linux developer", "rocket league on linux", "street fighter v on linux"]
description = "Street Fighter V on Linux was real."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Typically, when you read or hear an interview with Valve, it comes from the likes of Pierre-Loup Griffais, Lawrence Yang, and even Gaben himself -- especially when it comes to the Steam Deck. However, there's a lesser-known face, Timothée Besset, based in Dallas, Texas. He's been a contractor for Valve since 2015, and his work towards Steam for Linux, as well as his work on the developer experience for the Deck, is just as important as everyone else's work to make Linux and Steam Deck gaming a reality.

I've had the privilege of getting to know him a bit better. You'll find he is quite the *Quake* fan, particularly with *Quake 3*, and was involved in helping a lot of id Software titles come over to Linux prior to his time at Valve. He was also involved with bringing *Rocket League* over to Linux. Oh, and here's a bonus: *Street Fighter V* on Linux, as a native binary, actually existed.

**TL;DR**
- became familiar with Linux with the use of HP-UX, SunOS (now known as Solaris), and IRIX
- started in the late 90s working for id Software, writing utilities for *Quake 2*'s level editor and tools
- "I was the Linux, multiplayer dedicated servers, gameplay and netcode guy" for id Software when he worked full-time for the company starting in 2004
- contracted by Valve in late 2015 for helping them "on various Linux projects"
- Tim mostly works on the Steam for Linux client, the Steam Linux Runtime, and the developer experience for Steam Deck
- primarily codes with C++ and Python
- favorite game engine is idTech4
- favorite game: *Quake 3*
- helped bring *Rocket League* and *Street Fighter V* to Linux, along with "several" other titles (yes, *SFV* for Linux actually existed, but was never publicly released for "various reasons")
- Proton was a good move for developers who don't have the experience or the time becoming familar with Linux, but Tim says a native Linux version is better for "an extra few percent of performance and battery life" and easier debugging
- "It is now much easier to produce native binaries with stronger guarantees that they run well across the major Linux distributions," thanks to Valve's containerized runtime/image
- new Steam Linux runtime in the works: sniper, with "updated compiler and userspace libraries"
- common engines such as Unreal, Unity, and Godot truly do offer one-click export and support for Linux, provided there aren't any middlewares or shaders that don't support Linux in the way
- the Steam Deck: "I love it!"

# Give us a deep dive in regards to who you are, your history in the gaming industry, and how you ended up becoming a contractor at Valve.
I got started in the late nineties writing utilities around id Software's level editor and tools for *Quake 2* (idTech2). When Loki Software folded, id passed the maintenance of *Quake 3* (idTech3) to me for a few years. I eventually joined full time in 2004, after working on various idTech3 titles (*RTCW*, *Wolf:ET*).

![Quake 2](/images/interviews/ttimo/quake2.jpg)
*Image credit: id Software*

By then I was the Linux, multiplayer dedicated servers, gameplay and netcode guy. I continued doing that through shipping *Doom 3*, *Quake 4* and *Enemy Territory: Quake Wars*.

I then went back to idTech3 for a special project that became *QuakeLive*. Probably my favorite thing to have worked on in that era - I had my hands in all the pies, doing tech, writing backend systems, play(testing) the game.

After that it was time to move on. id was losing interest in multiplayer and it was time to go. I worked for a small mobile games company here in Dallas, and continued building backend systems and cloud apps.

![Quake Live](/images/interviews/ttimo/quakelive.jpg)
*Image credit: id Software/Bethesda*

I was getting calls from former colleagues, folks who knew my work to have me contribute to the cool things they were building, so I transitioned to freelancing. Pretty scary thing to do but so far it works out.

In late 2015 Pierre-Loup Griffais reached out about helping Valve on various Linux projects.

# How did you get started on your Linux journey?
I started with [HP-UX](https://en.wikipedia.org/wiki/HP-UX), [SunOS](https://en.wikipedia.org/wiki/SunOS) and [IRIX](https://en.wikipedia.org/wiki/IRIX) really. Eventually I could afford a PC and found that I didn't need to walk across campus to the computer lab anymore, I could continue using all the tools I was familiar with :)

![HP-UX](/images/interviews/ttimo/hpux.jpg)
*Image credit: HP*

# With Valve, what do you typically work on?
I mostly focus on the Steam client for Linux, on the runtime for running titles, and on the Steam's build environment and compiler toolchains. I also work on the developer experience for Steam Deck with the devkit program and associated tools.

# What game engines and programming languages are you most familiar with? Is there any particular one that's your favorite? (Outside of Source 2)
I'm primarily working in C++ and Python. I keep an eye on Rust, Go, C#, Scala .. I've played with Haskell and Erlang but those are mostly just out of curiosity.

Of all the engines I've worked with idTech4 (*Doom 3*) is probably still my favorite. Daniel Gibson [maintains a modernized version](https://github.com/dhewm/dhewm3) that is very faithful to the original and Fabien Sanglard wrote a [pretty complete review of the architecture](https://fabiensanglard.net/doom3/).

Although the source isn't public, I would give an honorable mention to [Saber3D engine](https://en.wikipedia.org/wiki/Saber_Interactive). A very clean and extensible, pragmatic, "C++ first" implementation.

# Back when Valve was making a push for native Linux games, what games have you personally contributed towards making the Linux port a reality? Can you comment on what the porting process was like for any of them?
There were several but *Rocket League* and *Street Fighter V* were the two biggest ones. I think this effort drove home that as projects kept getting bigger and the visibility of Linux releases grew, we were reaching the limits of what a single person shop could do in terms of porting.

![Steam Controller pre-order offer](/images/interviews/ttimo/steam_controller_offer.webp)

Outfits like Aspyr and Feral are better positioned there but ultimately the larger the project the more studios want to retain control and be closely involved in the production and QA of the port - quite understandably.

# Back in 2015, Capcom announced that [Street Fighter V was coming to Linux](https://www.pcgamer.com/street-fighter-5-coming-to-linux-and-steamos-in-spring/). We didn't hear anything about that until 2018, when you had reported to Boiling Steam ["It's not dead."](https://boilingsteam.com/podcast-9-with-tim-besset-street-fighter-vs-port-is-not-dead/) Nowadays, we can play the game via Proton, but can you comment as to whether a native Linux build actually existed?
Right, **there was a native build.** It never got released to the public for various reasons, but when I look at it playable via Proton on Steam Deck now, I think the efforts and learnings that went into the port did contribute to making that happen.

![SFV](/images/interviews/ttimo/sfv.jpg)
*Image credit: Capcom*

# Even though the Steam Machines were met with poor reception, what are your honest thoughts about that? Do you think it helped provide the incentive for more native Linux games, or was it just a failed project?
I wasn't around during Steam Machines so I don't really have any comments there. But like *SFV* I think it greatly informed what Valve is doing now.

# Back in 2018, Valve introduced Steam Play/Proton, and with this, many, many more titles on Windows were possible to play on Linux, and the number of compatible titles continues to grow with every update. How do you feel now that your work on titles like *Rocket League* have kind of went down the drain, now that Proton has taken over? Do you still work on helping developers bring their game over to Linux, or do you advocate for Proton instead?
What I love about Proton is the options that it gives developers for bringing their game to the Steam Deck. Trying to ship a Linux port when you lack the resources, time and know-how is not a good place to be for a developer. So we remove that pain. Now **we see developers who want to ship native for the right reasons - they squeeze an extra few percent of performance and battery life**, their codebase gets battle-tested against multiple compilers and runtime environments, etc.

We've done a lot of work to provide a solid runtime environment for native titles running under Steam for Linux. Unlike Windows, there's really nothing like binary backwards compatibility and 'universal binaries' in the Linux world, and we have to make sure that the many native titles that have shipped since Steam became available on Linux continue running smoothly.

A few years back we started supporting execution of native titles in a [containerized runtime](https://gitlab.steamos.cloud/steamrt/steam-runtime-tools/-/blob/main/docs/container-runtime.md). We also maintain an SDK distributed as a container image. **It is now much easier to produce native binaries with stronger guarantees that they run well across the major Linux distributions where Steam for Linux can be installed.**

![Steam Linux runtime - sniper](/images/interviews/ttimo/sniper.webp)

Now we are beginning to roll out an updated runtime codenamed [sniper](https://gitlab.steamos.cloud/steamrt/steamrt/-/blob/steamrt/sniper/README.md), which offers updated compiler and userspace libraries. A few titles on the store are already using it.

# You had mentioned "Now we see developers who want to ship native for the right reasons - they squeeze an extra few percent of performance and battery life." Can you comment on this a bit further? How exactly does shipping a Linux binary increase performance and battery life?
**There is a bit of overhead with Proton**. It's not very much, and it keeps decreasing with the constant work to improve the technology, but it's there.

There are also other advantages. **A native build will be slightly easier to debug and fine tune performance for**. We support remote debugging with Proton and Visual Studio, but if you have a native binary it's still a little easier to work that way.

# Let's say I make a game with Unreal Engine 5. Supposedly there's the argument of, "You can export the game to Linux with just one click," but is that really true? Is there more than just the one-click export? (I would imagine it depends on the complexity of the game, whether there is middleware involved, whether some more performance optimization can be added in, etc.)
For the most part it seems Unreal Engine, Unity and Godot are truly 'one-click export' to produce a solid native build that works with Steam for Linux. Provided like you said that you haven't pulled in middlewares that do not support Linux as a target. With UE you may have a few surprises if you've never tested your setup with Vulkan and may need to tweak a few of your shaders but that's about it.

![UE 5 Editor](/images/interviews/ttimo/ue5_editor.jpg)
*Image credit: ArtificialLife Newsletter*

# What are your thoughts on the Steam Deck?
I love it! I'm biased of course, I can't be negative about working on a product that clicks so well with it's audience. Other than the devices I have on my desk for dev and testing, I don't see the 'gaming' Decks at my house much - my kids immediately appropriated them.

# What are your favorite games of all time?
That would be *Quake 3* and it's mods. It was very meaningful for me professionally but also I still hang out with the friends I made during that era. Played a lot of [*Threewave*](https://venturebeat.com/pc-gaming/threewave-valves-lost-half-life-multiplayer-mod-is-now-playable/) CTF, Rocket Arena, Urban Terror .. I'm really a pure multiplayer guy, there's not much single player content that ever caught my attention. Oh, and I played a lot of *EvE Online* for a few years .. if it's still around when I retire I might well go back to it :)

![Quake 3](/images/interviews/ttimo/quake3.jpg)
*Image credit: id Software*

# Where can people find you?
For Valve / Steam matters I can be reached at ttimo@valvesoftware.com (please don't spam me). I've dropped off all social media at this point except [Mastodon](https://mastodon.social/@TTimo).

Tim also has a [blog](https://ttimo.typepad.com/) and even his own [page on Wikipedia](https://en.wikipedia.org/wiki/Timothee_Besset) if you want to get to know him even more. In addition, he has several [GitHub repos](https://github.com/TTimo) from the likes of the *Doom 3* GPL source release, Vulkan, and Mesa.

Thanks to Tim for making himself available to be interviewed!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
