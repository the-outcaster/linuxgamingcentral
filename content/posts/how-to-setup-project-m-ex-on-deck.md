+++
title = "How to Set Up Project M EX Remix on Steam Deck"
date = 2023-04-17T03:14:48Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/pmex_remix/cover.jpg"
tags = ["steam deck", "guide", "smash bros"]
keywords = ["project m ex remix", "pmex", "project m ex", "project m", "project m on steam deck", "project m ex remix on steam deck", "super smash bros brawl mod"]
description = "The most ambitious mod for Super Smash Bros. Brawl, right in the palm of your hand."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
# What Is Project M EX Remix?
Remember [Project M](https://pmunofficial.com/en/) back in the day, which eventually turned into [Project+](https://projectplusgame.com/)? The mod that turns *Super Smash Bros. Brawl* into a more competitive game? Well, Project M EX Remix (or PMEX Remix for short) keeps all those changes, while *massively* increasing the character roster, stages, music selection, and a whole lot more. Want to play as Shadow the Hedgehog? Zack Fair? Waluigi? They're all here, thanks to the modding community. 

PMEX Remix is probably the most ambitious modding project for *Super Smash Bros. Brawl*. It takes mods from the community and puts it into one nice collection. As a result, the roster size is even larger than *Smash Ultimate*. I'm not kidding you -- there's over 120 characters to choose from. It's also possible to play online thanks to Dolphin's netplay feature. There's even a "Codes" menu in which you can customize the game's modifiers, such as knockback strength, whether the HUD is visible, etc.

![PM EX Remix character roster](/images/steam_deck/guides/pmex_remix/css.webp)

# How to Get PMEX Remix to Work on Steam Deck
When you download PMEX Remix, you'll only get the Windows version of Dolphin. While we could technically get it to work on Deck with the use of Wine/Proton, there's two issues:
1. You won't be able to use your GameCube controller adapter.
2. Wine will add more CPU overhead than running Dolphin natively, which we don't want, as it can lead to performance issues and increased battery usage.

But fret not, it's fairly easy to get a native version of PMEX Remix running nicely on Deck/Linux desktop. Here's how to do it.

I assume you have a legal copy of *Super Smash Bros. Brawl* dumped from your Wii and stored somewhere on your Deck. If not, head over to the [Dolphin Wiki](https://wiki.dolphin-emu.org/index.php?title=Ripping_Games) for instructions on how to dump your disc. I do *NOT* condone piracy of the game!

![SSBB physical disc](/images/steam_deck/guides/pmex_remix/physical_disc.jpg)

#### Get the Necessary Downloads

Go to Desktop Mode. Head over to [Brawl Vault](https://forums.kc-mm.com/Gallery/BrawlView.php?Number=217920) to download PMEX Remix. The latest version as of the time of writing this is **0.95DX** (with a hotfix that was just uploaded yesterday). You'll be taken to a Google Drive link. **Download the Dolphin build**.

Extract the archive. Pay attention to the following files/folders, as we will need them:
- the `Launcher` folder and its contents
- the `RSBE01` folder and its contents inside of `User/Load/Textures/`
- the `sd.raw` file in `User/Wii/`

Next, download the [latest AppImage of Project+](https://github.com/jlambert360/FPM-AppImage/releases). After it's downloaded, right-click the AppImage in your file manager -> Properties -> Permissions -> Check the box for "Is executable". Close the Properties window, right-click the AppImage again, and add it to Steam with "Add to Steam". This way, we can launch PMEX Remix from Game Mode later on.

![Project+ marked as executable](/images/steam_deck/guides/pmex_remix/file_permissions.png)

#### Configure Project+

Open Project+. Click "Config" and go to the "Paths" tab in the window that pops up. Under ISO Directories, click "Add..." Locate the `Launcher` folder from the PMEX Remix Dolphin build that you had downloaded. Click "Open". This directory should now show up under ISO Directories. Check the box for "Search Subfolders" so that Dolphin can pick up both the netplay launcher and the offline launcher.

Next, click the three-dotted button next to "Default ISO" and locate your copy of *Super Smash Bros. Brawl*. In my case I have it stored in `~/Emulation/roms/wii/`. (Note: "~" is short for `/home/deck/`.)

Click the three-dotted button next to "SD Card Path" and locate the `sd.raw` file from the PMEX Remix Dolphin build that you had downloaded.

![Project+ paths](/images/steam_deck/guides/pmex_remix/paths.png)

Now we can configure the graphics. Click "Graphics" from the arrow in the main window in Dolphin. Here you can set the aspect ratio to your liking; by default it's set to 69:40. I'll go with 16:10. If you're playing the game while docked, adjust the aspect ratio to what your monitor's is. Check the box for "Use Fullscreen".

You may want to uncheck "Show FPS" and "Show OSD Clock" if you're using Steam's performance overlay, so there's less clutter on the screen.

![Project+ General graphics](/images/steam_deck/guides/pmex_remix/general_graphics.png)

Next, go to the first "Enhancements" tab. Adjust the internal resolution. You shouldn't need to set the resolution any higher than 720p, unless you're planning on docking your Deck to an external monitor.

![Project+ internal resolution](/images/steam_deck/guides/pmex_remix/internal_resolution.png)

Go to the "Advanced" tab. Check the box for "Load Custom Textures" but do NOT check "Prefetch Custom Textures"; the emulator will crash as soon as the game is loaded.

![Project+ enable custom texture loading](/images/steam_deck/guides/pmex_remix/load_custom_textures.png)

Now we can set our controls. Click the arrow on the right-side of the main window in Dolphin, and click "Controllers". If you're docking your Deck and you have your GameCube controller adapter connected, you can leave Port 1 to the default "GameCube Adapter for Wii U". Note that, even though you can *technically* [overclock the adapter](https://linuxgamingcentral.com/posts/overclocking-gc-adapter-guide/) on Steam Deck, please be aware that **you do so at your own risk**. I haven't been able to figure it out myself, but you can follow the instructions [here](https://github.com/hannesmann/gcadapter-oc-kmod/blob/master/STEAMOS.md) if you want to give it a shot.

Otherwise, if you're planning on using the Deck's integrated controls, click the dropdown menu for Port 1 and select "Standard Controller". Click "Configure". Under Device, click the dropdown menu and select "Microsoft X-Box 360 pad 0". Close the window; we'll configure our controls in Game Mode.

Now we copy the HD textures over. Copy the `RSBE01` folder from the PMEX Remix Dolphin build and put it in `~/.local/share/FasterPPlus/Load/Textures/`.

#### Configure Controls in Game Mode

Return to Game Mode. Project+ should be available under the "Non-Steam" category. Launch it. At this point you'll need to access the controller configuration window with the touchscreen. Tap "Controllers" and "Configure" port 1 if you're using the Deck's integrated controls. Now you can set up the controls to your liking. Tap "Close" when finished. (If you can't close the window for some reason, just hold the Steam button and press left on the D-pad to close it.)

![Project+ Deck controls](/images/steam_deck/guides/pmex_remix/deck_controls.png)

#### Good to Go!

After controls have been set, launch the offline version of PMEX Remix. Ensure the game runs and the controls, graphics, etc. are to your liking. Any time you want to exit the game and return to Dolphin, just hold Steam + left on the D-pad. You can also return to Steam like you would with any other game by pressing the Steam button and selecting the appropriate action from the context menu.

![PM EX Remix running on Deck](/images/steam_deck/guides/pmex_remix/running_on_deck.jpg)

# Optional Steps
#### Get Artwork

We can give custom artwork to PMEX Remix in our Steam library. This is thanks to the [SteamGridDB plugin](https://linuxgamingcentral.com/posts/steamgriddb/). Install [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader) if you don't have it already. From there you can access the plugin store in Game Mode and install SteamGridDB.

![PM EX Remix artwork from SteamGridDB](/images/steam_deck/guides/pmex_remix/steamgriddb.jpeg)

Select Project+ from your Steam library. Press Start and select "Change Artwork..." from the context menu. Search for "pmex" in the search filter. You should be able to see "Super Smash Bros PM EX Remix" from the list and select it. Now you can get PMEX Remix-themed artwork for the capsule, hero, logo, etc! You're not going to regret it; it's going to give your Steam library a fresh coat of paint.

![PM EX Remix artwork on Steam](/images/steam_deck/guides/pmex_remix/custom_artwork.jpeg)

#### Run PMEX Remix Immediately

There's no checkbox for starting up the default ISO when Dolphin is launched. Meaning that every time we want to launch the game, we have to use the touchscreen with Dolphin to launch the appropriate file. This can be a bit clunky in Game Mode, since we don't have access to a mouse and keyboard. However, we can add a custom parameter to Steam so that it immediately launches the offline version of PMEX Remix when Project+ is started up.

![PMEX Remix launch options](/images/steam_deck/guides/pmex_remix/launch_options.png)

In Desktop Mode, right-click Project+ from your Steam library and to go the Properties menu. Under "Launch Options" set the path to the offline .elf file. So it might look something like this:

`PMEX\ REMIX\ 0.95DX\ \[DOLPHIN\]/Launcher/P+EX\ REMIX\ OFFLINE/Project_Offline_Launcher.elf`

Test these settings by running the emulator through Steam and verifying that it immediately launches PMEX Remix.

#### Optimal Performance Settings

I recommend setting the TDP limit to around 5 W and a GPU clock speed of 600 MHz. I haven't tested how long the battery lasts with these settings, but this should give you a longer-lasting battery. You can technically lower these values and still get 60 FPS in most cases, but there will be some stuttering here and there depending on what's going on on-screen and the number of characters there are, so 5 W and 600 MHz is a more generous value. You can install [PowerTools](https://linuxgamingcentral.com/posts/preserve-battery-life-on-deck-with-powertools/) and further fine-tune the Deck's hardware for more optimal battery life.

![PM EX Remix power settings](/images/steam_deck/guides/pmex_remix/power_settings.jpeg)

# Need Help?
Join my [Discord](https://discord.gg/bTgCcWC4dm) and go to the #support channel. I'll see if I can help you out. Otherwise, you might be able to ask for help in the [PM EX Remix Discord](https://t.co/y0YxrUU2Rt).

Also, let me know if you guys want a video guide in addition to this.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
