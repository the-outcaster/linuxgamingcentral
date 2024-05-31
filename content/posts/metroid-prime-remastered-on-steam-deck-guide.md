+++
title = "Metroid Prime Remastered: Getting it to Work Nicely on Deck"
date = 2022-09-28T12:18:24-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/mpr.jpg"
tags = ["steam deck", "metroid", "emulation", "guide"]
keywords = ["metroid prime", "steam deck", "metroid prime remastered", "dolphin", "emulation", "wine", "bottles"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*EDIT (2/12/2023): this is for the UNOFFICIAL remaster. Not the official.*

If you're like me, you were probably left with a bad taste in your mouth after this year's [Nintendo Direct](https://www.youtube.com/watch?v=UJ9Iz7HhU-I). No *Metroid* announcements whatsoever. There were [rumors of an official remaster of *Metroid Prime* coming this year](https://ftw.usatoday.com/2022/06/metroid-prime-remaster-coming-this-year). It would have made sense considering this year marks the 20th anniversary of the beloved title. But, of course, our expectations got crushed.

Well, if Nintendo ain't gonna do it, leave it up to the fans. Hence we have an [unofficial remaster](https://linuxgamingcentral.com/posts/mpr/) that would knock any official one out of the water. Plus, we have the addition of keyboard and mouse controls, as well as support for resolutions much larger than what the Switch can handle. Long story short, we probably won't ever see a Linux release of this Dolphin fork anytime soon -- due to complications in porting the archaic Ishiiruka code into something that Linux can understand, according to one of the developers -- but fortunately for us, we've got compatibility layers like Wine and Bottles to do the work for us.

Getting MPR to work on the Deck was a *very* tedious process. Nonetheless, by following this guide, hopefully you won't have to go through the headache that I did. So let's get started.

*NOTE: I made this guide with the GameCube version of Prime in mind. The Trilogy may be a little different as far as controls go.*

# Get MPR
Download the latest release of MPR from [GitHub](https://github.com/AetherPrimus/MPR/releases) on your Deck in Desktop Mode. Extract the zip file to your `Documents` or your `Downloads` folder. The reason why it needs to be in a particular folder like these is because of the way Flatpaks work; they can only access certain folders. You can use something like [Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal) to manage Flatpak permissions and have Bottles -- the tool we're going to need next -- have access to different folders.

Take your legally-acquired ISO of *Prime* (it can either be v1.0 of the GameCube version or any version of the *Trilogy*) and copy it over to your Deck if you haven't already. I have mine in `/home/deck/Emulation/roms/gamecube/`.

# Install and Configure Bottles
Bottles is an application similar to Lutris. It creates individual containers called "bottles" and gives us all the dependencies we could possibly need for an application. Search for "Bottles" on the Discover app, or install it via the command line with:

`flatpak install flathub com.usebottles.bottles`

Bottles should now be available under "Utilities" on the Start menu. Open it up. Let's create a new bottle by clicking the "+" icon on the top-right. Give the bottle a name. Leave the environment on "Gaming".

![Bottles creating a new bottle](/images/mpr_on_deck/setting_up_bottle.png)

Click "Create". If everything went well you should have the bottle listed under the "Bottles" tab on the main window. Click the bottle and go to the "Programs" tab. Click the "+" icon on the right on the window border, then locate the `MPR.exe` file from the folder you had extracted earlier. "MPR" should now be listed under the "Programs" section.

![Bottles MPR added](/images/mpr_on_deck/program_added.png)

You can optionally add MPR to your Bottles library by clicking the three-dotted button on the program and selecting the appropriate option from the dropdown menu. Unfortunately I haven't had any luck adding the game as a non-Steam shortcut. But you're going to want to **add Bottles itself as a non-Steam game**, because we're going to need to launch Bottles through Game Mode later on to configure the Deck's controls.

# Configure MPR
Click the Play icon and the emulator should now open up. No, the interface isn't that great, but that's one of the caveats that come from Wine. Whatever you do, don't click the "MPR" button; the emulator will hang.

![MPR main window](/images/mpr_on_deck/roms_added.png)

Click the "Config" button and go to the "Paths" tab. Add the folder containing your ISO. You may also want to uncheck the box for "Confirm on Stop" in the "Interface" tab so you don't get a confirmation box before quitting the game.

![MPR adding ISO directory](/images/mpr_on_deck/game_directory.png)

Close the configuration window, then click "Graphics". **Make sure the backend is set to either Vulkan or OpenGL** in the "General" tab; this step is important as the default D3D11 version will cause the emulator to crash every time you try to run the game. D3D12 will make the emulator hang. The one caveat with Vulkan/OpenGL is there is no forced lighting. The game won't look as good without it, but still looks better than the original.

Set the aspect ratio to 16:10 to get rid of the ugly bars that will show up otherwise while playing. Then check the box for "Use Fullscreen".

![MPR using Vulkan](/images/mpr_on_deck/vulkan_enabled.png)

Under the first "Enhancements" tab, set the interal resolution to 720p; no point upscaling to 1080p as obviously the Deck doesn't support that high of a resolution (unless you connect it to an external monitor). You can optionally check the box for "Widescreen Hack".

![MPR using 720p with widescreen](/images/mpr_on_deck/720p_and_widescreen.png)

Under the "PrimeHack GFX" tab, you can optionally enable bloom; this will increase the graphics quality, but it's obviously going to consume more power.

![MPR enabling bloom](/images/mpr_on_deck/bloom_enabled.png)

Don't run the game just yet. We have to configure the Deck's controls. For which we will have to go to Game Mode.

# Configure Controls
Go to Game Mode. Launch Bottles. Run MPR. Tap "Controllers" from the main window. Configure Port 1. In the new window that pops up, set the device to "Steam Virtual Gamepad" if it isn't already. Now configure your controls. Don't forget to configure the camera controls under the "PrimeHack" tab as well.

![MPR configuring controls](/images/mpr_on_deck/deck_controls.png)

One thing you have to keep in mind is you can't assign L to the left trigger and A to the right. In-game, if you lock on to an enemy with the left trigger, then try to shoot with the right, the lock-on will just cancel, and Samus won't shoot either. It's weird and hard to explain. So you may be better off just assigning L to the left shoulder button instead. Then you can still shoot with the right trigger.

Alternatively, if you don't want to go through that hassle, I've provided a copy of my Deck configuration. You can [download](/mpr_deck_controller_config/deck.ini) and copy the file over to (get ready, this is a *long* file path):

`/home/deck/.var/app/com.usebottles.bottles/data/bottles/bottles/MPR__195/drive_c/users/deck/Documents/Dolphin Emulator/Config/Profiles/GCPad/`

Then select "deck" under the Profile dropdown menu on the controller configuration screen and tap "Load". Only thing I don't have configured is the C-Stick.

In Game Mode, you may want to make use of the gyro with the right trackpad/right thumbstick touch with Steam Input for more accurate camera controls.

# Run the Game
Tap on your *Prime* ISO and tap "Play". You should be good to go!

![MPR running on Deck](/images/mpr_on_deck/720p_without_widescreen.jpg)

Note that if you leave the game and try to run it again, MPR will likely complain of missing files. The HD textures won't load as a result. Just restart the emulator and you should no longer have that problem. (You can exit the game at any time by holding down the Steam button and pressing left on the D-pad.)

A lot of work...but it's all worth it for the HD textures, right??

Here's some [footage](https://youtu.be/6m3N-VqM6ac) if you want to see the game in-action!

**TL;DR**
1. Copy your legally-acquired ISO to your Deck. Download and extract [MPR](https://github.com/AetherPrimus/MPR/releases) to `Documents` or `Downloads` (configure Bottles permissions with Flatseal if needed)
2. Download and install [Bottles](https://flathub.org/apps/details/com.usebottles.bottles). Add Bottles as a non-Steam game
3. Create a new gaming bottle
4. Add `MPR.exe` as a program for the bottle
5. Open MPR via Bottles, add your ISO path, set graphics backend to Vulkan/OpenGL, set aspect ratio to 16:10, use fullscreen, set internal resolution to 720p, optionally enable bloom/widescreen
6. Go to Game Mode, open Bottles, run MPR, configure Deck controls
7. Go play

Someone's probably going to need some help on the way. You can comment here or join the [MPR Discord](https://discord.gg/XekpGVBH5m) if you have questions.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
