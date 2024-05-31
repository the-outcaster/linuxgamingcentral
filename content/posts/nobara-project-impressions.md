+++
title = "I Joined the Fedora Bandwagon (Nobara Project). Here's My Thoughts"
date = 2023-01-11T18:16:56Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nobara/impressions/desktop.webp"
tags = ["impressions", "fedora", "nobara"]
keywords = ["fedora", "nobara project", "nobara"]
description = "I might not ever go back to Arch again."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Back in June, when I first talked about [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project/), I had mentioned this:
> If Arch ever breaks on me I might just switch over to this.

Well, that day has finally come. Although, it wasn't necessarily Arch's fault; it was more so my *own* mistake of breaking the system that finally gave me the excuse to try out Nobara Project. At any rate, I've heard time and again the good things about Fedora, so I wanted to give this distro a shot.

*Please do NOT interpret this article as a review. This is more so just a quick impressions on Fedora/Nobara Project while using it over the past few weeks.*

In case you're not aware, Nobara Project is a modified version of Fedora that comes with a few tweaks, particularly in the gaming aspect and the pre-installed suite of applications. Per the description on the [official website](https://nobaraproject.org/):
> The Nobara Project, to put it simply, is a modified version of Fedora Linux with user-friendly fixes added to it. Fedora is a very good workstation OS, however, anything involving any kind of 3rd party or proprietary packages is usually absent from a fresh install...This project aims to fix most of those issues and offer a better gaming, streaming, and content creation experience out of the box. More importantly, we want to be more point and click friendly, and avoid the basic user from having to open the terminal.

