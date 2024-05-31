+++
title = "Enhance Your Sonic Frontiers Experience with Mods"
date = 2022-11-16T14:24:07-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/guides/sonic_frontiers_modding/cover.jpg"
tags = ["guide", "sonic", "modding", "steam deck", "steamtinkerlaunch", "hedge mod manager"]
keywords = ["sonic frontiers", "modding", "linux", "steam deck", "steamtinkerlaunch", "hedge mod manager"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**UPDATE (12/27/2022): updated [Steam Deck guide](https://linuxgamingcentral.com/posts/updated-sonic-frontiers-steam-deck-modding-guide/) is available!**

**UPDATE (12/5/2022): [video guide](https://www.youtube.com/watch?v=FJs1FADQI08) is up if you need it!**

*Sonic Frontiers* may have an "Overwhelmingly Positive" rating on [Steam](https://store.steampowered.com/app/1237320/Sonic_Frontiers/), but there are quite a few things we can do to make the gameplay experience even better. Such as:
- disable letterboxing during cutscenes
- unlocking framerate during cutscenes
- 4K video playback
- skipping intro video
- decreasing graphics quality for getting smoother gameplay on NVIDIA (or other low-end hardware including the [Steam Deck](https://linuxgamingcentral.com/posts/sonic-frontiers-on-deck-best-settings/))
- making speed upgrades faster
- reducing hitstop for more fluent gameplay
- improved physics for Cyber Space levels
- removing the cutscene when unlocking a portion of the map
- increased difficulty
- changing how Sonic looks
- and *plenty* of other enhancements

With all these mods you could practically get a fresh new session in after beating the game. So let's go over how to get mods running. This guide will cover both Linux desktop as well as the Steam Deck.

As always, small disclaimer that I'm not responsible if the Denuvo DRM triggers while you're doing this. So far I haven't had any issues, but I needed to throw that out there.

![Silver mod for Sonic Frontiers](/images/guides/sonic_frontiers_modding/silver_mod.jpg)

# 1. Get SteamTinkerLaunch
To mod *Sonic Frontiers* on Linux, we'll need to use [Hedge Mod Manager](https://github.com/thesupersonic16/HedgeModManager) (HMM). This tool allows us to mod any game that uses the Hedgehog Engine, which is what *Sonic Frontiers* uses. Because it's only available on Windows, we have to use Wine to run it. [SteamTinkerLaunch](https://github.com/sonic2kk/steamtinkerlaunch) (STL) makes this easy for us. If you're not aware of STL, it's basically the Swiss army knife when it comes to managing Windows-based games on Linux. See the article from [Boiling Steam](https://boilingsteam.com/supercharge-steam-with-steamtinkerlaunch-stl/) for more info.

Note that we'll need to compile the latest git version of STL in order to use HMM. The latest 11.11 release won't support this. If you're on Arch, you can install [steamtinkerlaunch-git](https://aur.archlinux.org/packages/steamtinkerlaunch-git). On Ubuntu-based distros, you can use [Pacstall](https://github.com/pacstall/pacstall). This is basically the AUR-equivalent for Ubuntu-based distros. After that's installed, you can install with:

`pacstall -I steamtinkerlaunch-git`

On Steam Deck, download the latest commit from the [main GitHub page](https://github.com/sonic2kk/steamtinkerlaunch), clicking the green "Code" button, then selecting "Download ZIP". Extract the zip file somewhere convenient. Open a terminal in the same location where the STL executable is located.

Run this to add STL as a compatibility tool in Steam (this step is optional; useful if you want to use STL for games outside of *Sonic Frontiers*):

`steamtinkerlaunch compat add` (or `./steamtinkerlaunch compat add` if you're on Deck)

![STL with Sonic Frontiers](/images/guides/sonic_frontiers_modding/stl.png)

# 2. Install Winetricks and Ensure It's Up-to-Date (on Desktop)
If you're on desktop, make sure [Winetricks](https://github.com/Winetricks/winetricks) is installed. Installing this is dependent on the distro you're using. Note that STL may have installed this for you already. Check your Winetricks version with:

`winetricks --version`

In order to use HMM with STL, your version will need to be **20220411-next** or higher.

![Checking winetricks version](/images/guides/sonic_frontiers_modding/checking_winetricks_version.png)

If you don't have this version, update to the latest one with:

`sudo winetricks --self-update`

Note that if you're on Deck, this step isn't necessary; STL downloads and installs Winetricks for any app that needs it.

# 3. Run Hedge Mod Manager
Once STL is installed and you have the latest version of Winetricks installed, you can download and run HMM with:

`steamtinkerlaunch hmm start nightly` (or `./steamtinkerlaunch hmm start nightly` if you're on Deck)

You will need to use the nightly release; the latest stable release at the time of writing this does *not* support *Sonic Frontiers*. This will take quite a while; up to 10 minutes when run for the first time.

If everything went well HMM should open up:

![HMM About Menu](/images/guides/sonic_frontiers_modding/hmm_about.png)

Here's some codes that I would recommend enabling:
- disable framerate limiter on cutscenes
- disable guardian interactions
- disable in-game letterboxing
- disable power boost cutscene
- disable shadows (for NVIDIA or low-powered hardware)
- fix resolution resetting on launch
- hide skip button in cutscenes

I'm noticing that just about every day there's a new code that gets added -- you may see a button that says, "Update Community Codes". Click this to get more codes. After you're done checking off codes, click "Save" to save your changes.

![HMM Codes Menu](/images/guides/sonic_frontiers_modding/hmm_codes.png)

# 4. Get Mods
For mods, we'll have to download them. You can find most of these over on [GameBanana](https://gamebanana.com/mods/games/15779). Supposedly the one-click install button works for the maintainer of STL, but it doesn't work in my case. So pick a mod, and manually download it. Some mods I'd recommend:
- [Colourful Frontiers](https://gamebanana.com/mods/412349) -- re-textures the button and skill tree icons to a more vibrant color. Note that this mod needs to get installed manually by copying over the file to the game's install directory. Instructions are provided on the mod page
- [Showin's Momentum Tweaks](https://gamebanana.com/mods/411485) -- "alters Sonic's physics to be much more momentum-based."
- [Impossible Difficulty](https://gamebanana.com/mods/412035) -- as the mod title says, this is useful if you want a challenge. Decreased damage output, decreased parry window, faster drain boost, buffed enemies, etc.
- [Buffed Titan Fights](https://gamebanana.com/mods/412169)
- [No Curscene After Challenges](https://gamebanana.com/mods/411700) -- removes the cutscene that's played every time you finish a challenge. Speeds up gameplay quite nicely
- [Potato Low End Foliage](https://gamebanana.com/mods/411534) -- backports the foliage from the Switch version, making gameplay more smooth on low-end PCs
- [Improved Physics](https://gamebanana.com/mods/411223) -- "tweaks both cyberspace and open-zone physics to have momentum and overall a better flow to gameplay."
- [Elder Koco Fixed](https://gamebanana.com/mods/411443) -- this makes upgrading Sonic's speed a much faster process
- [Halved & No Hitstop](https://gamebanana.com/mods/411402) -- "make the combat feel more flowing and a bit less sluggish, as well as make the homing attack chains feel more responsive."

Of course, should you want to change Sonic's model, you can do that as well, from [Silver](https://gamebanana.com/mods/411281) to [Minecraft Sonic](https://gamebanana.com/mods/411650) to [Amy](https://gamebanana.com/mods/411864) to [Blaze](https://gamebanana.com/mods/411309) to [Excalibur](https://gamebanana.com/mods/411887) and everything in-between. You may even want to try out a [low-poly model](https://gamebanana.com/mods/411922) if it helps at all with your framerate.

After mods have been downloaded, extract them to a convenient location. With HMM still open, go to the Mods tab. Click "Add Mod". Select "Installing from a folder" and click OK.

![HMM install from a folder](/images/guides/sonic_frontiers_modding/install_from_a_folder.jpg)

Wine's file manager will open. Select "/" to select your Linux drive. In my case I have mods placed in:

`Z:~\Desktop\frontiers_mods\`

Select "Open". The mods list should now be populated in HMM. There should also be a `Mods` folder inside of the game's install directory with all the mods you just added.

![HMM install from a folder](/images/guides/sonic_frontiers_modding/hmm_mods.png)

Check whatever mods you want to enable. Some mods may have a cog icon that isn't greyed out. If you click this, you can customize the settings for that mod. You can see here I can customize the settings for the titan boss fights and choose whether I want them buffed or normal.

![HMM install from a folder](/images/guides/sonic_frontiers_modding/buffed_titans_settings.png)

Once you're done checking off your mods, click "Save".

# 5. See Your Mods in Action
If you want, you can click "Save and Play" to launch *Sonic Frontiers* with the mods/codes enabled. But you can also just launch *Sonic Frontiers* directly from Steam and it should also pick these up.

![Werehog mod for Sonic Frontiers](/images/guides/sonic_frontiers_modding/werehog.jpg)

Oh, and here's a little bonus. If you want to skip the intro video whenever you start up the game, you can either delete or rename `sonicteam_logo.usm` and `sonicteam_logo_4k.usm`. These files are found in `/image/x64/raw/movie/` in the game's install directory.

# 6. (Optional) Make a Desktop Icon for HMM for Quick Access -- Desktop Only
If you'd rather not run `steamtinkerlaunch hmm start nightly` in the terminal every time you want to open up HMM, you can add a desktop shortcut. Open a text editor and paste this in:

```
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Type=Application
Terminal=false
Exec=steamtinkerlaunch hmm start nightly
Name=Hedge Mod Manager
Icon=/path/to/icon
```

You can use something like [this](https://clipground.com/images/sonic-icon-png-4.png) as the icon. Save it somewhere on your hard drive. Then point `Icon` to the file path of this picture. Save the text file to your desktop and make sure to give it a `.desktop` extension. On Pop!_OS, you'll need to right-click the desktop file and select "Allow Launching" to make it an executable. On other distros, this step will probably differ. You'll probably need to mark it as executable in the file properties menu.

Video coming soon?

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
