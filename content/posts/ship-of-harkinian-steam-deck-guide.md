+++
title = "Ship of Harkinian: Steam Deck Guide"
date = 2023-12-12T18:07:11Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/impressions/soh.jpg"
tags = ["guide", "steam deck", "zelda", "ship of harkinian"]
keywords = ["ship of harkinian", "ship of harkinian on steam deck", "zelda oot on steam deck", "zelda oot", "zelda ocarina of time", "steam deck"]
description = "Zelda: Ocarina of Time, 60 FPS on Steam Deck? Count me in!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**This guide has been updated on 1/19/2024 to add a video tutorial, as well as a one-line trick to extract the ROM from the TGC file. No need to set up Bottles!**

*Zelda: Ocarina of Time*. A true 90s classic. Now running natively on PC! More specifically, on Linux and Steam Deck! This reverse-engineered project is called [Ship of Harkinian](https://www.shipofharkinian.com/) (SoH).

{{< youtube gkmk0K0veKI >}}

So the question arises: why play *OoT* on native hardware as opposed to using emulation? There's quite a number of reasons, and here are some:
- go beyond the 20 FPS that the original game provided, with support for framerates that are as high as your monitor's refresh rate, giving you a buttery-smooth gameplay experience
- support for higher resolutions
- adjustable difficulty options, including how much damage you take or enemies that move at a faster pace
- quality-of-life improvements, such as faster text scrolling through long dialogues, faster walking speed, and not having to sit through Link playing a song on his ocarina. You no longer need to wait five minutes for King Zora to slide across his throne!
- a plethora of enhancements, from the color of Link's tunic, gyroscopic aiming when using the slingshot/bow, and a camera that allows you to move it around freely like any modern 3D game
- built-in randomizer, shuffling the in-game items and enemies, giving you a fresh gameplay experience
- mod support, including the changing of Link's model, the model of his sword, and the support of textures from the 3DS remake

If, on the other hand, you want as authentic of the N64 experience as possible, SoH gives you those options too. You can run the game at 20 FPS, decrease the resolution to make the graphics more pixelated, and whatever else you want to do to closely resemble 90s hardware.

Here's how to get SoH running on Steam Deck.

# Requirements
In addition to a softmodded Wii or Wii U, you will need a legal copy of the European/Australian version of *Zelda: Collector's Edition* for the GameCube. You can also use a PAL N64 cartridge, but dumping that will be outside the scope of this tutorial. The reason why you need the PAL version, according to the [SoH FAQ](https://www.shipofharkinian.com/faq), is as follows:
> The decomp started on the debug version because debug statements helped in identifying functionality during the decomp process. The only debug version available was PAL. In adding support for other versions to SoH, other PAL versions were much easier because the underlying functionality (especially with language) was the same. NTSC will take a bit more to get working the first time because of that and other differences, but afterward should be easier to add support for multiple NTSC versions.

If you don't happen to have a copy on hand, well, good luck trying to buy one at eBay without breaking the bank. Needless to say: **I do NOT condone piracy of the disc!**

![Ebay prices for Zelda: Collector's Edition PAL](/images/steam_deck_oled/guides/soh/ebay_prices.jpg)

A keyboard and mouse connected to your Deck via a USB-C dock would also help.

# Dumping the ROM and Extracting the TGC File
Dumping this game is going to be a bit of a process. You can't just dump it from your Wii or Wii U and call it a day. It's going to require using the Dolphin emulator to extract a specific file from the ISO.

Using your softmodded Wii, insert the disc into the disc drive. Follow the instructions over on [Wii Guide](https://wii.guide/dump-games.html) to dump your disc. An easy way to dump your disc is by using [CleanRip](https://oscwii.org/library/app/cleanrip) via the Homebrew channel.

Transfer the ISO to your Steam Deck. In my case I put it in `~/Emulation/roms/gamecube/`. On your Steam Deck, go to Desktop Mode. If you don't already have the Dolphin emulator installed, install it with [EmuDeck](https://www.emudeck.com/), or install it via the terminal with:

`flatpak install flathub org.DolphinEmu.dolphin-emu`

Open Dolphin under the "Games" category on the Start menu. Set your ROM filepath if you haven't already. Right-click *Zelda: Collector's Edition* from the ROM list, and go to Properties. Go to the "Filesystem" tab all the way on the right. Expand the category for "tgc" in the file browser. Right-click `zelda_PAL_093003.tgc` and select "Extract file..."

![Extracting the TGC file in Dolphin](/images/steam_deck_oled/guides/soh/extracting_tgc_file.png)

Extract the TGC file anywhere.

# Extract the ROM out of the TGC File
Previously I thought users had to use a hex editor -- in this case a hex editor that's only available on Windows. Turns out we actually don't need to go through that hassle. Just open up a terminal where your TGC file is located, and run this:

`dd bs=1 skip=476487616 count=32M if=zelda_PAL_093003.tgc of=zelda_oot.z64`

Give it about five minutes. There should now be a `zelda_oot.z64` ROM file that should be around 33-34 MB in size. Done!

Thanks to lukasm1293 from [YouTube](https://www.youtube.com/watch?v=VotwSz3aXf8) for the help!

# (Optional) Validate Dumped ROM
To verify the extracted file, head over to the [SoH Compatibility Checker](https://ship.equipment/). Click "Load a ROM" and select the .z64 file you just saved. If the verification process worked then the page should tell you what version of the game you dumped.

![SoH compatibility checker](/images/steam_deck_oled/guides/soh/soh_compatibility_checker.png)

# Get SoH
Use my [script](https://github.com/linuxgamingcentral/ship-of-harkinian-updater) to easily download and update SoH on Deck.

If you would rather download it manually, go to the [Releases](https://github.com/HarbourMasters/Shipwright/releases) section of their GitHub page. Under the "Assets" category, there are two different AppImages to choose from: Compatibility, and Performance. For this guide, we'll be going with the Performance build. Download the zip file and extract it. There should now be a `soh.appimage` file.

Right-click the AppImage, go to Properties, and under the "Permissions" tab, check "Is executable", then click "OK".

![Marking SoH appimage as executable](/images/steam_deck_oled/guides/soh/marking_appimage_as_executable.png)

If everything went well, and your .z64 file is in the same directory as the AppImage, SoH should extract some files, then run the game!

![SoH running for the first time](/images/steam_deck_oled/guides/soh/game_running.png)

Great! You can now close the game. Right-click the AppImage again, and select "Add to Steam" to add it as a non-Steam shortcut.

# (Optional) Get Artwork
Let's get rid of that ugly gray icon for SoH in Game Mode. Get the [SteamGridDB](https://linuxgamingcentral.com/posts/steamgriddb/) plugin with Decky Loader. Go to the non-Steam shortcut, press Start, and select Properties...

Change the name of "soh.appimage" to "Ship of Harkinian". 

![Changing appimage name](/images/steam_deck_oled/guides/soh/game_mode/change_file_name.jpg)

Close out of the Properties window. With SoH selected in your library, press Start again, and select "Change Artwork..."

Add some artwork to the game. So now you can go from something boring:

![SoH no artwork](/images/steam_deck_oled/guides/soh/game_mode/soh_without_artwork.jpg)

To something a little more interesting:

![SoH with artwork](/images/steam_deck_oled/guides/soh/game_mode/soh_with_artwork.jpg)

# Run SoH in Game Mode
Some things I'd recommend doing while running SoH in Game Mode, as far as controls:
- enable the back grip buttons. Set one of them to F1 so you can access the menu, and another to F11 so you can enter/exit fullscreen mode
- enable gyro and set it as joystick (SoH doesn't seem to pick up the gyro as mouse at the moment)
- set the right trackpad as mouse, with right trackpad click set as left mouse click
- set the left trackpad as a scroll wheel, so you can scroll through the various menus that SoH provides
- enable free camera in Settings -> Controller -> Additional Controller Options. Note that you will need to re-configure the C buttons and set them to a button instead of right-stick tilt, and assign right-stick to, well, right-stick

For some battery savings, you can set the TDP limit and GPU clock frequency all the way down to 3 W and 200 MHz respectively. Even at 60 FPS it still runs great. You can fine-tune the battery even further with PowerTools by setting the CPU frequency at 1000 MHz, disabling SMT, and downclocking the memory.

![SoH TDP limit set to 3 W](/images/steam_deck_oled/guides/soh/game_mode/tdp.jpg)

After that, here are some in-game recommendations:
- set MSAA to 8 and match the FPS to the refresh rate of the screen via the Settings -> Graphics tab
- optionally check off "Disable idle camera re-centering" to prevent the camera from going behind Link whenever he faces the camera
- set the preset to "Enhanced" under the Enhancements tab for QoL improvements, such as faster block pushing and item pickup messages being skipped
- set some difficulty options, such as increased damage taken and/or hyper enemies, for a more challenging experience
- mute low HP alarm, use the minimal UI, disable Navi call audio (finally, no more "Hey! What's up! Listen!")
- disable LOD to use high-poly models at a distance
- disable draw distance
- disable the music that plays when an enemy is close
- enable walk speed modifiers in Settings -> Controller -> Additional Controller Options -> Miscellaneous Controls. Set the first modifier to 200% for faster walking. Check the box to toggle the modifier instead of holding, and check "Don't affect jump distance/velocity". Now under Port 1 set the first modifier to any of the available buttons on the Deck (I used Select)

# (Optional) Further Enhance the Experience with Mods
There are a couple of mods over on [GameBanana](https://gamebanana.com/mods/games/16121?). Mods will allow you to change Link's model (want to play as [Pomni](https://gamebanana.com/mods/476530)? That's here), upgrade the textures to what the 3DS remake uses, adjust the HUD to use different icons, and other things. Here are some mods that I recommend:
- [Djipsi's 3DS Experience](https://gamebanana.com/mods/477979)
- [Melee Link/Ganon/Zelda](https://gamebanana.com/mods/445818)
- [Steam Deck UI](https://gamebanana.com/mods/459362)
- [OS Specific Intro Models](https://gamebanana.com/mods/442090) - there's actually a Steam Deck icon here, for when you first start the game

![Melee Link and Steam Deck HUD mod in SoH](/images/steam_deck_oled/guides/soh/game_mode/cover.jpg)

After a mod is downloaded, simply extract it into the `mods` folder where SoH is located. Restart the game, and the mods should automatically load. Note that you may need to check off "Use Alternate Assets" in Enhancements -> Graphics -> Mods in order to see alternate textures take effect. Also keep in mind you can't use multiple model swaps over the same character. For instance, you can't use the Melee Link mod in conjunction with the 3DS texture mod, unless you delete the OTR file for Link's model swap.

Enjoy *Ocarina of Time* on the go!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
