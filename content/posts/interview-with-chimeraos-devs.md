+++
title = "An Interview with Matthew Anderson and Joaquín Aramendía, ChimeraOS Developers"
date = 2022-11-02T10:18:27-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/chimeraos/logo.jpg"
tags = ["interview", "chimeraos"]
keywords = ["chimeraos", "holoiso", "steam big picture", "steam deck", "steam", "console gaming", "onexplayer", "onexplayer mini", "amd", "hp dev one"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
While it's true that we have distros like [HoloISO](https://linuxgamingcentral.com/posts/news-holoiso/) to give devices outside of the Steam Deck a SteamOS-like experience, it's kind of a shame that [WinesapOS](https://linuxgamingcentral.com/posts/winesapos-3.2.0-beta/) and [ChimeraOS](https://linuxgamingcentral.com/posts/chimeraos-35/) get swept under the rug. Both projects are devoted by very passionate developers, and they each have their own unique aspects that a lot of people tend to overlook. As a journalist, part of my job is to increase the awareness of projects like these, and today, I wanted to focus specifically on ChimeraOS.

Back in April, I had interviewed the project's founder, [Alesh Slovak](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/) (alkazar79). Back in June of 2020, I had [reviewed](https://boilingsteam.com/gameros-an-enhanced-version-of-steamos/) the distro itself on Boiling Steam. Back then, it had *so* many advantages over vanilla SteamOS 2.0...too many to count here. But let's just say it's an *awesome* way to transform your PC into a living room console, and it still lives up to that to this day. It might even be a [replacement for SteamOS 3](https://linuxgamingcentral.com/posts/the-growing-security-risk-with-steamos/) one day, giving your Steam Deck a much more up-to-date software experience.

As the ChimeraOS team consists of multiple contributors and developers, I had a chance to not only interview a few more of them, but along the way I also became close friends with them. In particular I'm referring to Matthew Anderson (Ruineka) -- the one who wrote the [HP Dev One review](https://linuxgamingcentral.com/posts/hp-dev-one-review-by-chimeraos-dev/) not too long ago -- and Joaquín Aramendía (Samsagax), who's a rally fan and stubbornly refuses to admit that he's a programmer, despite [contributing a kernel driver for the OneXPlayer](https://www.phoronix.com/news/OneXPlayer-Linux-Platform-Drv).

As with most of my interviews, small spelling/grammar fixes have been added, and bold has been added by me.

![Samsagax testing ChimeraOS on OneXPlayer Mini AMD](/images/chimeraos_interview/ruineka_and_samsagax/onexplayer.jpg)
*Image credit: Samsagax*

**TL;DR**
- both devs have contributed greatly to the growth and development of Linux and GameScope support for the OneXPlayer, as well as ChimeraOS itself
- ChimeraOS is a great distro to turn a computer or handheld into a couch-oriented gaming machine, and many of its unique features were created *prior* to the release of SteamOS 3, which Valve heavily borrowed from
- at least five devs who work on ChimeraOS
- programming languages they have used include C#, C, C++, Java, and Python
- rarely does either developer use Windows; they use Linux as their daily driver
- Ruineka prefers Pop!_OS with GNOME/Mutter. Samsagax uses Arch with GNOME
- the Deck is "revolutionary in many regards"
- the OXP is decent, albeit for the bugs on the software side (which both devs are working to improve)
- *Sonic Adventure 2* is Ruineka's favorite game; Samsagax is a big fan of rally games
- how to contribute to open-source: "find what doesn't work correctly for you and reach out to the developers behind the software to report the bugs"
- how to help contribute to the growth of ChimeraOS: submit pull requests if you know how to work with code, get involved in their [Discord](https://discord.gg/fKsUbrt) group, report bugs, game compatibility, and what you want to see in future releases
- what we can look forward to in the next release: external display fix for the Deck UI for docked handhelds, bug fixes, updated packages, and some other things that couldn't be disclosed

# Tell us who you are and the project(s) you are involved with.
**Ruineka:** I am Matthew Anderson and I'm all over the place when it comes to projects. When I run into an issue, or think of something that could be better I immediately pull up my sleeves and get to work. A few examples is getting the OneXPlayer fixes out into the Linux world because when I started there was virtually no support whatsoever. Naturally this led my way to sorting out touchscreen-related issues on Pop!_OS and running into the ChimeraOS project.

**Samsagax:** I'm Joaquín Aramendía, a mechanical engineer from Argentina. I do some specially crafted text files in my (short) free time. I had a minor involvement in the [Bumblebee project](https://www.bumblebee-project.org/) [aims to bring NVIDIA Optimus support for Linux], then did some projects on my own. Currently I'm collaborating with the ChimeraOS developers along others to make an alternative OS with a console experience for PC games.

![ChimeraOS running on Aya Neo](/images/chimeraos_interview/chimeraos_on_ayaneo.jpeg)
*Image credit: Alkazar79*

# ChimeraOS -- explain what this is, and why a person might want to use it.
**Ruineka:** ChimeraOS is a project that is aimed to be a console-like experience for your PC with added benefits from the [Chimera App](https://github.com/ChimeraOS/chimera) that adds the ability to remotely control packages from your phone. Such as install games from your Epic Games library or set up your emulators with cover art and everything. Alkazar has ambitious plans to extend the functionality of this further, or as he puts it he "has a vision," what that means would be best answered from him directly I think. 

As a person who is extremely passionate about handheld gaming I think that ChimeraOS is continuing to become a good option for a person looking to give Linux a try and doesn't feel comfortable using the command line to compile code or pull scripts from a GitHub page. Admittedly it has been rather difficult trying to keep up with the constant changes with the upstream [such as GameScope, the kernel, MangoHUD, etc.] that cause many regressions. We do our best to keep on top of these sorts of things; that way, the end user will never know it was a problem to begin with.

**Samsagax:** ChimeraOS is an Arch Linux-based distribution that strives to make PC games work as a console. It is intended for any type of PC but the more adequate setup is a HTOP or Handheld device with a gamepad on it. I currently run a similar setup on a desktop PC I assembled on my own with all AMD parts since it is the best supported setup. The OS has a lot of add-ons to make games work out of the box and **has it's own verification standard, very similar to the [Steam Deck Verified](https://linuxgamingcentral.com/posts/flawed-steam-deck-verification-system/) program, but Alkazar did it first.**
 
The OS comes bundled with a web app to access the device remotely and configure it, install non-Steam games and control some functions. For more advanced users there is also SSH access.

All in all it is a great OS with only one focus: get into games fast and without hassle. It is intended to be used with a gamepad on a couch and [not have to] worry about configuring the OS for games. Most of it is done for you in the background.

![Samsagax downloading Dirt Rally 2.0 on OneXPlayer Mini AMD](/images/chimeraos_interview/ruineka_and_samsagax/dirt_rally_2_on_oxp.jpg)
*Image credit: Samsagax*

# What are some things that you have personally contributed to ChimeraOS?
**Ruineka:** You'd think this would be easier to say than it really is, but truth be told the main battle since I've started assisting with the project has been helping Pastaq [another ChimeraOS contributor] with [HandyPT](https://github.com/ShadowBlip/HandyPT)/[HandyGCCS](https://github.com/ShadowBlip/HandyGCCS) (a power tool for handhelds, and a virtual controller that maps all the buttons to be usable on the devices in a similar fashion to the Steam Deck).

Finding solutions to the UEFI breaking on ChimeraOS with the 5.19 kernel was a battle, and dealing with the recent challenges of bisecting the 6.0 kernel breaking GameScope with older APUs (5000 series and older) are examples of behind the scenes work that many likely won't know ever was a problem, **the fix comes to you courtesy of Samsagax**. I also attempt to push things forward for Intel products trying to get things to work correctly for GameScope and games in general. TL;DR tons, and tons of testing and bisecting..

**Samsagax:** Honestly, not much in my view. Most of the things were already in place. I started by re-factoring some shortcuts code on the Chimera app and then got involved in writing some tests for it. Then I got involved into the OS foundations, cleaning it up a little and discussing some features. I started the [gamescope-session](https://github.com/Samsagax/gamescope-session) project on my own for personal use and asked Alkazar to include it in the distro. Now it is part of the project and we adapted the Steam Deck session to our own.

When the Steam Deck came along and a desktop was all the rage, Alkazar reluctantly accepted its fate and each of us tested a different desktop environment looking for one that was clean, feature complete, small, performant, and minimal. I tested GNOME (among others) and we all agreed it was the one.

I also made some adjustments for the OneXPlayer Mini AMD.

# How many developers have contributed to ChimeraOS?
**Ruineka:** There have been many contributors to ChimeraOS in many ways, I'm not entirely sure what the total head count is. I work with pastaq, alkazar, Samsagax, and ShadowApex the most however.

**Samsagax:** There [are] all kinds of contributions, big and small from a lot of developers. I can't come up with a number that makes justice to all of them since they are all needed to were we are now. I could say we are in the ballpark of 30 somethings, including yourself.

![Ruineka testing gamescope on Intel](/images/chimeraos_interview/ruineka_and_samsagax/intel_running_with_gamescope.jpg)
*Image credit: Ruineka*

# What programming languages are you familiar with? How long have you been coding?
**Ruineka:** I'm mostly familiar with C# because I used this when using Unity to work on a personal game project of mine. I was more or less forced to learn the ropes with C and C++ because of I wanted to write the fixes for GameScope needed to control the orientation of the display and add the ability for it to make use of the kernel quirks, which got merged upstream by the way, thats a huge relief! No more upside-down screens for people who aren't using a Steam Deck! I also had to learn Python on the fly to add support to the OXP Mini/Intel units to HandyGCCS. 

I've been coding as a hobby ever since I got interested in game development back in the RPG Maker XP days, which would be 2010 I think?

**Samsagax:** I know C/C++, Java, Python, R, Matlab, some proprietary RAPID code (for robots)
I leaned programming in high school an then I started to program and learn on my own in my free time when I was in my late teens and 20s. I'm no expert by any means. Most of the time is trial and error.

# I assume you primarily drive Linux on a daily basis. Have you ever needed to resort to Windows or Mac OS from time-to-time?
**Ruineka:** I daily drive Pop!_OS mostly and intend on setting up Arch Linux in the near future. I usually have to resort to Windows when trying to claim promotions for hardware that requires a verification tool to be ran and for testing performance for a point of comparison. I suppose it's useful when diagnosing hardware issues as well.

**Samsagax:** I'm forced to use Windows at work, but on all my devices I use GNU/Linux. I used to have some proprietary programs that only ran on Windows for work but that is it. When I'm in that situation on my own devices I try to look for alternatives or the last resort is virtualization. I even try to run stuff on the last good Windows version (XP). That far in time I put the good MS OS [to use].

![Ruineka testing GameScope on OneXPlayer](/images/chimeraos_interview/ruineka_and_samsagax/sa2_on_oxp.jpg)
*Image credit: Ruineka*

# What's your distro and desktop environment/window manager of choice, and why?
**Ruineka:** I'm a Gnomie which uses Mutter as the window manager/compositor and that's because it just works for me. I know others have the opposite experiences as me, saying KDE was more stable for them, but I guess that's what is great about having multiple options to choose from, huh?

**Samsagax:** When I first started I distro-hopped a lot; Ubuntu, Fedora, Mandriva, Mint. Until I fell in love with Arch Linux (I use it, btw!). Then I did come back to Ubuntu for a while, but it felt outdated; was a pain to install newer stuff than the software in their repos. Fedora was good in that aspect but broke a lot. Arch puts you in charge and if it breaks it is on you... That shift in thought made it my distro of choice.

As for DE I tested and tried to daily drive most of them. And there are some obscure and good alternatives there, like Enlightenment or Budgie. I used GNOME 2.32 as my first DE. It looked clean, nice, and was the most popular, then there was KDE, the most feature-rich but heavy one. When GNOME 3 came out it was a change of paradigm, I had to relearn what a DE was. And I really liked it. Now I can't conceive a DE that puts icons on the desktop... Daily drove KDE for about four years and switched back to GNOME in v40.

# What are your thoughts on the Steam Deck?
**Ruineka:** I think the Steam Deck is revolutionary in many regards. It's the first mainstream handheld PC as well as one the few options that have Linux pre-installed. Valve has dedicated a lot of time and money into Linux to make it a viable gaming platform and it shows.

As a person who has been gaming on handhelds since the original Game Boy and a person who modded his PSP to open the system up to be comparable to what the Steam Deck is today, I've been wanting something like this from an official source for most of my life. It running Linux is a huge bonus, but if you would have asked me as a kid I would have said I want it to run Windows...oh the irony.

![Ruineka testing Deck UI on ChimeraOS](/images/chimeraos_interview/ruineka_and_samsagax/deck_ui.jpg)
*Image credit: Ruineka*

# What are your thoughts on the OneXPlayer (OXP)?
**Samsagax:** I have a OXP Mini AMD. It is a good device with a Ryzen 5800U APU. It works pretty well and performs better than my old laptop in games. No complaints there. On the software side it is kind of a mess, on the firmware side especially. There is no documentation on the device itself. DMI strings [strings in the BIOS chip that describe the device] are all over the place with no way to tell apart versions. It has a button that is supposed to be quiet-mode but it turns off the fan completely! So it is quiet, alright... but you end up with a nice stove. I avoid that button entirely. Hope that is sorted out in a BIOS update.

Linux support was never in their radar until people started to install it on the devices. Seem that they only strived to make it work for Windows with Windows keybindings and things like that. The buttons emit Windows keybindings as well. Pastaq made a great translation to gamepad buttons in Handycon but there are some things that can be improved on the firmware side to make the thing more Linux-friendly and standard.

That is all my grievances but aside from that I use it daily to game on it. Did a full playthrough of *Stray* with about two hours of battery on full power draw. I was not able to play my driving games, but the story-based ones play great.

# What are your favorite games?
**Ruineka:** *Sonic Adventure 2* is by far my most favorite game, bugs/clunky mechanics and all! I also love games like *Freedom Planet/Freedom Planet 2* as well the *Tales* series (*Tales of Zestiria*, *Tales of Arise*, etc). These are the games that stand out most, but truth be told I love a lot of games!

**Samsagax:** Normally I play two games at a time: a "skill-based game" where you need to put in hours to improve, like driving simulators; and a story-based game in paralell to have those ups-downs of game tension, like *Shadow of the Tomb Raider* or recently [*Kena Bridge of Spirits*](https://linuxgamingcentral.com/posts/kena-bridge-of-spirits-review/). I usually don't replay those once the story is ended, they don't attract me that much. Open-world games don't get me either, I'm not an explorer. Driving games I play a lot.

![Samsagax playing Dirt Rally 2.0](/images/chimeraos_interview/ruineka_and_samsagax/dirt_rally_2.jpg)
*Image credit: Samsagax* 

I liked driving games from young age. I used to play *Need For Speed 2* with my Dad on split-screen. Those days are gone. We passed from local multiplayer to online single player. (I blame gamers for that, we let it happen). Hard-core simulators like *Dirt Rally 2.0* and some other casual ones like *Slipstream* (that is hard also!), *Vecter*, *Art of Rally*, *Neodash*. Did I mention I love rally? I'm waiting for *WRC Generations* to disappoint me in the same way as *WRC 10* did but will get it nonetheless for comparison reasons. Codemasters did a great game even without the WRC licence and it shows, the DR2.0 community is huge and very commited. Right now I'm running in a virtual rally with some friends at Global Rally Fans (we are competing in all tiers of Junior Rally Championship) and having a lot of fun there.

And also I play *Factorio* a lot. I got sucked into it. I left it because it was not in agreement with my schedule or free time compatible with a living.

# What would you recommend a person do if they want to help contribute to open-source?
**Ruineka:** I say just find what doesn't work correctly for you and reach out to the developers behind the software to report the bugs. I find that the feedback you get from them is a good way to start to develop the skills needed to start to understand the bisecting process of bugs etc. Once you notice the trend behind this, you'll be able to submit more valuable bug reports and even be able to find the solutions yourself as a follow up. It's not uncommon for a dev to ask you to try a certain patch, or make a change in the code and compile it for testing. You might not know how to do all of this, but I find that knowing an objective is the best motivator to start the learning process. After a while of working together like this with developers you'll gradually develop more skills and before you know it you are writing code yourself and submitting kernel patches upstream.

![Ruineka testing EmuDeck on ChimeraOS](/images/chimeraos_interview/ruineka_and_samsagax/emudeck_on_deck_ui.jpg)
*Image credit: Ruineka*

# What can the community do to help the growth of ChimeraOS?
**Ruineka:** I think the more upstream contributors overall is better from a maintenance perspective for the various projects/packages. That's because ChimeraOS is a consolidation of all these things. For ChimeraOS specifically the feedback and recommendations alone are invaluable. Knowing what is important for the user helps assist with what should be done. If they know how to code or write bash scripts they can always submit a PR and see if it ends up getting added to ChimeraOS or not. Being active in the [Discord](https://discord.gg/fKsUbrt) is a huge plus because many people working on ChimeraOS are active there and you'll get immediate feedback in a lot of cases.

In order for ChimeraOS to grow, it needs to meet the expectations from a wider audience.

**Samsagax:** Use it. Give it a try. And report games, bugs, wanted features and such. Join the [Discord](https://discord.gg/fKsUbrt) and test games on it. Also be aware of it's intended use. **Don't put it in your daily driver desktop**, it is not for that. But it is a power-on, launch a game and start playing OS. That said, enjoy and contribute guides, code, game fixes, which version of Proton works and what needs to be done to make some particular device work. And mostly, have fun with it!

# What can we look forward to with the next version of ChimeraOS?
**Ruineka:** I have a few personal things I'd like to do, but I don't really want to announce this yet without first talking to Alkazar. Overall the main thing is the external monitor fix for the gamepad UI will be included for docking the handhelds (it was broke on the previous version)...as of right now it's mostly a bunch of bug fixing and updated packages.

![Testing ChimeraOS on HP Dev One](/images/chimeraos_interview/ruineka_and_samsagax/chimeraos_running_on_hp_dev_one.jpg)

There you have it! Thanks to both Ruineka and Samsagax for agreeing to having this interview.

If you want to try out ChimeraOS, head over to the [official website](https://chimeraos.org/) to get started. And who knows...I might have another look myself and write another review on it!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
