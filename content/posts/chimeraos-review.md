+++
title = "Turn Your PC Into a Console With ChimeraOS"
date = 2023-03-03T15:23:17Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/distro_reviews/chimeraos/cover.jpg"
tags = ["distro review", "chimeraos"]
keywords = ["chimeraos", "chimeraos review"]
description = "You really need to give it a try."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
On my [to-do list](https://github.com/linuxgamingcentral/website) was this:
> An article dedicated to my favorite group of developers…but I’m not going to reveal what it is just yet *wink*.

Well, I'm about to reveal what exactly that article is. It's this. A review -- and a tribute -- to what, in my opinion, is the best gaming distro of all time. Only sad part is I'm a bit late to the party; [ETA Prime](https://www.youtube.com/watch?v=E2NIGPpz_vY) kind of stole my thunder when he covered the distro last week on his channel. I wanted to be the first one to surprise the dev team, as they're my favorite group of developers. They're some of the most humble people that I know. Need to make a note to myself to work a bit faster next time.

At any rate, I simply *can't* go about my daily routine without giving a shout out to ChimeraOS. It's a distro that I've reviewed [a few years ago](https://boilingsteam.com/gameros-an-enhanced-version-of-steamos/), and I wanted to come back and see what has been improved over the last three years.

![ChimeraOS CSS theming changed](/images/distro_reviews/chimeraos/melee_preview.jpg)

For starters, in case you're not aware of what [ChimeraOS](https://chimeraos.org/) is, it's an Arch-based Linux distribution that's designed to run Steam's Big Picture interface on startup. The idea is you can transform your desktop PC into a console by having a controller-driven interface, without ever needing to connect a keyboard or mouse. Basically, it was the much-needed spiritual successor to the old SteamOS 1.0/2.0, that got rid of *a lot* of the headache that came with SteamOS prior to version 3.0. It also provided an enhanced experience with things like the [Chimera web app](https://github.com/ChimeraOS/chimera), which allows the user to add ROMs and certain Flatpak applications with another device connected to the same network.

ChimeraOS also comes with enhanced security by keeping the core filesystem immutable. Updates to ChimeraOS -- things like the kernel, the graphics driver, etc. -- are handled entirely by the ChimeraOS team and not the end user. This allows for curated packages, ensuring they're properly tested and working before they are shipped to the end user. If something goes wrong, it's usually because of the ChimeraOS team, not the user.

That being said, users *can* still make use of their own software through the use of Flatpaks. These Flatpaks can be added through the aforementioned Chimera app, or by using the GNOME Software Center in Desktop Mode. Users can also unlock the file system via a terminal command, and install packages with pacman.

![Metroid Prime Remastered on ChimeraOS](/images/distro_reviews/chimeraos/mpr.jpg)

Sound familiar? That's because that is pretty much what SteamOS 3.x does. Like ChimeraOS, SteamOS 3 is based on Arch, uses an immutable file system, and makes use of software outside of Steam via Flatpaks. So here's an interesting tidbit that I'd like you to know: **the ChimeraOS team were the first ones to implement this idea.** Valve quietly copied these ideas into SteamOS 3, without ever acknowledging the ChimeraOS team. It seriously makes me wonder what SteamOS 3 would have been like if it weren't for ChimeraOS. ChimeraOS founder, Alesh Slovak, even [hinted](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/#looks-like-valve-took-a-lot-of-hints-from-chimera-the-immutable-file-system-the-use-of-flatpaks-for-applications-outside-of-games-and-arch-as-the-base-system-did-they-ever-acknowledge-you-at-any-point-in-time) at this when I interviewed him back in April.

# Installation
Installation of ChimeraOS is simple. Just head over to the [Download page](https://chimeraos.org/download), download the ISO, and flash it to a flash drive. Boot from this media and, with a keyboard connected, go through the installation process. You'll be greeted with a black background with white text; typical of any Linux distro. But give it a minute or two and you should get a blue screen of death.

Heh, I'm kidding. But the screen *will* turn blue, and you should have a text-based installer (kind of similar to [archinstall](https://wiki.archlinux.org/title/Archinstall)). For some reason ChimeraOS couldn't detect an Internet connection on my end via Ethernet, so I had to go to the Configuration screen and connect from there.

![ChimeraOS installer Internet settings](/images/distro_reviews/chimeraos/internet.jpg)

Here's an improvement from three years ago: previously, you could only install the distro with an Ethernet connection. As of [version 25](https://boilingsteam.com/gameros-has-been-renamed-to-chimeraos/), it's possible to connect to the Internet with Wi-Fi and proceed with the installation.

After connecting to the Internet, be it Ethernet or Wi-Fi, you'll be asked what disk to install the distro on. You won't be able to dual-boot with this distro; not on the same drive anyway. But if you have a seperate hard drive to spare, you can install ChimeraOS on this, and still retain other operating systems if they're on a different drive. Be aware the drive you select will be formatted, so if you have data on it, be sure to back it up before proceeding.

![ChimeraOS installer disk choice](/images/distro_reviews/chimeraos/disks.jpg)

The installer will download the latest image of ChimeraOS (which, at the time of writing this, is [version 39](https://linuxgamingcentral.com/posts/chimeraos-39/)), extract it, then install. Overall the installation shouldn't take any longer than five minutes. Once installed, you'll be asked if you want to reboot. If not, you'll be using the CLI. Not really sure what the point of that would be, so I would suggest restarting at that point.

After restarting, there's this new boot animation that plays. It's the ChimeraOS logo. The text will shine and will gradually move from left to right. Some stuff gets downloaded; apparently they're "configuration updates" but nothing more is described. I would assume it's downloading the Steam client and some minor ChimeraOS updates.

![ChimeraOS downloading configuration updates](/images/distro_reviews/chimeraos/downloading_updates.jpg)

As of version 39, the old BPM has finally been retired in favor of the new BPM, which the Steam Deck uses. Hopefully you're using an AMD GPU; you're going to have a sluggish experience if you're on NVIDIA (supposedly the beta Steam client [fixes NVIDIA performance in new BPM](https://linuxgamingcentral.com/posts/steam-deck-client-beta-update-2-17-2023/), but I cannot personally confirm this). If you're using NVIDIA, I would suggest opting into the beta Steam client for now; hopefully the navigation won't be as painful.

You'll go through the process as if you got your Steam Deck for the first time: language selection, and a "Welcome to Steam Deck" visual tour. Valve should really update the glyphs if the user is on desktop; right now the icons are all Steam Deck-oriented. (I wonder if it's possible to customize the glyphs yourself; there's probably some PNG files somewhere in the Steam installation folder.)

After all is said and done, you will be presented with the new Big Picture interface.

![ChimeraOS Deck UI home](/images/distro_reviews/chimeraos/deck_ui.jpg)

One suggestion for the ChimeraOS devs: would be nice if there was an installer ISO that *doesn't* require the use of an Internet connection.

# General Use
While the new BPM is nice, one thing you'll need to get used to is **Steam thinks you're using a Steam Deck**. So, for instance, when there's an update to Steam, the Settings menu will mention there's a new Steam Deck client update. Steam client update channel options are labeled as "Steam Deck Stable" and "Steam Deck beta". The Steam Input screen will show a Steam Deck by default. When installing a game, you'll still get the "Steam Deck compatibility" screen before installing. When viewing your Steam library, there's still the "Great on Deck" category. It's kind of silly on Valve's part to enable the new BPM by default on the stable Steam client branch, without even updating the icons if the user is on desktop. Not to mention the [bad performance on NVIDIA GPUs](https://boilingsteam.com/the-new-big-picture-mode-does-not-seem-to-work-well-with-nvidia-gpus-on-linux-clients/). Still, I'd rather take the new interface than the [archaic old BPM](https://linuxgamingcentral.com/posts/rip-old-bpm/).

![ChimeraOS Deck compatibility screen](/images/distro_reviews/chimeraos/deck_compatibility.jpg)

What actually kind of shocked me is **[Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader) actually works with ChimeraOS**. Not all the plugins work; particularly the [Audio Loader](https://github.com/EMERALD0874/SDH-AudioLoader). But most of them do. I was able to change the CSS theming in BPM. I was able to find out how much battery life my gamepad has with [ControllerTools](https://github.com/alphamercury/ControllerTools), and add artwork to non-Steam games with SteamGridDB. It was nice to be able to customize the Steam theme. I would like to see Audio Loader work sometime in the future so I can add some background music, but I'd honestly have no idea how or *if* the ChimeraOS devs would be able to work that out.

A nice feature is **GE-Proton is included out of the box with ChimeraOS**. No need to download and run ProtonUp-Qt. From what I've seen, it looks like [Boxtron](https://github.com/dreamer/boxtron) is also included for running DOS games. New versions of GE-Proton get added over time with updates to ChimeraOS.

![ChimeraOS GE-Proton in list](/images/distro_reviews/chimeraos/ge_proton_list.jpg)

[CryoUtilities](https://linuxgamingcentral.com/posts/interview-with-kyle-cryoutilities-dev/) worked for the most part as well. I couldn't use the installer script; I had to download the binary from the [Releases](https://github.com/CryoByte33/steam-deck-utilities/releases) in order to use it. I was able to change the swappiness value, enable shared memory on THP, enable compaction proactiveness, enable huge page defragmentation, and enable page lock unfairness. Only thing I was *not* able to do is change the swap size. I don't even know what the default swap size is on ChimeraOS, or if there *is* a swap file/partition.

Another utility that worked out of the box was [EmuDeck](https://www.emudeck.com/). Was able to add [*Metroid Prime Remastered*](https://linuxgamingcentral.com/posts/metroid-prime-remastered-review/) to Steam BPM, and add artwork via Steam ROM Manager without issue. For some reason Steam thinks the game is "My Pet Rock" but fortunately the [SteamGridDB plugin](https://github.com/SteamGridDB/decky-steamgriddb) came to the rescue, and I was able to add the proper artwork with this plugin.

My Mayflash adapter worked out of the box. Frigging *phenomenal*. What's even better was I was able to overclock the adapter without hassle. Just install the PKGBUILD of [gcadapter_oc_kmod](https://github.com/HannesMann/gcadapter-oc-kmod) after unlocking the file system, and I was good to go. Now I can play *Melee* with my overclocked GameCube controller online without issue. Add Slippi as a non-Steam game, have *Melee* launch on startup, and I can play online directly from Steam BPM. Fricking *gold*, man. Honestly, if that criteria passes, that's the *only* requirement that I have as to whether or not a distro has my approval. ChimeraOS certainly meets my approval.

![Melee on ChimeraOS](/images/distro_reviews/chimeraos/melee.jpg)

One caveat you should be aware of, is that **.desktop files don't seem to work**. Even after marking them as executable, double-clicking them will just open up the .desktop file in a text editor. The only way I was able to properly install Decky Loader, EmuDeck, etc. was by running the command within the `Exec` parameter in the terminal. For instance, to install EmuDeck I had to run `sh -c 'curl -L https://raw.githubusercontent.com/dragoonDorise/EmuDeck/main/install.sh | bash'`. Then, to use it, I had to run the AppImage found in `~/Applications/`.

When running a game, you'll be limited to 720p resolution. I'm assuming this is because of how Gamescope is set up. **To have higher resolutions available, you'll need to go to the game's properties in Steam and increase the resolution from there**. It's a bit of a nuisance; I would assume most desktop users are using 1080p, 1440p, or 4K resolutions, and this needs to be set on a per-game basis. To my knowledge there's no global option for this.

![ChimeraOS setting resolution in game properties](/images/distro_reviews/chimeraos/resolution.jpg)

The framerate limiter actually works from the Quick Access Menu. The framerate limit can be set to 15, 30, 60, or unlimited. Based on my testing the 60 FPS option also acts as the "Unlimited" option. The refresh rate slider isn't visible. Adjusting the TDP limit doesn't seem to do anything. When toggling the GPU clock speed limiter, the slider doesn't even become present. If a user has ChimeraOS installed on a laptop or handheld, adding these features might be a good idea for maximizing battery life time.

An interesting feature is ChimeraOS seems to have NVIDIA Image Scaling available from the QAM. Seems to work so far based on my testing. Interestingly enough this is only available on Deck if you're opted into the "Main" branch.

![ChimeraOS running Kena: Bridge of Spirits](/images/distro_reviews/chimeraos/kena.jpg)

# Chimera Web App
Formerly called Steam Buddy, the [Chimera Web App](https://github.com/ChimeraOS/chimera) allows you to add Flatpaks from Flathub, in addition to ROMs. Basically how it works is this: on another device, such as your phone, tablet, or laptop, you can access the web app, so long as said device is connected to the same network that the computer with ChimeraOS is, and the computer is on. With a web browser, you put in the local IP address of ChimeraOS in the URL, or `chimeraos.local` (the latter doesn't work for me, so YMMV). You'll then be presented with a password prompt. A password will show up on ChimeraOS. Put in this password on your phone, and now you've got some pretty neat options at your disposal.

![ChimeraOS web app](/images/distro_reviews/chimeraos/web_app.webp)

Things you can do with the web app:
- add ROMs from various consoles, upload them to the ChimeraOS machine, and then ChimeraOS will add these ROMs to Steam with the appropriate emulator
- add various Flatpaks to Steam, such as Spotify, *Minecraft*, *Super Tux Kart*, etc.
- use your phone as a remote for ChimeraOS; load or save a game, restart Steam, suspend the computer, turn it off, adjust volume, etc.
- enable or disable FTP/SSH access
- format other drives that are present on the system
- link your Epic Games account (and presumably add games from your Epic library to Steam; I haven't tested this)

You can do all of this on your phone; you don't need to connect a mouse and keyboard to the host machine to do the same thing. So, for example, if you wanted to add *Zelda: Wind Waker* to ChimeraOS, you would access the web app on your phone, locate GameCube from the emulator list, add your legal dump that's stored on your phone, add artwork, upload it to the ChimeraOS machine, then reboot Steam on said machine. *Wind Waker* should now be available on from the "Non-Steam" category in your library. Launch it and it should just work out of the box with Dolphin. Pretty convenient.

![ChimeraOS Spotify installed via web app](/images/distro_reviews/chimeraos/spotify.webp)

It's kind of difficult to explain this concept on paper, so I don't blame you if you're a little confused about this. I might have a video on this later on to explain this better.

One thing I'd like to see: add Nintendo Switch/Wii U/PS3 emulator support. Currently, you can only go up to the Wii era of games. That being said, you *can* make use of EmuDeck, as I had alluded to earlier, to add these games to your Steam library.

Another thing I'd like to see: Netflix support? It's technically possible by installing a Chrome app and adding said app as a non-Steam game, although it might not work nicely with a gamepad.

![ChimeraOS web app actions](/images/distro_reviews/chimeraos/remote.webp)

Oh, one last thing: add dark mode support. Although, I already know this is in the pipeline; I personally spoke about it with the project founder.

# ChimeraOS Playable/Verified
Similar to how the Steam Deck Playable/Verified program works, ChimeraOS has a similar service. The ChimeraOS team has their own curated program that will let you know how well a game plays with said operating system. As a quick example, *Soul Calibur VI* and *Ultra Street Fighter IV* are marked as "ChimeraOS Playable". *Gang Beasts*, *Horizon Zero Dawn*, and *Sonic Mania* are marked as "ChimeraOS Verified". Honestly, this isn't something that I've paid much attention to, but if you want to know whether the game you want to play works well or not with a gamepad, you can use this as a guiding system.

![ChimeraOS Playable/Verified games](/images/distro_reviews/chimeraos/chimeraos_playable_and_verified.webp)

# Desktop Mode
ChimeraOS [35](https://linuxgamingcentral.com/posts/chimeraos-35/) added a desktop mode. I know this was a long-standing debate with the team, as to whether they *should* add one, and if they did, *what* DE it would use. They finally added this and went with GNOME. I'm kind of curious why they went with GNOME. Likely because, outside of KDE Plasma, GNOME is one of the most popular DEs out there. But I'm glad they added a desktop. To me, this adds a lot more functionality to the OS (I wouldn't be able to install Decky Loader or use CryoUtilities otherwise). I was also able to write this review entirely on ChimeraOS because of this.

![ChimeraOS system specs](/images/distro_reviews/chimeraos/system_specs.png)

Just be aware the Desktop Mode is *incredibly* barebones. There's only one wallpaper, and a web browser isn't even included. Some suggestions I'm going to throw out to the team:
- add a few more wallpapers
- add a web browser

Just those two things I think would have made the desktop experience a little more bearable. Of course, vanilla GNOME is just...*nuts*. Like, why, *why* get rid of the minimize and maximize buttons? Why get rid of the desktop icons? Why get rid of the icons on the taskbar? Why can't I take screenshots in a format other than PNG? I was able to get a few extensions to work after unlocking the file system and installing `gnome-browser-connector` via the AUR, but of course, not all of them worked. Extensions always have a tendancy of breaking whenever there's a new update to GNOME. Of course, I'm not blaming the Chimera team for this; this is all because of the GNOME team's choices.

![ChimeraOS desktop](/images/distro_reviews/chimeraos/desktop.webp)

Though the file system is immutable by default, you can unlock it with `sudo frzr-unlock`. After unlocking the file system, you can install packages with pacman. And thank goodness, ChimeraOS does *not* butcher most of the packages from the official Arch repos. Meaning you should be able to install most Arch packages without any hassle. I know for a fact on SteamOS 3, installing packages is a *huge* pain in the arse, because there's usually this mess if you try to install one, and then when you think you found a solution, the situation only becomes *more* complicated for X, Y, and Z reasons. 

If you wanted to you could install an AUR helper, such as yay or paru, so you can easily install AUR packages. This has certainly been useful on my end, as without this I would not have been able to get GNOME extensions to work, neither would I have been able to overclock my Mayflash GameCube adapter. The one advantage SteamOS 3 has in this regard, however, is the user is able to lock the file system again by running the appropriate command in the terminal. To my knowledge, it's not possible to lock the file system again in ChimeraOS. I'd like to see this functionality in the future, so the OS is more secure.

![ChimeraOS desktop wallpaper selection](/images/distro_reviews/chimeraos/wallpaper.png)

If you have a flash drive, MicroSD card, or other hard drive installed on your system, ChimeraOS won't be able to detect them. I'm assuming the distro is missing the necessary packages/drivers needed for that. So, just be aware if you want to transfer files from different drives, you'll have to install the necessary software for that before doing so.

Any time you want to return to Game Mode, simply select the appropriate icon from the "Show Applications" button from the Dash panel. To go back to Desktop Mode, press the Guide button on your gamepad, and select the appropriate option from the menu (very similar to how the Deck works).

# Works on Deck
If you wanted to run ChimeraOS on Deck, that's totally possible. I haven't personally tested this; I would if my bloody MicroSD card wasn't stuck inside my Deck. But it seems like you can get [audio support](https://linuxgamingcentral.com/posts/audio-on-deck-support-outside-of-steamos/) after running the installer script from the acp5x-ucm-files repo. Based on Ruineka's testing (one of the ChimeraOS contributors), it looks like ChimeraOS is running great.

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/steam_deck/audio_on_deck_chimeraos.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

So, if for some reason you don't like SteamOS, ChimeraOS is a great alternative.

# A Great Couch-Gaming Distro Made Even Better
Going back to my [review from three years ago](https://boilingsteam.com/gameros-an-enhanced-version-of-steamos/), here was my "not-so-good" list:
- Not aimed for productivity use, as there’s no option to switch to a desktop, nor can multitasking be accomplished (i.e. you can’t play a game and ALT + TAB to another application)
- Strange mouse cursor issues with Flatpaks
- Controls for emulated games may be a bit off, though they can be fixed
- Bluetooth controllers have to be re-paired on every startup
- Need a wired Internet connection for installation; some folks may not have this
- The simplicity of the installer leaves little to no options in terms of configuration
- Certain shortcuts, when removed, will reappear after restarting Steam

Most of these issues have been addressed. Wi-Fi installation is now possible. Productivity use has also been added thanks to the addition of a desktop environment. I haven't had any issues reconnecting Bluetooth gamepads on each restart. Haven't had any "strange mouse cursor issues" with Flatpaks. Controls with emulated titles, at least with *Metroid Prime Remastered* and *Melee*, have been working just fine, without having to reconfigure them. Haven't tested the shortcut issue, but I would assume that has also been fixed. And the installer itself...well, it was made simple on purpose. And I hope it stays that way, so that there's no complications.

ChimeraOS even went so far as to address one of the things from my wishlist, that is, to add GE-Proton with the base system. And that they did. Both awesome and convenient.

![ChimeraOS running Sonic 3 AIR](/images/distro_reviews/chimeraos/sonic_3_air.jpg)

So, at the end of the day, my gripes are:
- installer still needs an Internet connection; would be nice to have an offline installer
- TDP limit/GPU clock speed doesn't work; this would be nice for laptop users or handhelds
- add some more functionality to the desktop; at the very least add Firefox or some other web browser, maybe add a few more wallpapers
- make it possible to actually *run* a .desktop file, without opening a text editor or having to resort to a terminal
- add Wii U/Switch/PS3 ROM support to the Chimera web app
- add a command to lock the file system once it's been unlocked
- don't make the user manually change the resolution for each game if they want to run it higher than 720p
- certain Decky Loader plugins don't work (although I'm not really blaming the Chimera team for this; this isn't SteamOS after all)
- the icons/glyphs for Steam BPM need to be updated; they shouldn't be Steam Deck-oriented (again, not necessarily blaming ChimeraOS here; I think that's more so Valve's fault)

There's far more strengths to ChimeraOS, however. It's a great -- and what, in my opinion, is the *best* -- Linux-based distribution to transform your PC into a living room console. Install it and forget about the mouse and keyboard. Just bring the computer itself, the power cable, HDMI/DisplayPort cable, and your favorite gamepad to your next LAN party. Relax from a long, stressful day by turning the computer on and doing some hardcore gaming -- again, all without needing that keyboard and mouse connected. On the other hand, if you *do* want to extend the functionality of ChimeraOS, and use it for purposes other than gaming, that's also possible thanks to the addition of a desktop. If you wanted to use something other than SteamOS on your Deck, ChimeraOS is also an option there.

I mean, I could go on and on about what I like and don't like about ChimeraOS, but this review is long enough. Just [download](https://chimeraos.org/download) it already and install it on a spare hard drive if installing on a computer, or a MicroSD card if you're on Deck. **Thank you, alkazar, Ruineka, Samsagax, pastaq, and the several other developers involved with this project.** You're fixing the things Valve is too lazy to do themselves, and making couch-gaming that much more of a pleasant experience.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
