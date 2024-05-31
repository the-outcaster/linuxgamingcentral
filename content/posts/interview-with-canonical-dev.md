+++
title = "An Interview with Ben Romer, Ubuntu Developer"
date = 2022-12-21T10:57:21-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/ben_romer_canonical/cover.jpeg"
tags = ["interview", "canonical", "ubuntu"]
keywords = ["ubuntu", "debian", "canonical", "snap", "flatpak", "ben romer"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Turns out one of my followers on Mastodon is a developer for Ubuntu/Canonical. I had the pleasure of interviewing what he does for Ubuntu -- he's one of the kernel developers ([Livepatch](https://ubuntu.com/security/livepatch) -- he'll explain what that is). It's a pretty interesting interview, as he explains the controversy behind Snaps, why Ubuntu moved on from Unity to GNOME a few years ago, what's going on with the Mir display server, and what we can look forward to in regards to the gaming aspect on Ubuntu. He even expresses his thoughts outside of Canonical/Ubuntu, such as what he thinks about the Steam Deck, what his gaming habits are, if AMD is better than NVIDIA or vice-versa, etc.

What I really appreciated about his answers is, instead of giving the typical PR response to most questions, he actually is very honest. I think you'll appreciate this too. Bold has been added by me.

**TL;DR**
- Ben Romer works as a kernel developer (full-time, from home in Philadelphia, PA) and has been doing so since 2015
- mostly spends his work time in the terminal, using such tools as GCC, Python, Bash, git, etc.
- familiar with many programming languages, but mostly develops with C
- favorite games include action RPGs such as *Phantasy Star* and competitive titles like *DOTA* and *Counter-Strike*
- uses an ASUS ROG Strix G15 laptop for both development and gaming purposes (RTX 2070 Super)
- prefers AMD over NVIDIA, but NVIDIA is "OK"
- impressed by the Deck's hardware and software, but would like to see a better transition for Gaming Mode and Desktop Mode (held horizontally, Game Mode; vertically, Desktop Mode)
- describes Ubuntu as "easy to maintain, frequently updated, and not usually too hard to fix when it does break"
- Canonical "has started up a team for improving gaming, and they're working their way through aligning people in the company to focus on it." This would include better Steam Snap support, better gaming support on the kernel level, better NVIDIA support, and perhaps even more anti-cheat support!
- outside of Ubuntu/GNOME, he's fond of Plasma and GNUStep
- the Unity desktop was abandoned in favor of GNOME since many of the devs behind it (as well as Ubuntu Touch) were laid off
- Snaps are good for IoT devices and servers for smaller storage footprint and automatic updates, but he admits Snaps are otherwise a "mixed bag"
- frustrated at the disintegration between software devs just focusing on their program and distro maintainers ensuring the program works on that distro

