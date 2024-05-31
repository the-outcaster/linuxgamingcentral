+++
title = "An Interview with Thomas Castleman, Creator of Drauger OS"
date = 2022-03-18T10:31:48-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://cdn.discordapp.com/attachments/685541375139250179/954397820452995112/profile_pic.jpg"
tags = ["interview", "drauger os"]
keywords = ["drauger os", "thomas castleman"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Thomas Castleman is the creator of the [Drauger OS](https://draugeros.org) distribution, based off of Ubuntu. Thomas' goal is to provide gamers a pleasant gaming experience by shipping the [Xanmod kernel](https://xanmod.org/), a lightweight desktop environment, and stability by using Ubuntu as the base. A while back I had reviewed the distro when it was in its' early stages on [Boiling Steam](https://boilingsteam.com/hands-on-with-drauger-os/), but now I had wanted to check in with him and see how Drauger OS is doing these days. In the interview we also find out the status of the Vetala, the gaming console designed specifically for Drauger OS, and the original reason why Drauger OS was made -- which is different now than it was back when the project started.

# Been a while since we last talked. How have you been, personally?

I've been great! I have less free time these days with Drauger OS growing so much, and a new job I recently took on. But overall nothing to complain about.

# For those who aren't aware, can you explain who you are?

My name is Thomas Castleman, you can find me as Batcastle online. I'm the Founder, Lead Developer, and Core Project Manager of Drauger OS.

# What is Drauger OS, and why was it made?

Drauger OS is an Ubuntu-based desktop gaming operating system. It was initially created to be the platform for me to work on to develop the ultimate emulation OS: the idea being you could hook up the original media from any old console that either used optical media or you have an adapter for, and the OS would be able to bypass DRM and encryption, detect what console the game was made for, and automatically launch the appropriate emulator to run the game.

This dream was killed when Nintendo started taking down, or threatening legal action against ROM distribution sites. In order to protect Drauger OS, I changed it's focus from emulation to gaming in general. All emulators were removed, and more general gaming software was added.

![drauger os desktop](https://www.technewsworld.com/article_images/2019/86210_990x660.jpg)
*Image credit: Tech News World*

# What is the lore behind the name "Drauger" OS?

A draugr is a creature from Norse mythology. They're said to be undead warriors, and posses a thirst for blood. They have superhuman strength, and tend to resemble modern zombies to some extent.

In _Skyrim_, one of the most common enemies the player faces when dungeon-crawling are draugr. They are often extremely annoying, and sometimes very powerful. Considering _Skyrim_ is one of my favorite games of all time, I decided to pay tribute to the draugrs of _Skyrim_ by naming this OS after them. 

Unfortunately, I have terrible spelling skills. So the first several times I wrote the word "draugr" in code, images, etc., I misspelled it as "drauger". At this point, it's something of an in-joke. And the misspelling helps prevent copyright issues, so I chose to leave it as is.

# How long has Drauger OS been in development for?

Publicly, Drauger OS has been in development since May 4th, 2018. However, it's true origins can be traced back to 2014. But those extremely early versions of Drauger OS have little to no direct connection to modern Drauger OS, outside of being early testing and concept work for it.

Some of those concepts were as simple as a server version of Ubuntu 14.04 with LXDE slapped on top. Others were more traditional gaming operating systems at the time, packaging a multitude of games and emulators. Because of all these internal versions, our first release had a version code of 7.2.7. Now we are close to releasing 7.6, and we have come a LONG way.

# Drauger OS is based off of Ubuntu. Any particular reason for that?

At the time Drauger OS was initially created, I wasn't very skilled in development or support. I had tried other Linux distros, but had used Ubuntu often enough that that was what I felt most comfortable with when helping others. When Drauger OS was created, that familiarity made it so that I felt like I understood more about the underlying OS I was working with, and was more confident providing support to users. This was hugely important as for several years, I was the only one providing support for Drauger OS. So, I really needed to know my stuff. Because of that familiarity, it felt like a logical choice. At this point, it's more to help new users learn the system easily since I have become better at supporting Linux as a whole.

![drauger os desktop 2](https://boilingsteam.com/wp-content/uploads/deepin_20_panel_profile.png)
*Image credit: Boiling Steam*

# Drauger OS comes with the XFCE desktop environment. I'm guessing that's to free as many resources as possible to the computer's hardware?

Yes, that's one of the main reasons. The other reason is because it provides a huge amount of configurability, and is still relatively user friendly (compared to something like a window manager). This may change in the future though, as we are looking at releasing Drauger OS 7.7 in a couple [of] years, and we are hoping to switch to Wayland by then. If Xfce doesn't have Wayland support by then, we won't really have a choice. We'll have to change desktop environments.

# One major feature to Drauger OS is it's unique installer. What was the reason for not using something like Calamares or other system installers? How has it been working, lately?

A few years ago, I was changing up the way I did development on the Drauger OS ISO. This required us to use a new installer. I tried both Calamares and Ubiquity, Ubuntu's installer, and neither one worked for me. Ubiquity would partition the drive it was supposed to install to, but that was it. Calamares would do that, and get roughly 10% of the files needed installed. It would then freeze for hours on end and end up erroring out. I talked to the Calamares devs in IRC and even together we couldn't figure out what the issue was.

Not seeing any other real alternative, I had started development on our own installer when I was trying to fix the issues I was having with Calamares. Once that started working, it became clear that that was a real option for us.

At this point, our installer, simply called `system-installer`, is having some refactoring work done. After that it will be ported to GTK 4.0, and then parts of it will be converted to C++ (it's written in Python right now). While it still has a few bugs here and there (OEM installation is riddled with them), most users doing a standard installation using auto-partitioning, or who know what they are doing when using manual partitioning, will have a reasonable experience.

The installation reports users have sent us have been super helpful in finding some of these bugs and squashing them. So I expect those reports will become even more vital to development down the line.

![drauger os website](https://cdn.mos.cms.futurecdn.net/ebD3WT7fstazmEnqp3Qo7Q.jpg)
*Image credit: Tech Trade News*

# Is Drauger OS entirely FOSS?

All the code that ships with Drauger OS by default is open-source. We ship a package known as `steam-installer`, which handles installing Steam for the user, and the user has the option of skipping out on proprietary media codecs and the Nvidia and Broadcom drivers, so **Drauger OS ships with only open-source software, by default**. But, you will likely get a better experience by installing some proprietary bits.

# Drauger OS comes with a customized kernel, allowing higher frame rates for games, more stabilized performance, and reduced screen tearing. Is this specific to AMD or NVIDIA, or do both GPU vendors benefit?

This is going to help AMD users more than Nvidia users, since we have no way of optimizing Nvidia's driver due to it's proprietary nature. However, as an Nvidia user on Drauger OS myself, I can say there is little to no detriment to using this kernel. So things should work out just fine for GPUs from either vendor.

# Is there still an option for launching the OS straight into Steam Big Picture Mode on the login screen?

Yes! This actually had a pretty big rewrite a while back which got this functionality working again! It's slow to log out, and doesn't do well with multi-monitor set ups, but it works!

# Have you made a request to get a development kit for the Steam Deck?

No. I plan to buy one with my own money. That way, I have more of an excuse to play video games on it than just, "I'm benchmarking something!" or "I'm testing something!"

That, and if Valve ever requests Steam Decks to be returned to them, I won't have to worry about it.

# Speaking of the Steam Deck, what are your thoughts on the device?

I think it's a really compelling device. Similar devices are either much more expensive, much less repairable, have thermal issues, or some other issue that makes it a deal-breaker in my opinion. ARM-based alternatives, such as a computer in a similar form factor using a Raspberry Pi CM4 are either super hard to find, nonexistent, or have nowhere near the fit and finish of the Steam Deck. There's an option called the [Odin Pro](https://www.indiegogo.com/projects/odin-the-ultimate-gaming-handheld/#/) which uses a Snapdragon 845, but that's still a Kickstarter. And the Nintendo Switch is far less functional (I don't see anyone SSHing into servers or writing code on a stock Switch), far less upgradable, and it's much more difficult to change the OS on them.

![drauger os loading screen](https://boilingsteam.com/wp-content/uploads/boot_splash.png)
*Image credit: Boiling Steam*

# Last time [I reviewed Drauger OS on Boiling Steam](https://boilingsteam.com/hands-on-with-drauger-os/) a few years ago, one major problem was I couldn't install the NVIDIA drivers. Has that since been fixed?

Yes, that has been fixed for quite a while now.

What was happening is that version of Drauger OS in particular was using a kernel I compiled for Drauger OS. At the time, I had very little experience with doing this, and was compiling the latest kernel version straight off the Linux kernel `git` repository.

Come to find out, the Nvidia driver does not like kernels that are that bleeding edge. If we fell back to the Liquorix kernel (the kernel we were using beforehand), the Canonical-sanctioned "generic" kernel, or the Xanmod kernel (the one we use now), the Nvidia drivers compiled and installed just fine.

We are retrying [to] compile the Linux kernel for ourselves internally, but we are being much more careful about it. We are not going to switch over to this in-house kernel until we can reliably build kernels that work with the Nvidia drivers. Until then, we are sticking with the Xanmod kernel.

# Do you have any idea as to how large the install base is?

I don't have any concrete numbers. But I can make a VERY rough, ball park estimate, but it requires a bit of math.

Starting off, pulling information about number of downloads (which you can see [here](https://download-optimizer.draugeros.org/stats)), September thru February, we averaged about 5,239 downloads per month. 

All these numbers that follow are literally just random guesses that seem reasonable. Take them with a grain of salt.

Assuming about 35% of those who downloaded the ISO actually tried the OS, about 25% of THOSE people actually installed it, and 85% of those installations were successful, that leaves use with an **average of 390 new users per month**. 

Beyond that, we have to start figuring out retention rate and things like that. And I have no idea what a good guess for any of that would be, so I'll stop with the math there and let people relax from that a bit! But if I had to give a decent guess based off that number, I'd have to guess maybe about 700 users worldwide at most.

![drauger os logo](https://sempreupdate.com.br/wp-content/uploads/2020/03/1981967-1562223043038-1afa1f412c78a.jpg.webp)
*Image credit: SempreUpdate*

# What has the general feedback for the distro been like?

Other than the occasional bug with the installer, it's been mostly positive. The biggest request I hear from users these days is that they want dual-boot support in our bootloader of choice: `systemd-boot`. I'm working on that literally right now (I have the code open on my other monitor as I type this).

A lot of people seem to like that we have a package called `nvidia-driver-latest` that handles installing the latest Nvidia driver and disabling Nouveau for normal users. I tend to suggest it for people running 1000 series Nvidia cards and newer. But it definitely makes people's lives easier. I've seen that a number of times.

Outside that, we get a lot of requests for a KDE version, to which I always tell people that it would require a lot of effort from us to do that. But if Xfce doesn't get Wayland support within the next year or two, we may have to bite the bullet and switch to it.

# The [Drauger OS console](https://boilingsteam.com/drauger-os-developer-looking-to-make-console/). How's that coming along?
It's stagnated due to the chip shortage. There is an enclosure on our [GitHub](https://github.com/drauger-os-development/Vetala-Case), but we need people to test it and provide feedback about things that need to be improved. But since they're so big it's hard to 3D print them. So that's about as far as we have gotten for now. Once the chip shortage eases up we hope we can pick back up on it.

# If you could summarize in a sentence or two why people should use Drauger OS, what would it be?

If you have at least a little Linux experience, and want a Linux distro you can tinker with that will provide fantastic gaming performance: Drauger OS is for you. It's a little quirky, but overall, it provides a great experience to anyone who doesn't mind tinkering a bit sometimes.

# Any concluding thoughts you'd like to share with us?

I look forward to the future of Drauger OS! We've come a long way since the initial release back in 2018. I'm excited to see where the next 4 years takes us. We're already switching our audio back-end to Pipewire with the next release, and exploring the possibility of switching to Wayland in the future.

If you ask me, the future looks bright for Drauger OS.

It does seem to look bright indeed! If you want to give Drauger OS a spin, head to the [official website](https://draugeros.org).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
