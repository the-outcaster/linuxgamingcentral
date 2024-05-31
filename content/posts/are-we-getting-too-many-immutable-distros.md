+++
title = "Are We Getting Too Many Immutable Distributions?"
date = 2023-01-31T16:46:16Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/opinions/immutable_fs/cover.webp"
tags = ["opinion", "immutable distros"]
keywords = ["immutable file system", "immutable file system inconvenience",  "immutable file system issues", "vanilla os", "blendos", "pop!_os", "chimeraos", "steamos", "steam deck", "flatpak", "flatpak issues", "flatpak permission issues", "appimage", "snaps", "distrobox", "containerization"]
description = "Flatpak: more like pain-in-the-asspak?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A bit of a random topic, but lately I've been seeing this trend where new distributions are being made (or, dare I say, *copied* or *stolen* from other projects), where the idea is to keep the core filesystem immutable, but allow the user's home directory to be writable. And while I think that's a great concept on paper, to me it causes more headaches than it offers security or other benefits.

Take, for example, [Fedora Silverblue](https://silverblue.fedoraproject.org/), which was first released to the public in October of 2018. Per the description on [Wikipedia](https://en.wikipedia.org/wiki/Fedora_Linux), the idea of having immutability in the first place is as follows:
> The immutable design is intended to make the operating system more stable, less prone to bugs, easier to test and develop, and create a platform for containerized applications as well as container-based software development.

![Fedora Silverblue logo](/images/opinions/immutable_fs/silverblue-logo.svg)
*Image credit: Fedora team*

And then shortly thereafter some other distributions would follow suit. [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos/) is an example. And then [Valve (mostly) copied off from the ChimeraOS team](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/#looks-like-valve-took-a-lot-of-hints-from-chimera-the-immutable-file-system-the-use-of-flatpaks-for-applications-outside-of-games-and-arch-as-the-base-system-did-they-ever-acknowledge-you-at-any-point-in-time) with SteamOS 3. And now that you have a larger, more popular entity doing this, the idea is becoming more attractive to distro developers. More distributions would come after that, whether they thought it was a good idea or not.

[Vanilla OS](https://linuxgamingcentral.com/posts/vanilla-os/). [blendOS](https://9to5linux.com/first-look-at-blendos-a-blend-of-arch-linux-fedora-linux-and-ubuntu) (which, from what I heard, supposedly steals a lot of code from Vanilla OS). And it looks like Pop!_OS is appearing to [get into it](https://github.com/pop-os/core) as well.

![Vanilla OS](/images/opinions/immutable_fs/vanilla_os.webp)

I'm all for the security benefits of locking the core system files. And as the description from Wikipedia puts it, it also makes the OS "more stable, less prone to bugs." But, of course, there's always the opposite side of the coin. While increasing the security of your system, you're paying in terms of convenience.

Take, for instance, that basically your set of software to use is limited to Flatpaks and AppImages (and maybe Snaps if your distro supports them).

# Flatpak Woes
Someone once jokingly referred to Flatpaks as a "pain in the asspak." And honestly, in some ways it *is*. 

Okay, so maybe with the advent of SteamOS 3, more and more Flatpaks are becoming available on Flathub. And the advantage of Flatpaks is that they are sandboxed and in isolation from the rest of the system. But now you have to deal with the fact that some software is just *not* available on Flathub. Add to this the convoluted naming scheme. So if you wanted to install Firefox, you would install it this way in the terminal:

`flatpak install flathub org.mozilla.firefox`

And every time you wanted to run it, you would have to add that whole reversed domain name:

`flatpak run org.mozilla.firefox`

No one is going to want to type that whole phrase in to run Firefox. And while you could alias the command to something like `echo "alias firefox='flatpak run org.mozilla.firefox'" >> ~/.bashrc` so you can run it with just `firefox`, that's yet *another* command that you have to run for convenience' sake. Nevermind the fact that on some distros, you'll first need to [install Flatpak and enable the Flathub repo](https://flatpak.org/setup/) if it doesn't do that out-of-the-box.

![Trying to add an attachment with Discord Flatpak](/images/opinions/immutable_fs/adding_attachment_in_discord_flatpak_fail.png)

Permission issues? Yep, there's that as well. Now you have to use something like Flatseal and manually add the permissions for *each* app. Yet another tool that you have to install and use to make another app work the way it was intended.

"Permission issues? What are you talking about?" you might ask. Say you have Discord installed as a Flatpak. Then you want to attach a photo or document and send it off to someone. The only folder locations that Discord has access to, by default, is `Videos`, `Pictures`, and `Downloads`. If you want to send a file, either the file has to be in one of these three folders, or if you want to attach the file from elsewhere, you'll need to add the folder path with Flatseal.

So at the end of the day there's three issues:
1. Not all software is available as a Flatpak.
2. Convoluted naming scheme; running the app via the terminal isn't exactly convenient.
3. Permission issues, which require *another* Flatpak to be installed and configured.

# AppImage
Out of all three universal packaging systems, AppImage is probably my favorite. They're super portable, they have all the dependencies included to run across virtually *any* distribution, and they don't have any permission issues. Yet, problems are present here as well:
1. It doesn't appear that we'll be getting [Wayland support](https://linuxgamingcentral.com/posts/appimage-dev-rejects-wayland-support/) any time soon, unless someone forks LinuxDeployQt and adds support that way.
2. AppImages have to be manually updated; most of them don't have a self-update mechanism.
3. AppImages are just files, so if you want to integrate them into your system, you have to use something like [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher). Even then, you're limited to the *Lite* edition if your file system is immutable.

![AppImageLauncher integration prompt](/images/opinions/immutable_fs/adding_attachment_in_discord_flatpak_fail.png)

# Snaps
I think Snaps are kind of out of the question; [everyone and their brother hates Snaps](https://linuxgamingcentral.com/posts/interview-with-canonical-dev/#you-had-alluded-to-snaps-as-being-unpopular-why-is-there-so-much-controversy-behind-snaps-from-your-viewpoint-what-are-the-advantages-of-this-packaging-system) for a plethora of reasons, including Snaps not respecting the user's theme and taking a long time to load. So we can rule this packaging system right out of the gate, unless you're using Ubuntu. And Ubuntu itself isn't immutable, so...

# Containerized Distros
[Distrobox](https://linuxgamingcentral.com/posts/distrobox-1.4-adds-steam-deck-documentation/), to me, is *brilliant*. With it, you can basically run *any* kind of distro -- be it Arch, Fedora, Ubuntu, etc. -- inside of your host system via a container. This way you can install and run packages on your host machine, even if it may be immutable. On Steam Deck, this is a *great* addition to have.

![Distrobox](/images/distrobox/cover.jpg)

Vanilla OS also incorporates the idea. Although it's using Ubuntu as the base, you also have the ability to install Arch and Fedora packages on the same system. That's pretty convenient, thus eliminating the need to distrohop.

And yet, sadly, this *still* has its disadvantages.

I installed Vanilla OS on a spare hard drive and I was almost immediately turned off by it. Yes, I basically have three distros in one. But the core file system is locked. Sure, I can install Ubuntu, Arch, and Fedora packages with their unique `apx` package manager, which installs the packages through a container. But what about drivers? I couldn't get my [GameCube controller](https://linuxgamingcentral.com/posts/phobgcc-review/) adapter to work at all. On some distros, the adapter works out of the box. But this particular distro doesn't.

So I needed to install [wii-u-gc-adapter](https://github.com/ToadKing/wii-u-gc-adapter). And this requires building from source. So of course, I can't do that on Vanilla OS without using a container, since it lacks the dependencies needed to install the package. The only way I can install those dependencies is if I use a container. Even then, after being able to successfully compile the package, Slippi just *refused* to pick up the adapter when running the driver. I've no idea why, and the developers of Vanilla OS didn't know either.

![Vanilla OS - can't use Mayflash adapter](/images/opinions/immutable_fs/unable_to_use_gcc_adapter_on_vanilla_os.webp)

The only other solution I could think of was just to build Slippi from source and see if that would solve anything. No, of course it didn't. The thing that is a *huge* PITA with Vanilla OS is, even though you *can* install a dependency on the native system, the problem is you need to restart the OS *every time* you make a change to `apx`. So I install a couple of dependencies for the Dolphin emulator, run the compile script, and the script lets me know I'm missing a dependency. So I install that dependency, restart the system, run the script again. After having to reboot the system half a dozen times just to make sure I have all the dependencies I need, Slippi still wouldn't compile and I just gave up.

And look, I know half of my followers could care less about a 21-year-old game, but to me, this is a deal breaker. When I come home from a long day at work, I want my software to *just work*. I don't want to have to spend half a day trying to figure out why I can't play *Melee* without my GCC adapter.

# Unlocking the File System Doesn't Solve the Problem
On some immutable systems like SteamOS, you can unlock the file system with:

`sudo steamos-readonly disable`

Does this mean that you can install Arch packages? Not necessarily. First, Valve butchered most, if not *all* of Arch's repos. Making simple packages like `neofetch` a *huge* pain to get. Even if you do manage to get an Arch package installed, you have to contend with the fact that said package will likely get wiped with the next SteamOS update. All that hard work you put forth just to get that package to display your system info just went to the wastebasket.

# Do You Really Want to Use an Immutable Distribution?
If this article sounded more like a rant than it was an opinion, well, I guess I'm just frustrated at all the hassle immutable distros cause. Flatpaks, AppImages, and Snaps were all made as a way to compliment additional software to the end user without touching the root filesystem, but each packaging system has their own set of quirks. Look, I understand the idea is increased security. Newcomers to Linux will certainly appreciate this, as it reduces their chances of breaking the system. But what you get for security, is what you have to pay for in terms of convenience.

![Vanilla OS - can't use Mayflash adapter](/images/opinions/immutable_fs/security_vs_convenience.jpeg)
*Image credit: ROKKEX*

As such, I don't like seeing this trend of more and more distributions adopting this immutable file system scheme. Compiling software or drivers is going to be *way* more of a hassle than it's worth. On top of this you will likely want to use software that *isn't* available as a Flatpak or AppImage. Even if it is available, you either have permission issues -- which are going to take even *more* steps to solve than just installing the software as a native package -- or you don't have a convenient way of updating the software if it's an AppImage. And Snaps...well, let's just forget about that. Installing software through a container might be a temporary solution, but in some ways that *still* causes issues. Unlocking the file system is an inconvenience and whatever changes you make will likely get wiped with the next update.

So I think if I were to wrap this article up in a nutshell it would be this: immutable file systems are good for newcomers to Linux. But for more experienced Linux users and developers, a mutable file system is the way to go.

What do you think? Do you think the idea of having an immutable file system is a good idea or not? And should more distros adopt this idea or slow it down?

*Cover image credit: Dmitry Lepisov*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
