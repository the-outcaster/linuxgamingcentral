+++
title = "How to Synchronize Save Files Between Computers for Games That Don't Support Steam Cloud"
date = 2022-09-05T09:36:11-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/syncthing/cover.jpg"
tags = ["guide", "syncthing"]
keywords = ["syncthing", "steam cloud"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Many games on Steam support cloud saving. Meaning, once you exit the game, your save file will be synchronized with the Steam Cloud. You can then play the game on a different device and quickly resume where you left off.

Some games, however, *don't* support cloud saves. You'll usually be able to tell by seeing if there is a cloud icon next to the green PLAY button, or by going to the Steam store page for the game. The old-fashioned method would have you manually copy the save file over to the next machine. This can be a bit of a pain. However, there's a tool that we can use that will simplify our life: [Syncthing](https://syncthing.net/). With Syncthing, we don't have to manually transfer the save files over. Just sync them between local machines on your network without any manual intervention.

I should note that this guide is **just between local machines on your network.** It's probably possible to sync save files outside of your LAN, but that is outside the scope of this tutorial. Another note is that Gardiner Bryant has a [video](https://youtu.be/VdX1109RUtA) version of this if you prefer your tutorials that way.

# Get Syncthing
Syncthing, as you might have guessed from the name, is a program that synchronizes files between two or more computers. Syncthing is [open-source](https://github.com/syncthing/syncthing) and licensed under the Mozilla Public License 2.0. It's available for Linux, Mac OS, Windows, and pretty much *any* device that has support for a web browser.

Simply head over to the [Downloads](https://syncthing.net/downloads/) page on the official website and look under the "Base Syncthing" section. Download the version appropriate for your device. If you're using the Deck, for example, you would select the 64-bit Linux version. If you're on a Debian- or Ubuntu-based distro, you can install it as a [package](https://apt.syncthing.net/). You can, of course, install it on Arch via the [AUR](https://aur.archlinux.org/packages/syncthing-bin) as well.

Extract the archive to a convenient location on your device. Double-click the `syncthing` executable file and a new tab should open up with your default web browser. The URL should be something like `http://127.0.0.1:8384` and the Syncthing interface should be present:

![Syncthing interface](/images/syncthing/step1.jpg)

So here I am on my Oryx Pro laptop by System76. The device name in this instance is "pop-os". You will be asked if you want to anonymously report various statistics based on your usage of the program. Syncthing also recommends setting up a username and password, but this is optional.

Repeat this process for all the computers you want to sync save files with. For the sake of this tutorial I will be syncing with my desktop, called "salientos".

# How to Sync Save Files
Make sure you know where the save file is located. This is generally different for every game. An easy way to find out the location is by checking the game on [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Home). For this tutorial, I'll be demonstrating [*Ex-Zodiac*](https://store.steampowered.com/app/1249480/ExZodiac/). Since the game is pretty new, there's no page for it on the Wiki. But I happen to know where the save file location is. On Linux, it's:

`~/.local/share/godot/app_userdata/Ex-Zodiac/`

On the other hand, if you're wanting to sync a save file from a game that's played through Proton, the file path is going to be *much* longer. Let's take [*Nickelodeon All-Star Brawl*](https://www.pcgamingwiki.com/wiki/Nickelodeon_All-Star_Brawl#Save_game_data_location) as an example. On Windows, this save file would be located in `%USERPROFILE%\AppData\LocalLow\GameMill Entertainment\Nickelodeon All-Star Brawl/`. On Linux, we have to append that file path to:

`<Steam-folder>/steamapps/compatdata/1414850/pfx/`

Usually `<Steam-folder>` would be `~/.local/share/Steam`. If you have Steam installed as a Flatpak, it would be:

`~/.var/app/com.valvesoftware.Steam/.local/share/Steam/`

If you're with me so far, the default save data location for *Nickelodeon All-Star Brawl* would be:

`~/.local/share/Steam/steamapps/compatdata/1414850/pfx/drive_c/users/steamuser/AppData/LocalLow/GameMill Entertainment/Nickelodeon All-Star Brawl/`

Make sure the machines that you want to sync save files with are all running Syncthing. We're going to want to add a remote device; the other computer that we want to sync up with. "Click Add Remote Device" under Remote Devices. The device ID of the other computer running Syncthing should be present underneath the first text field. Simply click on it to add it. You can then give this device a name. In my case I'm going to name it "Desktop" since that's what I want the save file to sync with. You can ignore the rest of the options that are present; you shouldn't need to mess around with them at this time.

![Syncthing adding a new device](/images/syncthing/adding_a_new_device.jpg)

Observe the Syncthing interface on the other device. There should be a prompt at the top of the page, asking if you want to add a new device. Go ahead and add it and give it a name if it's not filled in already.

![Syncthing add new device prompt](/images/syncthing/new_device_prompt.jpg)

The remote device should now be listed under "Remote Devices". Give it a few moments and it should say "Connected" or "Up to date" in green text.

![Syncthing new device added](/images/syncthing/remote_device_added.jpg)

Great! Now we can share folders between devices. Under the "Folders" section in the Syncthing interface, we're going to want to add the folder where our save file is present (it doesn't matter which device you use). Click "Add Folder". Give the folder label a name. In my case, I'm going to name it to "Ex-Zodiac Save" since I'm demonstrating *Ex-Zodiac*. Under "Folder Path", copy the file path of the save data location and put it here. So I would put `~/.local/share/godot/app_userdata/Ex-Zodiac/`.

![Syncthing adding a new folder](/images/syncthing/adding_a_folder.jpg)

Under the "Sharing" tab, check the box next to the device that you want to sync this folder with. I'm going to check off "Desktop" since that's the device I want to sync with. Click "Save". Now go back to the other computer, and you should get another prompt at the top, where you will be asked if you want to add the folder from the other computer. Click "Add". This time under Folder Path, make sure it is pointed to the save file location for that device. On the Desktop for me, it's the same path as on the Oryx Pro. Click "Save" and now your save file should be synced between each device!

![Syncthing new folder prompt](/images/syncthing/folder_prompt.jpg)

Test it out by using the device that didn't have the up-to-date save file. If everything went well this device should pick up the more up-to-date save file from the other computer. Now you can easily synchronize save files between devices on your local network without having to manually transfer the save file over! Just make sure Syncthing is running in the background on both machines. If you're playing a game in Game Mode on the Deck, you may need to go to Desktop Mode and run Syncthing to get the save synced with your other computer.

Using the same principles, you can also sync your save files from emulators, games from the Epic Games Store, GOG saves, etc.

Any questions, feel free to ask away in the comments.

*Cover image credit: vectorstock.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