The distro was created by Thomas Crider (GloriousEggroll), the person who's also responsible for the development of the excellent [GE-Proton](https://linuxgamingcentral.com/tags/ge-proton/). I'll have to ask him where he got the name "Nobara" from (the only thing that showed up on DuckDuckGo was the name of a [girl](https://jujutsu-kaisen.fandom.com/wiki/Nobara_Kugisaki) from a Japanese anime). Regardless, I kind of dig the fact that the distro doesn't have "OS" appended to it. Just keep it simple, like Nobara Project. I like it.

So...this article ended up being *a lot* longer than I expected. If you're just here for Nobara itself, you can skip to [the appropriate section](#difference-between-nobara-project-and-vanilla-fedora). The next few sections will go over vanilla Fedora and the benefits it has.

# Stable, While Cutting-Edge
It's nice having bleeding-software with Arch. Only problem is the software has *barely* been tested. So while you might be getting the benefits of [kernel 6.1](https://linuxgamingcentral.com/posts/kernel-6.1-released/) with faster btrfs speeds, you're also going to have [suspend issues](https://lists.archlinux.org/archives/list/arch-general@lists.archlinux.org/thread/YUTWVY6LIZDS4H63CT6N2WXHB3FYXUKA/). Your version of GLIBC might have upgraded to 2.36, but now [certain games with EAC won't run](https://linuxgamingcentral.com/posts/glibc-eac/).

![Cutting-edge versus bleeding-edge](/images/nobara/impressions/CUTTING-EDGE-vs-BLEEDING-EDGE.jpg)
*Image credit: [Constant Tech](https://constanttech.com/the-importance-of-cutting-edge-vs-bleeding-edge-technology/)*

Even though the latter issue may have been patched later on, the problem still remains that users *will* come across regressions from time-to-time, due to these packages being pushed out before they're ready for prime time. So rather than having users deal with regressions, Fedora stays behind. Right now, on Nobara 37, I'm on kernel 6.0-18. Basically, the latest *stable* kernel as of the time of writing this. And Nobara in particular already has the EAC regression fixed for GLIBC 2.36. So, the beauty of Fedora is it strikes a good balance between having the latest software, while also ensuring it's not broken.

# A More Robust Package Manager
When updating packages on Ubuntu-based distros, you'd typically run:
```
sudo apt update
sudo apt upgrade
```

On Fedora, the DNF (Dandified YUM) package manager simplifies this to just one command:

`sudo dnf update`

Although you may need to pass the `--refresh` flag to force the cache to refresh if you run the command twice within a three-hour period. The system will not only check for updates, but ask if you want to upgrade any of the packages if there is an update available.

![dnf update example](/images/nobara/impressions/dnf_update.png)

As you can see here, DNF will install six packages, upgrade 115 of them, and uninstall seven. The thing that I also like about DNF is that it forcefully makes you type in "y" if you want to proceed. By default if you press Enter without typing "y" in, the packages won't upgrade, unlike other package managers. This makes you cognizant of what you're doing, and makes sure that you actually *are* ready to upgrade. This same principle applies if you're installing a new package or uninstalling an existing one.

Here's another benefit of DNF: let's say you tried to run an application through the terminal that isn't installed on your system. Depending on the package, you'll get a prompt asking if you want to install said application. You don't get that on Ubuntu, or Arch for that matter. Just get a dead "package not found."

![Running spectacle without it installed](/images/nobara/impressions/running_spectacle_without_it_installed.png)

# COPR - The AUR Equivalent for Fedora
Some might argue, "Arch has the benefit of the AUR -- you can get just about any kind of package!" True that. However, Fedora essentially has an AUR equivalent: Community Projects ([COPR](https://copr.fedorainfracloud.org/)). For instance, if you wanted to upgrade to kernel 6.1 anyway, ignoring the suspend issues, you could add [this repo](https://copr.fedorainfracloud.org/coprs/g/asahi/kernel/) and install the package from it to your system.

![dnf update example](/images/nobara/impressions/copr.png)

COPR might not have the same amount of packages available as the AUR, but as Fedora becomes more popular, I would imagine so will the COPR getting filled with community packages. (Don't be surprised if you see me add [Slippi](https://linuxgamingcentral.com/tags/slippi/) at some point.)

# Embracing New Technologies Before Anyone Else
Here's the funny thing: even though Fedora tries to be stable, it's also the distro that tries to push new technologies forward before anyone else. For example, back in late 2020 with the release of Fedora 33, it uses **btrfs as the default file system** when installing. Most distros today, including Pop!_OS, still use ext4 as the default. Now whether you prefer ext4 over btrfs or vice versa, is your preference. But btrfs *does* have the advantage of compression. When I switched my Steam Deck's file system over to btrfs, I saved [over 50 GB of space](https://linuxgamingcentral.com/posts/save-disk-space-on-deck-with-steamos-btrfs/)! So, if you want to be able to install more games on your system, btrfs is the way to go.

![Fedora 37 desktop](/images/nobara/impressions/logo-horizontal-white.svg)

Red Hat Enterprise Linux (RHEL) -- for which Fedora serves as the upstream source -- was also the one to **embrace the first stable release of Flatpak** back in December 2016 along with Debian. It wouldn't be until later on that other distros would adopt this sandboxing technology, for keeping your root files untouched. Flatpaks would become popular enough that [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos/) and SteamOS 3 would use it so users could still run their favorite applications while keeping the file system immutable.

Finally, Fedora 33 had **[ZRAM](https://linuxgamingcentral.com/posts/pop-os-gets-zram-upgrade/) enabled out-of-the-box**, providing increased performance in games on systems with low RAM with the use of compression. Just a few days ago, Pop!_OS incorporated this. Fedora already had it for two years.

# Fedora Keeps Things Vanilla
Many distributions ship with GNOME out-of-the-box. These distributions will often modify GNOME to make it more akin to their users' taste. Fedora keeps GNOME as vanilla as possible, with little to no tweaks. Other packages like the kernel also remain largely untouched.

![Fedora 37 desktop](/images/nobara/impressions/fedora_37.webp)
*Image credit: [How-To Geek](https://www.howtogeek.com/835679/whats-new-in-fedora-37/)*

Nobara *does* come with a few tweaks, however, which I'll get into now.

# Difference Between Nobara Project and Vanilla Fedora
Fedora itself is great, but Nobara Project takes things a step further by including non-free software, such as the NVIDIA graphics drivers -- which, on vanilla Fedora, can be a bit of a pain. But there's *tons* of other features, improvements, changes, the whole nine yards, which I've listed below.

**Enhancements**
- patched kernel with: 
  - [Zen](https://liquorix.net/#features) patches
  - [OpenRGB](https://openrgb.org/)
  - [AMD CPPC](https://www.phoronix.com/review/amd-pstate-first) (optimizes Ryzen CPUs, although from the looks of it [it doesn't seem to do much better](https://www.reddit.com/r/Amd/comments/pbbqd0/cppc_enabled_vs_disabled/))
  - AMDGPU enabled for pre-Polaris cards instead of Radeon
  - **Steam Deck support** and Windows Surface support
  - [Waydroid](https://github.com/waydroid/waydroid) support
  - better [ASUS laptop support](https://gitlab.com/asus-linux/asusctl)
  - fix for [simpledrm](https://gitlab.com/cki-project/kernel-ark/-/merge_requests/1788) on NVIDIA
  - better [VFIO IOMMU group control](https://aur.archlinux.org/cgit/aur.git/tree/add-acs-overrides.patch?h=linux-vfio)
- pre-installed applications: 
  - Steam
  - Lutris
  - MangoHUD
  - GOverlay
  - GameScope
  - OnlyOffice
  - CUPS/printer drivers
  - [Vapoursynth](http://www.vapoursynth.com/about/) with [ffms2 patch](https://bugzilla.redhat.com/show_bug.cgi?id=1835641)
  - Wine
  - [ProtonUp-Qt](https://linuxgamingcentral.com/tags/protonup-qt/)
- GNOME:
  - [VRR support](https://gitlab.gnome.org/GNOME/mutter/-/merge_requests/1154) for Mutter, GNOME's window manager
  - [X11 fractional scaling](https://salsa.debian.org/gnome-team/mutter/-/raw/ubuntu/master/debian/patches/ubuntu/x11-Add-support-for-fractional-scaling-using-Randr.patch) support
  - GNOME extension manager can [auto-update](https://gitlab.gnome.org/GNOME/gnome-shell/-/merge_requests/2358) without needing the GNOME extension app
- latest Mesa drivers and mesa-git Vulkan drivers
- NVIDIA drivers are automatically installed if said GPU is detected during installation
- you have the option of installing video codecs after installation
- a package is provided for easy installation of [xone](https://github.com/medusalix/xone) and [xpadneo](https://github.com/atar-axis/xpadneo)
- better Nouveau Wayland support
- [GameScope](https://github.com/Plagman/gamescope), [GOverlay](https://github.com/benjamimgois/goverlay), [MangoHUD](https://github.com/flightlessmango/MangoHud), and [vkBasalt](https://github.com/DadSchoorse/vkBasalt) all "regularly updated"
- Blender includes ffmpeg support and [HIP support](https://www.phoronix.com/news/Blender-3.0-AMD-HIP-Ready) for AMD GPU rendering
- DaVanci Resolve has [dependencies installed](https://nobaraproject.org/docs/davinci-resolve/configuring-davinci-resolve-with-amd-gpus/) so you will be all set after installing said application
- patches for OBS Studio, including a browser plugin, Vulkan/OpenGL capture, NVENC, PipeWire audio capture, and more
- Wine includes 32-bit/64-bit dependencies for easier Lutris and Wine gaming
- Discord comes with "enhancement launch options" (but the application isn't included by default)
- *League of Legends* can be run via Flatpak with an included [patch](https://github.com/flatpak/flatpak/issues/4297)

![Nobara Project running on Deck](/images/nobara/impressions/nobara_on_deck.jpeg)
*Nobara running on Deck*

**Changes**
- Flathub and RPMFusion repos enabled by default
- GNOME: increased wait kill timer from five seconds to 30 -- useful for games that take longer than five seconds to load, such as *League of Legends*
- max parallel downloads with Fedora's DNF package manager increased from three to six
- vm.max_map_count = 16777216 set by default for [*Star Citizen*](https://robertsspaceindustries.com/star-citizen/)
- Nautilus, GNOME's file manager, restores the classic type-ahead functionality, the toggle between breadcrumb and text navigation, and fixes drag n' drop functionality when extracting files
- [AppArmor](https://www.apparmor.net/) replaces [SELinux](https://www.redhat.com/en/topics/linux/what-is-selinux) since it's "more user-friendly, less intrusive, and easier to write policies for"

![Nautilus search](/images/nobara/impressions/file_manager.png)

**Fixes**
- patched GLIBC that [borked certain EAC games](https://linuxgamingcentral.com/posts/glibc-eac/) and fixes Chrome Embedded Framework (CEF) compatibility with outdated CEF versions
- Wine fix when creating new prefixes
- locked FPS fixed on [XWayland](https://build.opensuse.org/package/view_file/home:hwsnemo:xwayland/xwayland/xwayland-vsync.diff?expand=1)
- fix for [*Dying Light*](https://www.gamingonlinux.com/forum/topic/2766/page=12/#r17381)

Wow. Quite a list, huh?

# Editions
Nobara comes in three flavors: official, GNOME, and KDE. Official is basically GNOME with a few extensions enabled to make it more akin to Windows, with a taskbar at the bottom, a launcher on the bottom-left, your favorite applications next to that, and status icons on the lower-right.

![Nobara 37 official](/images/nobara/version_37.webp)

I actually kind of dig the official flavor, a lot. See, vanilla GNOME is just *way* too simplified for me. In contrast, while KDE has a more familiar desktop appearance, it's much too bloated for my tastes. So the official flavor is *perfect* for me. It's GNOME with more sophistication, and if you're a Windows user you'll definitely appreciate the similar appearance.

Prior to downloading any of the flavors, you will have a EULA to either agree or disagree. Obviously, if you don't agree, you won't be able to download the ISO.

![Nobara EULA](/images/nobara/impressions/eula.png)

# Nobara Welcome
After Nobara is installed (I'd have a few screenshots showcasing the installer but sadly no VM software is working for me at the moment), you'll be greeted with a welcome screen. Frankly, I'm turned off by any sort of pop-ups that appear on my screen when I log in -- but thankfully there's a checkbox that you can tick to disable the window from appearing on future logins (you can open this back up later on under the "Accessories" menu from the launcher).

![Nobara welcome screen](/images/nobara/impressions/welcome.png)

On this welcome screen you can:
- update your system
- install patented media codecs/libraries (although you may have been prompted to install this before)
- install the proprietary NVIDIA/AMD drivers (although you may have been prompted to install this before)
- install webapps
- install/remove Blender, Kdenlive, OBS Studio, Discord
- install xone/xpadneo drivers
- install GE-Proton
- launch the GNOME Software Center/KDE Discover, depending on what DE you're using
- customize the look and feel of your desktop
- visit the [troubleshooting](https://nobaraproject.org/docs/upgrade-troubleshooting/) and [documentation](https://nobaraproject.org/docs/) sections on the official site
- join the [Nobara Discord](https://discord.gg/6y3BdzC) or the [subreddit](https://www.reddit.com/r/NobaraProject/)
- open various links to contribute to the project

It's actually kind of nice. You can do all of this with just a click of a button. No need to enter a terminal. Certainly useful for newcomers to Linux. I'm not sure if it was intentional to add "Update my system" to both the First Steps and Troubleshoot Issues tabs, but to me I dislike the duplicate option. Just pick one tab or the other.

![Nobara welcome screen first steps](/images/nobara/impressions/first_steps.png)

Another improvement I'd like to see is, say for example I install the third-party media codecs. After they're installed, the welcome screen still says "Launch". There should be a change in the button label to indicate that they've been installed. And there should also be an option to uninstall if for some reason the user changes their mind.

# Different Software Managers
A note when it comes to installing software on Nobara with a GUI -- you have both the Nobara Package Manager and the GNOME Software Center (or KDE Discover if you're using Plasma). The difference I've seen between the two applications is I would use the Nobara Package Manager for installing native RPM packages. The GNOME Software Center is useful for installing Flatpaks. Just try not to get yourself confused between the two software managers.

![Nobara package manager](/images/nobara/impressions/package_manager.png)

![GNOME software center](/images/nobara/impressions/gnome_software_center.png)

# Impressions
I like Nobara. As a long time Arch and Pop!_OS user, it wasn't as much of a learning curve than I thought it was going to be. It's stable, yet still provides up-to-date software, and includes bleeding-edge Mesa Vulkan drivers. Very useful for my 6700 XT. It's also nice to have a bunch of gaming utilities set up out-of-the-box. I didn't need to look for and install Steam, MangoHUD, GOverlay, and ProtonUp-Qt -- those were all provided, saving me some time.

Interestingly enough GameMode is NOT included with Nobara, but you can install it with `sudo dnf install gamemode`.

Apparently the patched kernel includes [FUTUX2](https://www.phoronix.com/news/FUTEX2-2021-Still-WIP), which supposedly improves performance for games played with Proton. I haven't really seen a difference to be honest, at least based on the naked eye. Regardless, the gaming experience has been pretty great so far. Not perfect though, as I'll get into later.

![OBS hotkeys](/images/nobara/impressions/obs_hotkeys.png)

I did have an issue concerning hotkeys with OBS Studio. The only way I could get hotkeys to work is if the application is in focus. This isn't a issue with Nobara necessarily; [it's more so a problem with Wayland](https://www.reddit.com/r/wayland/comments/innoc5/obs_wayland_the_shortcuts_dont_work/). The only solution I found for Fedora specifically was by digging up a year-old [Reddit thread](https://www.reddit.com/r/Fedora/comments/omcxr7/fixing_obs_keybindings_on_wayland_on_fedora/), and even then I had to modify the commands a bit to make sure it was working on my end.

Another problem is occasional game crashing with [*Crisis Core* remake](https://linuxgamingcentral.com/posts/crisis-core-remake-on-deck-report/). On Steam Deck, the game plays *perfectly*, without any random crashing. On Nobara with my 6700 XT, however, there is random crashing from time to time, particularly when performing a Limit Break or before a cutscene triggers. There's a variety of factors as to why this is: it could be the bleeding-edge Mesa Vulkan drivers, it could be GE-Proton, it could be the FUTEX2...I'm not sure. Disabling GameMode didn't help, and downgrading GE-Proton didn't help either. I'd have to do some more testing to see if I can replicate the issue across other games.

I'm kind of curious why Nobara went with OnlyOffice as the pre-installed office suite rather than LibreOffice. I do recall [Manjaro getting backlash](https://dnetc.net/manjaro-and-the-controversy-with-the-offices-suites/) for including said suite with their installer some time ago. Was there any particular reason why Nobara adopted this move? Can't say that I'm a fan of this decision.

# Arch? Only if I Need To
Don't get me wrong: I still like Arch. But going forward I'm only going to use it if I *really* need bleeding-edge software for some reason. As I said, Fedora keeps packages new, while at the same time making sure they actually don't break on the user. The DNF package manager is more robust in my opinion, there's the COPR for obtaining community-maintained packages, it uses btrfs by default, and ZRAM is enabled. On top of this Nobara's spin of Fedora with the "official" desktop environment is great, it provides most of the gaming-related packages I need out-of-the-box, comes with a few gaming-oriented tweaks, and most, if not *everything* can be done without the use of a terminal, thanks to the welcome screen.

![Arch VS. Fedora meme](/images/nobara/impressions/arch-vs-fedora.png)

I did have a few issues with hotkeys and *Crisis Core* remake suffering from a few random crashes. The former issue is more so Wayland's fault though. As far as the latter, I'll need to investigate what's causing the crash. Also not a fan of OnlyOffice being included in the installation. But Nobara Project is still *awesome*. Thanks, Eggy!

**TL;DR**

The good:
- more robust package manager
- COPR allows users to install unofficial packages maintained by the community
- embraces new technologies before other distros
- cutting-edge software that has still been tested before it goes out to the public
- "official" Nobara flavor makes GNOME more Windows-like in appearance
- plenty of gaming packages provided out-of-the-box, along with many tweaks to the kernel for gaming performance boosts

The not-so-good:
- crashing issues with *Crisis Core* remake
- welcome screen could use a few improvements as far as duplicate options and letting the user know whether a certain package is installed or not
- OnlyOffice included with base install
- hotkey issues with OBS Studio (more so a Wayland issue though)


Want to give Nobara Project a shot? Head over to the [official site](https://nobaraproject.org/) to get started!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