# Explain who you are and how you ended up working for Canonical.
My name's Ben Romer, I've been a programmer and Linux user since 1995. In the past I worked for Unisys, doing SVR4 and .NET code, and had been a fan of Ubuntu since 6.04. Unisys laid me off (as part of a [mass layoff](https://www.computerworld.com/article/2585614/unisys-announces-layoffs-as-q3-income-drops-by-53-.html)) from my job there as kernel upstream engineer, and I took the opportunity to apply at Canonical, and got hired. I've been working on Livepatch ever since.

![Unisys](/images/interviews/ben_romer_canonical/unisys.jpg)
*Image credit: Unisys*

Outside of work I like esports, and karate; was an instructor pre-COVID.

# Do you work at home, or does Canonical have a physical location where it's required to work in the office? Are you full-time or part-time?
I work full time from home (Philly PA, USA!) and nearly everyone in the company is remote and full time. We have a small, permanent UK office. The company has large-group week-long meetings every year around release time, so every six months or so, everyone in engineering gets together for a week to talk about work and socialize. It's a real job perk -- I've been to a bunch of places in Europe I'd never have had the chance to go otherwise.

# How long have you been working at Canonical, and what do you typically do there?
I've worked at Canonical for nearly 7 years. I was put on our Livepatch project, day one, and have been doing that the entire time. Livepatch is a security tool that lets us fix (some) holes while a system is still up, to give the sysop time to prepare for a reboot when convenient. My job is to take security fixes, modify them so they'll work when loaded at runtime, build, test, release, and maintain those patch modules.

![Ubuntu Livepatch](/images/interviews/ben_romer_canonical/livepatch.jpg)
*Image credit: Canonical*

# What set of software tools do you use for your daily workflow?
My working set is fairly standard for an Ubuntu kernel dev, so GCC, Python, Bash, git with code being stored on Launchpad (of course), and Debian packaging tools. It's all CLI so I spend most of my work time in the terminal. I also use kvm and lxd daily, for testing things out.

# What programming languages are you familiar with, and which one do you usually work with?
Ahh, languages were kind of my thing for a while, so I know many. C is my main thing for projects, with all of its usual accompanying tools for generating code (flex/bison for instance) and debugging (valgrind/efence/etc). In no particular order I've also used Python, Delphi, Vala, Java, Javascript, Lisp, Modula-3, and several less common ones like FORTRAN and Ada. I've also made toy compilers for Java and C, but nothing serious.

# Are you a gamer? If so, what games do you typically enjoy playing?
I LOVE games. My first gaming system was the Atari 2600, and during the console wars, I was on team Sega.

My favorite games are action RPGs (*Phantasy Star*, in particular), and side-scroll platformers, indie games, and competitive games (so *DOTA*, *Counter-Strike*, *Overwatch*). Anything with good art and a sci-fi/fantasy setting is perfect.

![Phantasy Star Online](/images/interviews/ben_romer_canonical/pso.jpg)
*Image credit: Sega*

Indie games are really the best, though. I love seeing the creativity and being able to talk right to the people doing the making.

# What hardware do you have inside of your gaming rig?
Hardware-wise I go for gaming laptops, due to those trips I mentioned -- currently I'm on an [ASUS ROG Strix G15](https://www.amazon.com/ASUS-Display-R9-5900HX-Keyboard-G513QR-ES96/dp/B08SJTW9LK). Having a powerful but portable system lets me work *and* play anywhere I go, and (with the exception of sound) ROG hardware has just worked with Ubuntu. I wanted to get their Advantage model for my last upgrade, which was an RX 6800, but with the GPU shortage it was really hard to find, so I ended up on an RTX 2070 Super.

![ASUS ROG Strix G15](/images/interviews/ben_romer_canonical/asusrogstrixg15.webp)
*Image credit: ASUS*

# AMD or NVIDIA, and why?
AMD vs Nvidia is a hard question. There's so many variables! For example, right now I'm on Nvidia and Xorg -- which is *solid* -- because Wayland is still very buggy on Nvidia. I get weird ghosting issues on Death Stranding (pun not intended), and ugh, if you've ever tried to run Nvidia Prime and Wayland at the same time, you've experienced some real pain. If I had AMD, I'd probably be on Wayland, and happier -- but it just wasn't available how I wanted it at the time.

The AMD in the Steam Deck though, man, what an amazing setup, I wish I could get THAT in a laptop, with a fat battery and laptop hardware next to it. Give me an eight-hour-battery gaming rig with keyboard and mouse controls please! Anyhow, now that [Nvidia's drivers are in the process of being open-sourced](https://linuxgamingcentral.com/posts/nvk/), maybe some of the sharp edges will go away, and we'll see a more fair competiton there, but if I could get anything I wanted, I'd be on an AMD right now. But Nvidia is OK.

![AMD Vs. NVIDIA](/images/interviews/ben_romer_canonical/amd_vs_nvidia.jpg)
*Image credit: Tom's Hardware*

# Do you have a Steam Deck, and if so, what are your thoughts on it?
I freakin' LOVE my Steam Deck. It's such a great bit of hardware -- so customizable, and SteamOS is very, very impressive, *and* it's a pretty damn good gaming system even on its own!

The one thing I do wish was a bit smoother is the desktop/gaming mode transition. If it were me designing it, I would have had both modes available at the same time - specifically, held horizontal it's in game mode, but held vertically, it's a tablet. Would have been great for guides and such.

Once Ubuntu's kernel gets support in place and can be a really viable choice on the Deck, I'd like to set up a custom build of Ubuntu that works like I described, maybe do some additional integration with other stores, and native games as well. Maybe even get an Android environment packaged up, and be able to play their games too.

![Crisis Core remake on Deck](/images/steam_deck/crisis_core_remake.jpg)

But yeah, the Deck is really a masterpiece of hardware design. I love it.

# Explain why a person might want to use Ubuntu as their daily driver for gaming and everyday use.
While I'm not really fond of distro wars, I will say there is a lot to really like about Debian, Ubuntu, and derivatives. It's easy to maintain, frequently updated, and not usually too hard to fix when it does break. Gaming-wise, you can get nearly every major Linux gaming tool in a well-maintained .deb format. On the kernel team we have several people responsible for video and a lot of direct contact with hardware vendors, so bugs get addressed fairly quickly.

The thing I really like about Ubuntu is the desktop. The dock reminds me a lot of my college-years OS ([NeXT](https://en.wikipedia.org/wiki/NeXT)); it's fast and easy to maintain, and if you don't like the tools Canonical's picked, you can swap them out for KDE, or another store. It's quite flexible, but the main benefit (in my honest opinion) is sane default settings for packages. A good amount of the time, you can just install the .deb and be done with it.

![Alienware with Ubuntu](/images/interviews/ben_romer_canonical/alienware.webp)
*Image credit: Dell*

**Canonical isn't doing enough for gaming -- but is changing. Recently the company has [started up a team for improving gaming](https://discourse.ubuntu.com/t/introducing-early-access-to-the-steam-snap/28082), and they're working their way through aligning people in the company to focus on it.**

While there are some very unpopular things about Ubuntu (Snaps...), overall the hardware support is good, the desktop is quick and easy to learn, and it's easy to approach it from a software dev standpoint.

# What specifically can we look forward to regarding the gaming aspect for Ubuntu?
Back at the end of April, [we opened up a Snap-packaged version of Steam for trials](https://www.gamingonlinux.com/2022/04/canonical-going-all-in-on-gaming-for-ubuntu-new-steam-snap-package-in-testing/), and started hiring people for "the Ubuntu gaming experience team" in May. There was of course a whole bunch of work done around this to enable the Steam Snap, and now have **about a dozen devs working directly on gaming support** and related stuff, like the Nvidia drivers.

There's a lot about the Steam snap that just doesn't work like Snap wants (like GameScope, for instance). Snap is actually very much at odds with how games tend to work -- games wanting control of the whole machine, more or less. It's just a straight up conflict of needs. Steam wants full access to a ton of devices, and gamers want to install things wherever they want, they want customized Proton, they need to tweak configs, install mods, all of that -- while one of Snap's primary purposes is to default to "no access" -- so we need to fix that, as well as making those things easy.

![Steam on Snapcraft](/images/interviews/ben_romer_canonical/steam_snap_store.webp)

**We're just shy of 40 people in total with their eyes on the ball -- kernel people, devs for Snap, devs for Steam support, maintainers of FOSS games, and also people you might not expect, like our cloud service devs**. After all, we want to be able to play, but we don't want to create risk by doing that. Just imagine how embarrassing it would be for some gaming-focused feature to cause a cloud provider to get compromised.

I'm no oracle, but I can tell you what I'm looking forward to, and trying to push.

In the short term, I'd look for the Steam Snap to get a lot better, for better gaming support in the kernel, and more specifically for our Nvidia driver support to improve a lot. Longer term, **I'd personally like to look at things we can do with livepatching to improve gaming -- who knows, maybe it'll help us get more anti-cheat systems on board?** That's the kind of thing I'd love to work on.

# Any distros/DEs/window managers outside of Ubuntu that you like?
I'm really fond of Plasma, not specifically the Steam Deck's packaging of it, but just in general. Part of it is a fondness for QT and C++, and the desktop itself is just gorgeous. I'm too heavily invested in GTK apps though to really switch. Every now and then I'll get on a nostalgia kick and go see how [GNUStep](https://gnustep.github.io/) is doing, I really miss the elegant simplicity of NeXT, but it's just so niche I don't think I could get away with it as a daily driver.

![KDE Plasma](/images/interviews/ben_romer_canonical/plasma.webp)
*Image credit: [u/amradoofamash](https://www.reddit.com/r/archlinux/comments/y1w6yo/unable_to_update_to_plasma_526_on_arch/)*

# Starting with Ubuntu 18.04, [Canonical shifted from their Unity desktop to GNOME](https://arstechnica.com/information-technology/2018/05/ubuntu-18-04-the-return-of-a-familiar-interface-marks-the-best-ubuntu-in-years/). Why was this change made?
I had just started with Canonical when the desktop and phone layoffs happened, so I don't have a whole lot of insider info, but I'll tell you what I do know.

You might remember the [Ubuntu Phone project](https://www.pcmag.com/news/ubuntu-touch-phonetablet-support-ends-june), which ended at the same time? The switch-over was primarily because of that. A lot of Unity devs were laid off, and quite a few from Mir too. If I recall correctly, this was justified by the community complaints about Ubuntu being non-standard, and of course, the phone wasn't taking off.

![Ubuntu Touch on Librem 5](/images/interviews/ben_romer_canonical/ubuntu-touch-on-purism.webp)
*Image credit: [FossBytes](https://fossbytes.com/librem-5-ubuntu-touch-support/)*

Now, I really liked Unity, and I loved what was going on with the development tools back then; there was a definite push for QT/KDE to become the choice for desktop/phone apps, which would have been great since QT targets Android too, but (again if I recall correctly) the phone just wasn't doing well enough. Unity 8 is still around [now renamed to [Lomiri](https://unity8.io/)] though being developed outside Canonical now, [Mir lives on as a display manager for IoT devices](https://mir-server.io/) (mainly), and of course Snaps stuck around...

# You had alluded to Snaps as being "unpopular." Why is there so much controversy behind Snaps? From your viewpoint, what are the advantages of this packaging system?
And they're quite divisive in my experience. I think a lot of the hate comes from early issues with them -- they were slow, there were bugs, snapd is yet another long-running networked service, you can't control update timing -- and some things still linger on, like requiring app developers to adapt their code to know if it's in a Snap (or not). There's also the heavy-handed changeovers of popular browsers to Snap, and that made a lot of people angry too.

And then there's of course the political issues with packaging -- if you're a hardcore advocate of your distro's packaging, you'll see Snaps (and Flatpak) as kind of a parasitic distribution, because they replace your focused work to package for your distro with this claim of being "generic." Of course, they're not really generic, just different -- and have the same kinds of support library issues as DEB/RPM/whatever.

![Snap meme](/images/interviews/ben_romer_canonical/snap_meme.jpg)
*Image credit: It's FOSS*

From a security standpoint Snaps are a mixed bag -- sure, they're containerized, but the vast majority of Snaps require access to your home directory, and if there's a security bug in a library, you have to rebuild and replace every Snap that uses it, instead of just updating your distro library and being secure. Finally, Snap was pitched as a way to get updates to users faster, but most Snaps have debs as dependencies anyway, so it's not really any *faster*.

Snap's primary advantages really only show when you're talking about IoT devices or servers, and some of the annoyances actually become advantages. With Snaps there, you have only the bits of software you actually need to run, so it cuts the storage footprint down; you get fully automated updates, which reduces admin workload and/or simplifies maintenance for an end-user who might not even know what OS is running; and it's all containerized, so one update doesn't break all.

# Some time ago, [`sudo apt install <package_name>` got aliased to `sudo snap install <package_name>`](https://askubuntu.com/questions/1345385/how-can-i-stop-apt-from-installing-snap-packages). Can you comment as to why this change was made?
I'm not intimately familiar with why things around packaging get changed -- often times, these decisions are made by the maintainers of a package, or as part of a push for something else. I'm just a kernel guy. But I can give you some educated guesses here, and maybe talk a bit about packaging again.

So Ubuntu (and Canonical) get a lot of criticism from a lot of angles re:packaging. There's people who say "Ubuntu is just stealing from Debian," that kind of narrow mindset... It's not really a valid criticism in my honest opinion -- a lot of Canonical employees *are* Debian devs, so I'd say the situation is more like Fedora/RHEL was. Devs have to eat too, and Ubuntu does that -- and is still free anyway. But then, when we do come up with a (universal!) packaging scheme like Snap, the same sort of criticisms come up. It's not an argument you can ever win, because every user and every dev has their own use cases.

![Packaging meme](/images/interviews/ben_romer_canonical/standards.png)
*Image credit: [XKCD](https://xkcd.com/927/)*

To make it worse, when devs have to split their attention like that -- now I have to package a deb, Flatpak, Snap, RPM, each with specific requirements, the devs get frustrated, and everyone just ends up unhappy. The thing that sucks here is, distros were meant to remove that problem -- the upstream devs focus on their program, and the distro maintainers focus on making it work on their distro, you know, a strong separation between development and integration.

It's partially the fault of these universal packaging systems in my honest opinion -- **"just Snap or Flatpak" it, sure, but now you have to test it everywhere instead. That's what the distro was supposed to do -- package it, test it, bang out bug reports. Add in neglect of competing packaging systems and marketing people making demands, and you end up with a less-than-useful store, and "forced" transitions between formats,** even if the devs were the ones that asked to change it.

# Anything else you want to share with us?
I don't really have anything else to add, but I do want to say *thank you!* to everyone who's supported Ubuntu or one of it's derivatives, and to Linux users and FOSS users in general. There's something magical about seeing people thrive through sharing and I hope our way of making things grows to become something universal.

![Ben Romer's website](/images/interviews/ben_romer_canonical/website.png)

Thanks to you, too, for putting up with my rambling!

Ben Romer (BroWren) is on [Mastodon](https://mastodon.social/@browren@mastodon.cyborgcentral.net) if you want to give him a follow. He also has his own website, [Cyborg Central](https://www.cyborgcentral.net/). If you're fond of a retro-looking font, I think you'll like it!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
