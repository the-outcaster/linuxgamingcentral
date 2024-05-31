+++
title = "An Interview with Samus Prime, Founder of Metroid Prime Remastered (And Some Other Devs/Artists)"
date = 2022-10-11T08:05:46-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/mpr_interview/cover.jpg"
tags = ["interview", "metroid", "emulation", "mpr", "metroid prime"]
keywords = ["metroid prime", "metroid prime remastered", "mpr"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As someone who is quite fond of *Metroid Prime*, I had an opportunity to chat with a few of the developers/artists behind *Metroid Prime* Remastered (MPR). MPR is an unofficial mod that, as the team brings out in this interview, greatly enhances the lighting, shading, and overall graphics quality of the gem that was released 20 years ago. And because it's using PrimeHack, it also incorporates all the benefits of that, including keyboard and mouse controls, dual-stick controller support, and an adjustable field of view slider. MPR also allows you to customize the in-game HUD, change Samus' suit colors, and so much more.

For this interview, I got, not just one person, but *three* people that are part of the entire team:
- Samus Prime (SP): founder of the project
- Ray3D: lead texture/lighting artist
- SirMangler: lead programmer

So most questions will have three different answers. Here we'll find out how they got into the *Metroid* series, what their favorite hobbies are, what their thoughts are on the Deck, and if MPR will ever see a Linux version (it has to be used through Bottles/Wine for now). They're also looking for more artists to join the team, so if you happen to have skills in that area, they would certainly appreciate the help.

![MPR Samus in space](/images/mpr_interview/screenshot1.jpg) 

*Note: responses have been edited for minor spelling/grammatical errors.*

**TL:DR**
- MPR is a fork of the Dolphin emulator with keyboard and mouse controls, dual-stick controller support, adjustable field of view, along with stunning upgrades to the visuals of *Metroid Prime*
- nine people currently make up the MPR team, ranging from programmers to artists
- the team is quite fond of the Deck, and are impressed with how customizable and easy it is to use
- a native Linux version of MPR is planned, though we don't have an ETA as to when that will happen
- the team is looking for more artists; if you'd like to get involved in the project, reach out to them

# So, explain who you are and the projects you're involved with.
**SP:** My name is Jason. I am the creator of [Samus Prime](https://www.youtube.com/c/SamusPrime), a YouTube channel dedicated to my passion for *Metroid*. In 2018 I started working on MPR and founded the project along with Ray 3D. I also produce music and have been involved with several projects.

**Ray3D:** I am Ray3D, I am a Lead Texture and Lighting Artist on Project MPR. In my day jobs, I work as Senior Surfacing Artist for an animation studio and also teach as an instructor in Game Dev and Animation at a Vancouver-based college.

**SirMangler:** I'm the lead programmer in MPR, professionally I'm a contracting software engineer. The biggest project I'm involved with aside from MPR is [PrimeHack](https://github.com/TheDrifter363/primehack), a big component of MPR that introduces all of the fancy new controls and some graphics settings like FoV. That's where I learnt most of what I know about reverse-engineering and writing in PPC (assembler), thanks to shio. PrimeHack started separately from MPR in 2018, though I joined when most of the work began around 2019.  I'm also working on my own project, a "Twitch Plays" hack for a *Pokémon* game, though it will be far more complex and silly than normal as it will literally alter the gameplay at the whim of the viewers.

![MPR Phazon Suit](/images/mpr_interview/phazon_suit.jpg)
*Image credit: MPR team*

# What are your favorite hobbies?
**SP:** Gaming of course. I also love to hike and trail run, I live literally right by the mountains and I love nature. I also love playing basketball and am a huge Utah Jazz and San Fransisco 49er fan.

**Ray3D:** Making 3D art used to be a hobby for me until it became a job. I am always thankful that I was able to do such a thing. I still spend a ton of time outside of work on my own personal art projects. I hope to have an IP of my own in the near future. Aside from that, I enjoy modifying electronic devices and getting my hands dirty with some DIY projects usually involving things like hardware mods for consoles and entertainment/studio setups.

**SirMangler:** The most consistent hobbies I have are procrastination, programming, [and] coffee. If I get more time, I'd like to work on Linux support for *Xenia* and reverse-engineer *Animal Crossing* to figure out how it's entity system works. 

# What got you into the *Metroid* series? Any game in this series that is your favorite?
**SP** *Super Metroid* changed my life. That game made me a gamer and is the reason why I love the series. *Metroid Prime* and *Metroid Prime 2: Echoes* are also right at the top all time. Playing those games were always an escape from some difficult times. I would get lost in the music and atmosphere of those game for hours. I still play and finish them every year.

![MPR Samus scanning an enemy](/images/mpr_interview/screenshot2.jpg) 

**Ray3D:** *Metroid Prime* was probably the first AAA game I played as a kid when I was a about 8 years old. However, I really couldn't play that game much as my tiny brain could hardly process it's stunning complexity. However, that game always lingered in the corner of my mind as I always recalled it having a great atmosphere. I finally had the chance once more, to revisit that game when I was 15 with the *Trilogy* re-release on Wii. Throughout my high-school summer break, while all my friends were busy playing *Call of Duty* on their PS3, I sunk my teeth into *Metroid Prime Trilogy*. While they were obsessed with raw graphical prowess of the PS3, I remained enthralled by the atmosphere of *Metroid Prime*. 

The feeling of isolation and exploration still evokes a thrilling feeling inside. From exploring the dusty Chozo Ruins in *Prime 1* to the sprawling technological marvel that is the Sanctuary Fortress in *Prime 2*, I can vividly recall feelings of isolation, awe, wonder and dread (pun intended) all at the same time during my first playthroughs. Video games seldom do what the *Prime Trilogy* does so well that is; "Show! Don't Tell". *Metroid Prime 2: Echoes* is no doubt my favorite in the franchise as they took everything that made *Prime 1* great and improved it. From exploration down the minute particle effects.

*Prime 2* embodies the "Show, Don't Tell" principle so well that I would recommend people new to the games industry to study that game in great detail. In recent memory, *Elden Ring* is one of the few games that embodies that principle really well.

![MPR Samus Dread suit](/images/mpr_interview/screenshot3.jpg) 

**SirMangler:** My elder brother bought and played the *Metroid* series. I played it on GameCube and then on Wii through *Trilogy*. I'm quite fond of *Prime 3*, as silly as some of the motion controls were and tedious that the aiming could be. Grapple lasso always felt fun, especially towards the end of the game. The accessibility we've brought to *Prime 3* in terms of controls makes me proud. It's possible to make a close approximation of the GameCube controls for *Prime 3* now. 

# MPR -- explain what this is for *Prime* fans and the benefits they get with this over vanilla *Prime*.  
**SP:** MPR is a modded version of Ishiiruka Dolphin that utilizes forced lighting which allows us to add things like material and cube maps into *Prime*. It also allows us to control the game engines dynamic lighting and more of it to make scenes even more amazing. It also has some other really fun features like the ability to choose different versions of Samus' suits and customize the games HUD and reticle. There is even more we are working on but not ready to talk about yet. I promise it will be worth your time if you're a *Prime* fan.

**Ray3D:** Project MPR is a remaster of *Metroid Prime 1*. A much needed visual update to a legendary game that fans have been craving for the past 10 years. Outside of just visual updates to the textures we have added many quality of life improvements to the game as well. For starters, every texture has been given not just a resolution upgrade but also material maps. Now every texture interacts with the lights in game in a more realistic manner. On top of that, there is also a dynamic lighting system, which SirMangler worked really hard to implement, that really make all those HD textures and materials pop. We also have higher resolution baked lighting thanks to the Metaforce team which is now far more accurate and rendered using Blender's path traced Cycles engine. 

One of the biggest additions is no doubt PrimeHack which incorporates a proper dual-joystick and keyboard-mouse support for the *Metroid Prime* [series]. It really goes above and beyond just a visual upgrade. And one day will be the definitive way to play *Prime 1*.

![MPR Samus vs. Parasite Queen](/images/mpr_interview/screenshot4.jpg) 

**SirMangler:** MPR is a love letter to the *Metroid* games. For us we can express how important this game was, and we can follow in the footsteps of the original developers by working with, and recreating their work. We want MPR to be the definitive way to play. Everything is optional and tweakable. You can play *Prime* as if it were a remake, all the fancy new textures and materials and lighting, new controls, etc. Or you can treat it as a coat of new paint. Original controls, and new textures and increased FoV to suit your modern high-res monitor without removing from that "original GameCube" feel.

# How many people are working, or have worked, on MPR?
**SP:** We currently have nine people that are on the development team. We also have team members who contribute their knowledge from their own respective projects, such as Antidote ([Metaforce](https://github.com/AxioDL/metaforce)) and Tino B (Ishiiruka Dolphin). So even though they aren't actively developing MPR, their knowledge has been paramount in our ability do to so. We have had some others come and go, the biggest contribution coming from Mr. Mendelli.

# You all have a Steam Deck. What are your thoughts on the device?  How has the learning curve -- considering most of you have never touched Linux -- been with the software experience? 
**SP:** I love my Steam Deck. It blows my mind to see full-fledged AAA PC games being played in the palm of my hands. I also love that Valve has kept the platform completely open. The truth is I haven't had a lot of time to dive into Linux and all the amazing options available for the Deck. My personal work and family life, along with MPR take up the majority of my time so I've only been able to do some quick gaming here and there on the Deck. But I love it, and it definitely gives me the ablility to game when I probably wouldn't have before. I am still really looking forward to getting all my emulators set up, especially Dolphin.

![SP's Deck](/images/mpr_interview/sp_deck.jpg) 
*Image credit: SP*

**Ray3D:** The Steam Deck is a great console, it might just be my favorite of all time. In a world of increasing "walled-garden" ecosystems, where companies slowly take away the freedom and control people have over the devices they purchase. For example even Android (supposedly open platform) -- phone manufacturers pull shady tactics like disabling hardware features such as the camera for simply unlocking your bootloader. The Steam Deck is a much needed refreshing change of pace. It is a truly open platform that allows you to tinker, tamper and tweak (TTT) as you like. 

The Desktop Mode is perhaps it's best feature as it really extends what the Steam Deck is capable of outside of just a gaming device for Steam-only games. It truly feels like I own the device and not the company making it. It is a "personal console." It is the direction I wished [the] mobile phone industry took years ago with regards to gaming. Whether it's playing your Steam Library, old PC games or emulators, the Steam Deck does it all with little to no friction. While not everything might run perfectly, it mostly does. And I have no doubts things will improve over time.

What really got me to buy the Deck was the sheer amount of community content and support surrounding the system. There is almost always a solution to any problems that you might encounter. While Arch Linux can seem daunting for first time users, there are tons of guides, videos and subreddits to [use]. As someone who likes to tinker around and go exploring in order to try to understand the inner workings of a device, it was surprisingly a lot easier so far than what I originally expected. There are certainly a few things that can be quite the departure from Windows. Things like connecting to a VPN don't always have a proper GUI and instead require you to use simple commands in the Terminal.

![Ray3D's Deck](/images/mpr_interview/ray3d_deck.jpg) 
*Image credit: Ray3D*

What surprised me was that I actually preferred some crucial things like Dolphin File Explorer over the Windows File Explorer. Most day-to-day applications are available for the platform and can be acquired through various means. I can even do some 3D art using Blender on the Steam Deck. The most impressive moment I had with it thus far was running an old childhood game -- *Chamber of Secrets* for Windows on the Deck. And it ran flawlessly, better than Windows itself. While it takes some time to understand some technical aspects such as compatibility layers, Wine or Proton, it's well worth learning about it as it really opens up the possibilities of what you can do with your Deck. I only wish nothing but success for the Steam Deck as I hope it sets of a trend in the industry of having more open platforms.

**SirMangler:** I daily drive a Steam Deck, unironically. My old laptop broke and I simply do not need a new one. Learning curve might be a little tedious to new users trying to follow the archaic Windows-isms, but I had prior experience with Linux. To someone interested in dipping their toe into linux, I say, the Steam Deck is perfect. Just try to think of it as something completely new, and modern. Try do it the Linux way, or the Arch way, which is usually always one or two simple terminal commands. If it feels like it's too complicated, then you need to find a better guide (AKA something not on the Arch website), or take a few steps back. And remember, **Valve butchered most of the arch-pacman packages, you need to reinstall them or you'll have a nightmare of a time!**

![SirMangler's Deck](/images/mpr_interview/sirmangler_deck.jpg) 
*Image credit: SirMangler*

# Will MPR ever get a native Linux version?
**SP:** I really hope so. We've looked into it and have had some limited success but it's not where we'd like it to be. There are some other options out there such as Metaforce (which we have full intention of supporting when it's ready) and also the possibilty of the main fork of Dolphin to add support for material maps. If either of these become a reality, making a native Linux version of MPR will definitely be on our list of to-do's.

**SirMangler:** I don't own a device with Windows on it and shio, the creator of PrimeHack, also daily drives Linux. Believe me, we feel your pain. Let me break down where we sit:
- MPR is the culmination of a lot of work. It goes Dolphin Emulator -> Ishiiruka -> PrimeHack -> MPR 
- Ishiiruka is a fork of Dolphin Emulator, from roughly five years ago. We must use Ishiiruka for our visuals (materials, bumps, cubemaps, specs and phong/forced lighting). Back then, Linux support wasn't great
- Linux cannot run DirectX, so you're limited to OpenGL and Vulkan
- Vulkan is experimental in Ishiiruka, it's been known to corrupt the cache and either crash blatantly or cause performance tanking. When I try to use it, all my visuals are hue shifted (everything is green and purple)
- OpenGL is slow, and has bugs causing it to not render some of our visuals properly. It also doesn't support material maps/bump maps, causing our textures to look flat and not responsive to light

I compiled MPR for Linux; it took a great deal of time to fix the various issues and find the necessary dependencies. But it was really buggy. It would crash if you sneezed too loud. Right now, running this under a compatibility layer such as Wine seems to be the most stable way to play. Linux Gaming Central got Vulkan to work, which is awesome.

![MPR Samus' ship](/images/mpr_interview/screenshot5.jpg) 

So is that it for Linux? Not at all. We have no intention of being glued to a five-year-old build of Dolphin forever. And until then, hopefully we can pave the way for better stability in the mean time. **I want a native build for Linux for development alone. I do not want to work on MPR in a virtual machine forever.** Until then, I recommend you check out Linux Gaming Central's [guide](https://linuxgamingcentral.com/posts/metroid-prime-remastered-on-steam-deck-guide/), it's my personal recommended setup. 

# Is there anything the community can do to help contribute to the project?
**SP:** The community has been great and we love the response the project has received. Their are several ways you can help us out. First, **we need more artists.** We have more than we've ever had, but life happens and as such, not everyone can actively contribute at once. We have four artists working on textures and materials right now; the more we can get actively contributing, the faster we can get the full project out.

We also have a [Patreon](https://www.patreon.com/join/aetherlabs?) if you'd like to support us that way. We have some really fun rewards including some cool custom Samus suits and monthly pictures and up-to-the-moment looks at where we are with Phaze 2 of MPR.

# Anything we can look forward to in the future with MPR?
**SP:** Absolutely. I can't wait to show you.

![MPR Samus in morph ball mode](/images/mpr_interview/screenshot6.jpg) 

That's a wrap! Soon we can look forward to Phaze 2 of the mod, where more areas in the game will receive the visual upgrade. Here are some guides on getting MPR set up on Linux, if you're interested in trying it out:
- [getting it to work on desktop](https://linuxgamingcentral.com/posts/mpr/)
- [getting it to work on Deck](https://linuxgamingcentral.com/posts/metroid-prime-remastered-on-steam-deck-guide/)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
