+++
title = "An Interview with Álex Román, Project Heartbeat Developer"
date = 2022-03-14T14:22:24-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ph_dev/pic.jpg"
tags = ["interview", "godot"]
keywords = ["project heartbeat", "godot", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I had the pleasure of interviewing a game developer who works on [*Project Heartbeat*](https://linuxgamingcentral.com/posts/project_heartbeat_review/) -- a rhythm-based game written in Godot 4. Álex developed this game on Arch Linux. Pretty much every tool that he used in the development process is open-source, albeit for the Steam SDK. As LGC cares deeply about native Linux games, let's get some insight into the development of *Project Heartbeat*. (Bold has been added by me.)

# Let's start off with the basics. Who are you, why you got into Linux, your history with game development, etc.

I'm Álex Román from Spain, also known on the Internet as EIREXE. I've been doing software development since I turned 8 years old, I originally wanted to be a fighter jet pilot when I was growing up but software development felt much more fun (and didn't give my family a heart attack). My relationship with GNU/Linux was a bit tumoltuous at first, but I think that's to be expected when you are doing a big paradigm shift from something like Windows into something Unix-like, something that I had zero experience with, so I spent a lot of time going back and forth and started using Arch full-time around 2017.

My stint of work before *PH* was relatively short (I am only 22 years old and the ongoing pandemic didn't help). I spent most of my late teenage years working anywhere I could. I worked at my old elementary school's IT department which was nice. My final job before *Project Heartbeat* was at a company related to a Formula 1 team as the simulator developer (and other computer-related shenanigans). I called my boss an expletive that rhymes with the word stunt (to be fair, he was one) which promptly caused me to get fired using the pandemic as an excuse, oh well. I am much more happy working on *Project Heartbeat*.

# How long have you been using Linux?

Since I was around 10 years old. [So about 12 years.]

# What's your primary distro of choice these days and why?

Arch with the window manager i3, it just works for me and my workflow, it's fast to install and easy to make a minimalist installation out of it, of course this isn't for everyone, but it is very nice for my use case.

![ph gameplay 1](/images/ph_dev/1.jpg)

# Are you a solo developer, or does EIRTeam consist of multiple contributors?

I am a solo developer, the only exception has recently been Lino, a developer from Argentina who decided to volunteer to work on some aspects of the game (particularly the editor).
The background artwork is usually commissioned from local artists such as [@Guinii4](https://twitter.com/guinii4) or [@sadnesswaifu](https://twitter.com/sadnesswaifu). Besides from that **the bulk of the 30+ thousand lines of code of the game, menu designs and graphics are made by me entirely**.

# I see from *Project Heartbeat* you're an anime fan. What anime games/TV shows have you taken inspiration from for the development of this game?

I didn't really take much inspiration from any anime in particular. It's very hard to add personality to a game people expect to work in a certain way, but I try to add some here and there.

I obtained most of my personal philosophy from a show called [*Crayon Shin-chan*](https://en.wikipedia.org/wiki/Crayon_Shin-chan) which has a very interesting history with its relationship with Spain, it's one of the few countries where it hasn't been censored. *Crayon Shin-chan* is a show with a type of humour that really fits with the people here, I find it very funny how little carefree and shameless it is, it really represents my attitude towards life.

Although I rarely watch anything nowadays (I have focus issues, so I usually listen to stuff while working) I'd say my two favourite shows I watched as an adult are [*Miss Kobayashi's Dragon Maid*](https://en.wikipedia.org/wiki/Miss_Kobayashi's_Dragon_Maid) and the anime adaptation of Nisio Isin's great [*Monogatari* series](https://en.wikipedia.org/wiki/Monogatari_(series)), they are both amazing and worth a watch for anyone.

# Did you develop *Project Heartbeat* on Linux or Windows?

I **developed it from the start on Linux**, the workflow there is just nicer and having a tiled window manager is a must for me to be any productive.

# Can you share with us what tools you used in the creation of *Project Heartbeat*? Are they all FOSS tools?

The game runs on a customized version of Godot I call the Shinobu engine, it's not really that much different from Godot but it has some nice goodies such as using ANGLE for rendering on windows, using the low latency WASAPI mode introduced in Windows 10 and other minor bugfixes that Godot was too slow to fix, so I took matters into my own hands.

The in-game note graphics are made using a very terrible python script I wrote at the start of development, it takes simple shapes and automatically turns them into all possible versions of a note graphic, it works quite well honestly. For other graphics I use Krita, most of the promo material is also made using Krita. **I generally try to use FOSS tools only, I think the only exception is the Steam SDK**.

# Do you work on *Project Heartbeat* full-time, or is it a side project?

I work on it full-time, but I am trying to find something to do, development on PH has inevitably slowed down as it becomes closer and closer to feature complete, there's only so much you can do to a rhythm game. I am currently working on a side project inspired by *Metal Gear Solid 3* using a modified version of Godot 4.

![ph song editor](/images/ph_dev/song_editor.jpg)

# What has the general feedback for the game been so far?

Generally positive, there are some hard-to-reproduce bugs that have been making me pull my hair for months, but most people are happy with it, not bad for a first try.

There was an initial resistance from people of the *Project DIVA* [a game that's very similar to *PH*] and overall Vocaloid communities, mostly on Twitter, and I suppose some still don't like the fact *Project Heartbeat* exists. I do admit I may have been a bit intentionally incendiary early on but hey, you gotta pay the bills somehow, all publicity is good publicity as they say.

# Looks like *Project Heartbeat* is available on both Linux and Windows. How have Windows users reported game compatibility?

**Windows is a nightmare** and I wish it didn't exist, particularly Nvidia, their drivers suck, Optimus sucks and particularly Optimus with OpenGL is a terrible experience that I don't wish on anyone. These issues come in the form of very strange frame pacing problems. The *Project DIVA* community faced the same problem (they play an OpenGL arcade game modified to run on PCs), their solution to all problems involves copying the OpenGL framebuffer to DX11 using some undocumented APIs (aptly named wglDX) and presenting this copied frame using old-school exclusive fullscreen, I don't understand it and I'm not sure I want to know why this is even a thing that happens.

Windows I/O is also a disaster, I am inexperienced in terms of Windows so I was unaware that Windows' performance when try to do any I/O on a file is horrible, even things as simple as reading the modification date, this is (as I understand) why most games use big container files instead of loose files, *PH* songs are in folders, luckily it's well optimized so it shouldn't be a problem, but I still would have made songs into their own container format had I known this beforehand.

Outside OpenGL and I/O woes the game just works the same on Windows as it does on Linux.

# Any interest on developing a Mac port? Maybe console ports later down the road?

I have no interest in working with Apple's platforms, I think they are a pain in the neck to work with for little gain.
Regarding consoles, there was a homebrew Switch port for a while, it's now largely been abandoned, but I think I will be revisiting it eventually, it unfortunately used Nouveau so performance was terrible, but hey, it worked...

Funnily enough the very first console version announced was an official Xbox platform port, I obtained the development tools for native Xbox One development but stopped working on it over a year ago due to concerns surrounding game censorship from major game companies and them having an (in my opinion, undeserved) control over what can or can't be sold.

# Can you share with us the percentage of those who bought the game on Linux vs. Windows?

**Around 5.6% of people who bought the game bought it on Linux**, which is a shame because playing it on Linux is the way to get the best experience in all aspects.

# How much longer do you think *Project Heartbeat* will be in early access?

I would have taken it out of early access already, but I will wait for Godot 4 before doing that, Godot 4 is pretty cool and it makes some optimizations that were previously hard or impossible to do much easier, hopefully that will happen before the end of the year.

![ph gameplay 2](/images/ph_dev/2.jpg)

# What new features do you plan on bringing to the game?

There are a few things in the making, such as a new controller macro design UI that's simplified (the current system will remain as an "advanced" mode), broader sound options for hold notes and (if I can figure out how) UI skinning.

# Any future projects or games that you'd like to work on?

I have a fear I might never be able to repeat my "success" again and that part of the future terrifies me. *Project Heartbeat* was a project tailor-made to me, extremely technical and where the thing that matters the most is the code, but this isn't true for most games, most games can get away with questionable code quality and still make money and run well (see [*Celeste*](https://www.rockpapershotgun.com/celeste-movement-code)). I personally think I have a good feeling for when something feels right and how to make it feel right, it might seem trivial but a lot of games get these fundamentals wrong. The recently revamped "Direct joystick access" system the game uses is an example of a fundamental thing but a hard one to get right. Hopefully the *MGS3* inspired game turns out good, I have high hopes for it.

# Anything else that you'd like to share with us?

You can learn more about *Project Heartbeat* at [https://ph.eirteam.moe](https://ph.eirteam.moe) and you will also be able to play *Project Heartbeat* in person at a few Spanish conventions this summer. You can follow us on Twitter at [@PHeartbeatGame](https://twitter.com/PHeartbeatGame) for development updates and even join the [Discord server](https://discord.com/invite/KtcT8Qk).

Thank you for interviewing me, it was a pleasure.

That will wrap this interview up! If you're a developer and would like to get in touch, all the details are available on the [Contact](https://linuxgamingcentral.com/contact/) page.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
