+++
title = "An Interview with Luke Short, Creator of WinesapOS"
date = 2023-02-16T16:25:29Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/profile_luke_short.jpg"
tags = ["interview", "winesapos"]
keywords = ["winesapos", "luke short cloud", "luke short interview", "luke short", "winesapos on steam deck"]
description = "Want to harness the power of SteamOS without having to install it? You should give winesapOS a try."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
There's a few SteamOS-based distros around the block. One that you might not be aware of is [winesapOS](https://linuxgamingcentral.com/tags/winesapos/) -- which, at the time of writing this, has [over 500 stars](https://github.com/LukeShortCloud/winesapOS) on GitHub. I wanted to get in touch with the main developer, Luke Short -- the person who helped me get in touch with Intel regarding their [Optane SSD](https://linuxgamingcentral.com/posts/intel-optane-ssd-review/) -- and discuss what exactly the distro does, and why a person might use it over other gaming-oriented distributions. More importantly, I also wanted to get his thoughts on what it's like maintaining a distro that uses SteamOS packages -- the common theme that I'm seeing, not just with winesapOS, is that it's kind of a royal pain in the arse to stay up-to-date and make sure none of the packages break.

**TL;DR**
- Luke Short is a solutions engineer at VMware and works on Kubernetes. Outside of his job, he works on winesapOS
- winesapOS started out as a shell script for running commands to install Arch Linux, and to add Linux support to Macs
- winesapOS has been around close to three years, and was the first distro to be based on SteamOS 3
- advantages of winesapOS: portable, Mac support, and test-driven development
- one full-time dev and two part-time
- other than lack of sound, winesapOS support on Deck is great
- the Steam Deck: "a game changer for the industry"
- the most difficult part of maintaining the distro: packages need to be manually tested when SteamOS gets updated to make sure they don't break anything
- short-term goals: major upgrade support. Long-term: support for ARM devices

