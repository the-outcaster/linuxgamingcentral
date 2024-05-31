+++
title = "An Interview with GDKChan, Founder of Ryujinx (Nintendo Switch Emulator)"
date = 2022-10-10T06:59:11-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ryujinx/interview/cover.png"
tags = ["interview", "ryujinx", "emulation", "nintendo switch"]
keywords = ["gdkchan", "ryujinx", "emulation", "nintendo switch", "splatoon 3", "xenoblade chronicles", "metroid dread", "super mario odyssey", "interview"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
When you've heard or looked up the term "Nintendo Switch emulation," chances are you'll come across one of two emulators: Ryujinx, and Yuzu. But you're probably more familiar with the latter, as it tends to be the more popular emulator. After all, Valve themselves showcased Yuzu's logo on one of their Steam Deck videos, only to [quickly take it off](https://www.eurogamer.net/steam-deck-promotional-video-removed-after-it-accidentally-showed-off-a-switch-emulator) after the Internet took the news by storm.

However, I like to give the more niche projects the spotlight they deserve. Ryujinx is no exception. It's a perfectly capable emulator; it can even [handle emulation on Deck pretty well](https://linuxgamingcentral.com/posts/ryujinx-vs-yuzu-tested-on-deck/) in most cases. And as the founder of the project, **GDKChan**, brings out in this interview, in some instances it outperforms Yuzu when it comes to stability and compatibility.

I always enjoy talking to GDKChan. [I interviewed them last year over on Boiling Steam](https://boilingsteam.com/an-interview-with-gdkchan-creator-of-ryujinx/), and their answers blew away my mind. It felt like I was immersed in another world as they freely expressed what was on their mind, and in the process, I learned quite a few new things as well. So I wanted to sit down with them again, see what their thoughts are on the Steam Deck, how the reception has been now that [Vulkan has been merged into the main branch](https://linuxgamingcentral.com/posts/vulkan-now-merged-with-ryujinx-main-build/), and some of the things we can look forward to with this fantastic emulator.

Note that this interview contains some minor edits for spelling/grammar fixes. Bold has been added by me.

**TL;DR**
- Ryujinx was launched to the public in February 2018 and was the first emulator to successfully emulate commercial titles
- Ryujinx should be picked over Yuzu for compatibility and stability purposes
- the Vulkan backend has mostly been met with very positive reception, albeit for NVIDIA users on Linux, since there wasn't much of a performance gain there
- some AMD-specific fixes were added to the Linux version of the emulator thanks to one of the devs owning a Deck
- it was relatively easy to package Ryujinx as a Flatpak, but more difficult to get it to conform to Flathub's standards
- gdkchan primarily develops on Windows, but they did use Linux for a while when improving the GPU performance of the emulator, due to better Intel driver support
- maintaining two separate versions of the emulator (Linux/Windows) is a bit of a hassle when it comes to driver support
- LDN will become open-source once it utilizes UDP (rather than the TCP it uses now) and the `ldn_mitm` custom sysmodule
- it's unlikely that the Denovo DRM will affect those emulating Switch games
- the name "gdkchan" comes from the "G" in the founder's name, with "DK" being short for "dark." "chan" is a Japanese honorific
- their profile picture comes from *Kimi ni Todoke*, a Shoujo romance manga
- games that they like to play include *Diddy Kong Racing*, the *Shantae* series, the *Phoenix Wright* series, and *Monkey Island*
- what the community can do for the project: get familiar with C# and contribute directly, test changes, find regressions, test games on specific hardware, contribute financially
- new feature to look forward to: the Avalonia UI and some other goodies

# Explain who you are and what led to the creation of Ryujinx.
I'm known as "gdkchan" and over the years I've made a few emulators for fun; probably the only one that is noteworthy is Ryujinx, which is a Nintendo Switch emulator written in C# with a fairly high level of compatibility.

Ryujinx started as an Arm64 emulator. .NET, much like Java, works by compiling the code to an intermediate language (IL), rather than to machine code that the CPU can execute directly. This IL is then compiled to machine code when the program is actually executed using a JIT (Just-In-Time) compiler. So, the crazy idea that I had at the time was "translating" the Arm code to IL, and the built-in .NET JIT would then compile that to machine code that could be executed on the PC CPU. What could go wrong?

It started as a simple CPU emulator, but ultimately my goal was using it as a Nintendo Switch emulator. The Switch was a new console and there were no emulators for its games yet, or at least no emulators with video output that could run commercial games. I also enjoy Nintendo games, having had a Game Boy as a child; in fact, I still have a Game Boy and some cartridges. So, it just seemed like the perfect opportunity to make a Switch emulator and, just like that, in December of 2017 Ryujinx was born.

![ARM processor](/images/ryujinx/interview/arm.jpeg)
*Image credit: Arm*

However, it was not until February of 2018 that I actually released the emulator to the public. My goal for a release was having at least one commercial title rendering graphics in the emulator; personally, that's when I think things start getting interesting.

Working on this emulator was a big step forward for me, since the most recent system I had emulated in the past was the Game Boy Advance, which did not really require a JIT recompiler nor re-implementing an OS. Plus, of course, the Game Boy Advance possesses much simpler hardware and, while it had an Arm CPU, it was a much older model (ARMv4 compared to the ARMv8 CPU on the Switch). 

# Why might a person pick Ryujinx over Yuzu? 
To the best of my knowledge, the most popular reasons a user would pick Ryujinx are for its **stability and compatibility.** Historically Yuzu has had stability issues, with games crashing after some time playing, and generally it has a lower compatibility with games. I think most people are interested in emulating first-party titles, so this difference in compatibility usually only becomes apparent for them when a new release works on Ryujinx but not Yuzu. This has happened with many games, and we don't need to go too far back for examples.

*Splatoon 3* (which at the time of writing, was just released a few weeks ago and is the most recent first-party title) boots on Yuzu but with some issues. First, an eShop dump does not work at all on that emulator due to unimplemented file system service functionality, so the only option is to use a game cart dump. On top of that, it has graphical issues and, from what I was told, the game crashes on some AMD GPUs. Ryujinx does not have any of those issues. In particular, the file system functionality that *Splatoon 3* needs is something we implemented several months ago to fix some niche indie multiplatform games (which I guess most of our users won't care about). But it just goes to show how important fixing niche games can be to ensure future "big" titles will work on release.

![Splatoon 3](/images/ryujinx/interview/splatoon_3.webp)
*Image credit: Nintendo*

Another recent case where a first-party game was working on Ryujinx first was *Fire Emblem Warriors: Three Hopes* which did not work at all on Yuzu on launch, but worked on Ryujinx. In fact, one of our progress report writers tested this game on an old build from 2021 and, even then, this game worked. Of course Ryujinx also has many issues left to iron out, but its stability and compatibility overall is better than Yuzu's.

# After many months of hard work, [Vulkan has finally made it to the main branch](https://linuxgamingcentral.com/posts/vulkan-now-merged-with-ryujinx-main-build/). How has the reception been so far? 
From what I have seen, the reception has been **overwhelmingly positive.** The shader stuttering on first run was a very common complaint, and most people did not know it was due to the slow GLSL compilation; SPIR-V really made a big difference there. Plus, AMD GPU or Intel integrated GPU users can reliably use the emulator now. Some games did indeed work with OpenGL before on those vendors, but it was really hit or miss, and some were agonizingly slow.

**I think those disappointed with Vulkan are mostly NVIDIA users and Linux users that expected a large top-end performance improvement. The NVIDIA OpenGL driver and Mesa on Linux have decent OpenGL support**, so getting a performance improvement out of Vulkan is much harder. People often tend to compare it to improvement on PC games, but it's not a valid comparison. PC games have significantly more flexibility to adapt to the API and provide what it needs: for example, information about how a particular resource will be used in future gameplay. As an emulator we don't have this information because it's out of our control, and entirely up to the game.

# Do you have a Steam Deck, and if so, what are your thoughts on it?
I don't have one, and currently do not have any plans to get one. I might consider getting one in the future, since there are clearly a significant number of people interested on Switch emulation on the Steam Deck. I don't think I'd use it much outside of Switch emulation development, though. We do have a developer on the team that owns a Steam Deck and has fixed some Linux AMD-specific issues affecting it.

![Metroid Dread on Deck](/images/steam_deck/dread.jpg)

# A few months ago, [Ryujinx got the Flatpak treatment](https://linuxgamingcentral.com/posts/ryujinx_now_on_flathub/), allowing users to easily install the emulator on their Deck. On a scale of 1-10, how difficult was it to get the Flatpak version working?
I was not the one that made the emulator available on Flatpak, but I think it was not too complicated. From what I recall, it mostly required some changes to the locations in which the emulator stores logs and a few other files, then setting up the appropriate pieces on GitHub to pull the code from our repository, and finally handling the publishing of the package.

That being said, I got a response from one of our developers, **Thog/Marysaka**, who has a Deck and handled the Flatpak process:
> I would probably say 3 for Flatpak but 8 for the upstream on Flathub. Being able to get a Flatpak package up and running was for the most part trivial but integrating with Flathub (the most popular repository for Flatpak applications) required some rethinking of the build progress. Flathub enforces that every app should build on their own infrastructure without any Internet access (apart from the initial step that fetch external resources) and that conflicted a bit with our release model.

# How familiar are you with Linux? Is it your daily driver or do you stick with Windows/MacOS?
I can use Linux and know the basics; it's not my "main" OS. **I usually use Windows, and only switch to Linux when there's something specific that I need to test there.** I did use Linux as my main OS for several months in 2019 though. The main reason for that was because I was improving GPU emulation in the emulator, and only had an integrated Intel GPU to test with. The proprietary Intel driver on Windows was simply awful. For my specific GPU, the driver only supported OpenGL 4.1, and even then it contained a lot of bugs. The open-source Linux driver, in comparison, supported OpenGL 4.3 and even Vulkan 1.0. Eventually I upgraded to an NVIDIA GPU, at which point testing on Windows was no longer an issue.

![Xenoblade Chronicles on Ryujinx](/images/ryujinx/interview/xenoblade.jpg)
*Image credit: MutantAura*

# Is it difficult maintaining three different versions of Ryujinx (Linux/Windows/Mac)?
Sort of, but **the main difficulty doesn't come from the different operating systems; the different drivers are the real issue.** There are some peculiar qualities between them that we have to account for on the emulator: distinct calling conventions (these dictate how parameters are passed to the functions, and how values are returned. Linux and MacOS follow the System V convention, while Windows has it's own), differences in memory management, and a few other particulars. Linux and MacOS are both "Unix-like" operating systems, so usually we just use the same code path for both. Occasionally there are some restrictions or differences that we need to account for on one OS or the other, but nothing too complicated really. And, **out of the three operating systems, Linux is usually the most flexible.**

Supporting the various drivers and GPUs is the hard part. Windows can only use proprietary drivers from each vendor. For Linux there are open-source drivers and, in some cases, also proprietary drivers in addition to that. Graphical issues that occur on Windows might not affect Linux and vice-versa. This complicates things because we need to constantly switch between OSes to test these things. Sometimes there's more than one driver to test on Linux, and sometimes issues only affect a given GPU architecture (which we might not have available for testing).

We don't support MacOS right now but when we do, the situation will get even more complicated for sure. If we go with MoltenVK, there are a bunch of unique limitations that no other Vulkan driver has. Since MoltenVK is just a translation layer that ultimately makes Metal (Apple graphics API) calls, it inherits all of Metal's limitations. And older x86 Macs have Intel integrated and AMD GPUs, which will likely be rife with unique issues too.

# What's the status of the [LDN local wireless](https://linuxgamingcentral.com/posts/ryujinx-ldn-2.5-released/)? Will it be eventually fully open-source?
Currently we want to support connections to/from a modified Nintendo Switch with the `ldn_mitm` custom sysmodule, but there are a few obstacles to getting that working. As for our own implementation that allows connection between emulator instances on the Internet, I think it's working mostly okay. There are some games where it doesn't work, though, and various connection issues. We have been planning to switch to the UDP protocol for quite some time (currently it uses TCP), but that work is not done yet. This is also what's stopping us from open-sourcing the code, as we don't want to release an incomplete feature that has significant architectural changes yet to occur. I believe that once we switch to UDP, many of the stability and compatibility issues will be solved too.

![Ryujinx LDN 2.5 with Mario Kart 8](/images/ryujinx/ldn_2.5.jpg)
*Image credit: Ryujinx team*

But yes, **LDN will be open-source eventually**, for other reasons as well. In particular, rebasing LDN each time around to have all the latest improvements takes quite a bit of work; work which could be avoided if we just merged it with the master/main branch of the emulator.

# What are your thoughts regarding [the new protection for Switch games against emulation](https://linuxgamingcentral.com/posts/drm-coming-to-emulated-switch-games/)?
I didn’t see this coming, to be honest, but **I don't think it will affect us much.** Most people are interested in emulating first-party games, and it's very unlikely that such titles will ever use this "protection". Irdeto already stated that Nintendo is not involved in this; for their part I believe Nintendo would have developed their own solution against emulation by now, if they desired such a thing.

In general, I don't think Denuvo for Switch games makes sense. I doubt that the number of people emulating pirated Switch ports of games available on PC is significant or at least it does not have a significant impact on sales. I don't have solid numbers on this (and they don't either, as indicated on their post), but emulating a Switch game is not really comparable to running a native PC version of a game. Emulation is much more demanding which means the user will need to have high end hardware to ensure an optimal experience. Then there are the other emulation-specific complications: the shader stutters, potential graphical glitches, and the fact that the Switch port of a game almost always looks worse than the same game on PC due to the Switch’s inherent hardware limitations. When you take all that into account, it's hard to believe someone willing to go through all that trouble would actually buy the game if the emulation route was not an option. This Denuvo solution also most likely doesn't (and can't) do anything about piracy on the Switch itself, which is by far where most of the pirated games are being played (on hacked or modified Switch consoles, that is).

I have some ideas of what they might do to detect emulation, although we can't say for sure until a game using the "protection" is released. The obvious solution to whatever their detection algorithm may be is to just make the emulator more accurate; but accuracy always comes at the cost of performance. This is very important for newer consoles, since they are much more demanding to emulate than the older ones. As a result, we often need to take shortcuts to make games run at a reasonable speed. These shortcuts can be broken fairly easily by someone motivated to harm the successful operation of an emulator. The main problem is GPU emulation. To get decent performance we need to use the host GPU, which limits us to what the host graphics API allows us to do.

![Denuvo on Nintendo Switch emulation](/images/denuvo_switch/cover.jpg)
*Image credit: multiplayer.it*

One example of this is indirect draw. An indirect draw is a draw command where the parameters are fetched from a GPU buffer that can be written by a shader. This is something that any modern GPU and API supports, but on NVIDIA it is implemented using a Macro, which is a small program that runs on the GPU and can submit more commands, in addition to being able to read and write GPU registers. For indirect draws, the driver calls a Macro program that will read the draw parameters from a buffer and then submit the draw commands using those parameters. The only performant way to emulate this is by pattern matching the Macro program on the emulator, and then performing the indirect draw using the host API. This is more of a high level (HLE) approach, as we recognize specific code and replace it with our own implementation. It is also something that can easily break, since any change to that Macro program would stop the emulator from being able to recognize it, and then it would trigger a much slower path to emulate the indirect draw. This is just an example, and it wouldn't even be much of an issue in this case since there is at least a slower path in place, so it would still “work”. But there are a few features where we depend on this kind of pattern recognition in order for it to work at all, because there's just no way to emulate it otherwise while still using the host GPU.

Another thing to take into consideration is that the Switch is a rather "locked" platform. Certain methods that are used on PC games to make reverse engineering harder, for example, can't be used on the Switch, as it does not allow dynamic code generation (along with other limitations). The Switch also does not allow direct access to the hardware, which limits the kinds of checks they can do. There's also the fact that the checks and code obfuscation techniques they may use will make the game run slower, which is a moderately significant issue as well, considering that the Switch already struggles to run certain games. They could limit the checks to only occur during some loading screen, for example, to prevent it from actively slowing the game down, but then it would also be easier to patch it out. And, whatever they do, it will most likely break on a potential backwards-compatible Switch successor.

Ultimately, I think this is something that will hurt the legitimate consumer more than a potential pirate who is using an emulator. All that work just to attempt stopping a small number of people that most likely would never buy the game anyway; it just doesn't make sense. Hopefully not many (or any) third-party developers will use this.

# Where did you come up with the name "gdkchan"? Any special meaning behind it?
The "G" is from my name, while "DK" is just a short version of "Dark". The name I was using before gdkchan had "Dark" in it, so I just shortened that. I was around 14 when I came up with it and the "Dark" sounded cool back then I guess. And "chan" is a Japanese honorific; it's technically not correct to use it as part of a name but, well, people do that. I think the reason I included the "chan" was because just "gdk" is too short and would likely be already taken if I tried to register it somewhere. I think it works pretty well. It's short, easy to type, and easy to remember.

# Origin of your profile picture?
It's Kuronuma Sawako from *Kimi ni Todoke*, a Shoujo romance manga. She is a shy character, and often misunderstood. She is called "Sadako" by her classmates, which is Samara's name on the original Japanese version of *The Ring* movie (Ringu). The nickname is probably due to her poor communication skills and some resemblance to the girl from the horror movies (like the long, black hair), and similarity of the name too. There are even some rumors that if someone looks at her eyes directly they will be cursed. Once people get to actually know her, they find she is actually a very nice and hardworking person.

![Kuronuma Sawako](/images/ryujinx/interview/gdkchan_pfp.jpg)

This specific image is from the ending of the first season of the anime. I liked the art style there, and the chibi Sawako, so I decided to use it as a profile picture. I think this happened in 2015 or 2016; I haven't changed the profile picture since then as I think changing it can be a little confusing for others, after someone has associated a specific person to the old profile picture. At least it is for me. When I see people constantly changing profile pictures and names on Discord for example, and then the person messages me again, I need to take a moment to look at the chat history to find out who the person actually is.

# What's your favorite game of all time? Second? Third?
That's a tricky question. I haven't played many games, especially over the past couple of years. Currently I spend most of my free time programming and trying to improve Ryujinx. Rarely do I take the time to actually sit down and finish a game.

But back to the question: it's hard to pick a favorite. There are many games that I like, but they are vastly different so comparing them is hard. I had a lot of fun with *Diddy Kong Racing* on the Nintendo 64; it's easily my favorite kart racing game. One thing about it that makes it stand out is the selection of many different modes of possible gameplay. The game features three types of vehicles: a car, airplane and hovercraft. It also has a great adventure mode that is perfect for single player. In fact, basically all Rare (Rareware) games for the Nintendo 64 were great. I'm still impressed by just how much content they managed to pack on *Conker's Bad Fur Day*. The game is fully voice acted too! It's hard to believe all that could fit on a Nintendo 64 cartridge. When you look at a newer system like the Nintendo Switch, sometimes even a simple visual novel contains several gigabytes of data.

![Shantae Half Genie Hero](/images/ryujinx/interview/shantae.jpg)
*Image credit: WayForward*

*Shantae* is a game that I discovered more recently, which nowadays is known for being a somewhat obscure Game Boy Color game. Eventually I played some of the newer *Shantae* titles and really enjoyed them; they're some of my favorite 2D platformers. The first game really stands out on the Game Boy Color, and now all *Shantae* games are available for the Nintendo Switch. On top of that, they are all working on Ryujinx. Actually, *Shantae* is one of my go-to games for testing when implementing a new graphics API or porting the emulator to a new platform. Since it's a fairly simple 2D game, it's usually easy to get running.

There are some games that I was not expecting to like at first, such as *Phoenix Wright*, which is an investigation/questioning game, and really funny one at that. I've also played a few older Lucasfilm Games point and click adventures too, with *Monkey Island* being my favorite among them.

# How can the community get involved with the project? What's the highest priority?
Any programmer that knows a little bit of C# can contribute to the project directly. Even without any prior experience working on a emulator, there's a lot of things that needs to be done and only requires basic knowledge. It's also a great way to learn new things for those interested in emulation. Other than that, we also always need someone to test changes, find regressions, test games on specific hardware (like AMD GPUs). Even just hanging out on our Discord can be helpful, we always have people in need of help for setting the emulator up or getting a game to run, and those a bit more knowledgeable can help with that. We also have a [Patreon](https://patreon.com/Ryujinx) for those that can contribute with money, it's greatly appreciated.

![Super Mario Odyssey on Ryujinx](/images/ryujinx/interview/smo.jpg)
*Image credit: MutantAura*

As for the highest priority, personally I think it's **improving the core emulation.** It's also the hardest component to get contributors for. When we get people contributing to the project, it's usually on the UI. Our CPU emulator is lacking some optimizations, some Arm instructions have slow implementations, some help on that front would be nice. We have a new contributor now (**Wunkolo**) working on AVX-512 support. I can't test it myself right now as I don't have a CPU that supports those instructions (I might get one soon-ish), but would be nice to get faster implementations using the older SSE and AVX instructions too, for the older CPUs. **LDj3SNuD** has also made some significant improvements recently (which, for those not aware, has helped a lot with instruction implementations, optimizations and tests in the past).

Another thing I would like to see is **a better way to track our compatibility.** Currently we use [GitHub](https://github.com/Ryujinx/Ryujinx-Games-List/issues) to keep our compatibility list, it sort of works, but it's not really ideal when you need for account for multiple reports. Sometimes games behave differently on different hardware. It also needs some manual work on our part to update the main post with the most recent information, and labeling. Would be nice to get a system that could handle this better, since the GitHub issue tracker was not really made for that.

# Anything we can look forward to as far as new features to the emulator?
Our main focus right now is improving the existing features. For example, we want to allow LDN to connect with modded Switch consoles in the future (which I guess one could consider a new feature). There's the **Avalonia UI** that has been in the works for quite a while. It will finally bring localization support to the UI, so our users will be able to use the emulator in their native language rather than English. It also has a few other quality of life improvements.

![Ryujinx with Avalonia UI](/images/ryujinx/interview/avalonia_ui.jpg)
*Image credit: [emmauss](https://github.com/Ryujinx/Ryujinx/pull/2507)*

When Avalonia becomes the main UI, I want to work on some features like a memory editor and maybe a disassembler. It will useful for people making game mods. I'm not sure when that will happen though, as I already have other things planned that will probably take priority.

# Anything else that you want to share with us?
I want like to thank you for this opportunity. I enjoy talking about emulation and it's not every time we get to do this. We often get questions like "Is there any project in the works to improve performance" or "When will X issue get fixed"; finding someone interested in how the emulator works, how it started or just thanking us for the work we did so far is a lot less common.

We have a small surprise to show in the next few months that I think some of our users will enjoy, so look forward to it!

That wraps this interview up. Check out some of my other articles on Ryujinx if you'd like to learn more:
- [Ryujinx VS. Yuzu on Deck](https://linuxgamingcentral.com/posts/ryujinx-vs-yuzu-tested-on-deck/)
- [OpenGL VS. Vulkan on Deck](https://linuxgamingcentral.com/posts/switch-emulation-on-deck-opengl-vs-vulkan/)
- [LDN 2.5 release notes](https://linuxgamingcentral.com/posts/ryujinx-ldn-2.5-released/)
- [How to use *Smash Ultimate* mods](https://linuxgamingcentral.com/posts/guide-use-mods-with-ssbu-on-ryujinx/)

Also, be sure to check out the [interview from last year on Boiling Steam](https://boilingsteam.com/an-interview-with-gdkchan-creator-of-ryujinx/) as well! There you can also find a [guide](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) on how to get your backed up Switch games running on Linux. Steam Deck HQ has a [guide](https://steamdeckhq.com/tips-and-guides/setting-up-emulation-with-emudeck/) if you want to get emulation set up on Deck.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