# Explain who you are, what you do, and why you founded winesapOS.
My name is Luke Short. At my day job, I’m a Solutions Engineer at VMware working on cloud technologies such as [Kubernetes](https://kubernetes.io/). My focus is on enabling companies to automate and scale their applications while adopting cloud-native practices. The ultimate goal is to give teams more time to work on things that matter such as mission critical applications.

![winesapOS](/images/winesapos/cover2.jpg)

Historically, online I’ve actually been known as “the Chromebook guy” who reported on various Linux gaming news in the ChromeOS space. I used to do a lot of freelance writing for places such as [Android Police](https://www.androidpolice.com/author/luke-short/) and [Chrome Unboxed](https://chromeunboxed.com/author/luke/). Nowadays, a lot of my energy outside of my day job is directed towards winesapOS. 

My operating system started off as an experiment. Could I automate installing Linux, make it portable, and get it running perfectly on Macs? *Halo: The Master Chief Collection* had just come out for PC and it worked on Proton! My best friend and I love *Halo* and, for the first time since our childhood, we could play together again! Except he had a Mac. macOS couldn’t play *Halo*. Not even through CrossOver at the time. Adding insult to injury, his Mac even had an AMD discrete graphics card! **I knew that installing Arch Linux was just a bunch of commands. I thought: “What if I took those commands and put them into a shell script?” Thusly, the experiment started and worked!** It has grown massively since then.

# What is the significance of the name “winesapOS,” and how long has the project been around?
The word “winesap” is actually a type of apple. Since the original goal was to work on Macs, it seemed like a fitting name. Most people will be surprised to know that winesapOS has been around for almost three years now. What really put us on the map is that **we were the [first Linux distribution to ever be based on SteamOS 3](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.0.0-beta.0).** I did a lot of planning after the Steam Deck’s announcement to prepare winesapOS for the switch from Manjaro to SteamOS. All of that hard work paid off once the Steam Deck launched and the source code was available. It was an easy transition that took only a few weeks.

![Winesap apple](/images/winesapos/winesap.jpg)
*Image credit: Gardener Direct*

# Why might a person want to use winesapOS? Can you explain the benefits it has over other distributions?
**Portable and persistent storage.** Our operating system was built from the ground-up to be portable. You can flash it to an external drive and take it with you on the go. All new files and changes will be saved upon reboots. With that being said, most of our users actually use it on an internal drive.

**Mac support.** We provide lots of third-party drives for the best experience on Macs. By using winesapOS, you can turn any Mac into a gaming machine with the power of Linux!

![winesapOS on a Macbook Pro](/images/winesapos/running_on_a_macbook_pro.jpeg)
*Image credit: [Luke Short](https://twitter.com/LukeShortCloud/status/1549259554222878722)*

**Test-driven development (TDD).** Unlike most other Linux distributions, winesapOS was built from the ground-up with TDD. That translates to a stable operating system since we have automated testing. When something breaks, I know about it immediately. Thanks to the community, we now have a continuous integration (CI) pipeline to test every single commit.

# What role do you play as far as development of the distro? How many people actively contribute to the code?
I am the main developer of winesapOS. Besides code, I am passionate about documentation and project planning. I use feedback and advice from the community to drive the development of winesapOS.

Here are some fun metrics about our project:
- Full-time developers: 1
- Part-time developers: 2
- Participaints for bug and feature requests: around 25
- Commits: almost one thousand
- Users: a few thousand (estimated)

We have also worked with other operating systems such as Batocera, HoloISO, and PS4Linux to share our learnings.

# How is compatibility with winesapOS on the Steam Deck?
Overall, it’s great! Since we are based on SteamOS, we inherit the same drivers. **One problem is that getting the internal speakers to work is very tricky.** Valve has not upstreamed all of their Steam Deck hardware support and setting up the drivers on our fork is tricky. Where distributions such as HoloISO try to be as close to SteamOS as possible, we try to take the SteamOS formula and improve upon it from the ground-up. This leads to occasional caveats including lack of sound support.

![winesapOS on Deck](/images/winesapos/on_deck.jpeg)
*Image credit: [Luke Short](https://twitter.com/LukeShortCloud/status/1549999624546500608)*

# Speaking of the Steam Deck, what are you thoughts on the device?
The Steam Deck is literally a game changer for the industry and Linux gaming community. My gaming computer has dusted away as I prefer to play games on the couch or in bed. I’ve gotten a bunch of my friends on the Steam Deck bandwagon and we’re all loving it so far. I’m excited to see what the next generation of portable PCs will be like!

# Since winesapOS is based on SteamOS, how has it been as far as difficulty keeping up with all the changes Valve makes? Do things tend to break on winesapOS once it upgrades to a newer version of SteamOS?
The most time consuming part when Valve updates SteamOS is that winesapOS needs to manually update the mesa-steamos and linux-steamos packages. These are hosted on the Arch Linux User Repository (AUR) with tweaks to allow them to build and work on a wide range of generic hardware (not just the Steam Deck). We then need to run various tests to make sure they still work on the latest rolling Arch Linux release. I’m investigating a few different ways of automating all of this.

When Valve released SteamOS 3.4, they decided to randomly change all of the repository names. This broke all Linux distributions using their repositories, including ours. This has been fixed in our [winesapOS 3.2.1 release](https://linuxgamingcentral.com/posts/winesapos-3.2.1/). More communication from Valve in the future would be greatly appreciated from the community.

![winesapOS logo](/images/winesapos/logo.webp)
*Image credit: [Luke Short's wife](https://twitter.com/LukeShortCloud/status/1503420536495345666)*

**People ask me all the time if it’s worth it to use the special packages from SteamOS. After using them for a year, I can confidently say no. You’re better off using the latest upstream packages.** For example, their Linux kernel is still stuck on Linux 5.13 which has been end-of-life for a half a year now. They only backport patches for AMD Radeon’s RDNA2 architecture so it's highly specific. In winesapOS, we also include the latest Linux LTS kernel for those who need a secure and modern kernel with improved hardware support.

# Can you give us a sneak peak as far as what we can look forward to with the next major update to winesapOS?
Short-term, **major upgrades are our focus.** The reason I don’t go with distributions such as elementaryOS is because they do not offer major upgrades. In fact, winesapOS 1 was supposed to be based on elementaryOS but we had to switch to Ubuntu to support major operating system upgrades. That is a deal breaker to know that a system will become end-of-life. It’s almost as bad as Windows! My current priority is making sure that we have an upgrade path for winesapOS 2 to winesapOS 3. Long-term, **I have ambitious plans of supporting ARM devices** such as the Raspberry Pi and Apple silicon.

# Anything else you want to share with us?
I’m always planning ahead and thinking about what the next evolution of winesapOS may be. My ultimate goal is to help bring Linux gaming to the masses and I will always continue to contribute towards that goal!

![winesapOS on PC](/images/winesapos/on_pc.jpeg)
*Image credit: [@di-egoalves](https://twitter.com/di_egoalves/status/1510335513932218377)*

If anyone wants to follow me and my work, the best place to start is my personal blog: https://lukeshort.cloud/

Though they're a little outdated, there's a couple of more interviews with Luke [on](https://boilingsteam.com/podcast-16-with-luke-short-how-far-are-we-from-having-steam-on-chromeos-and-how-the-steam-deck-will-change-linux-gaming/) [Boiling Steam](https://boilingsteam.com/steam-on-chromeos-a-win-win-situation-for-both-google-and-valve/) if you'd like to get to know him more!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
