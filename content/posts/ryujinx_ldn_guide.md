+++
title = "Play Nintendo Switch Local and Online Multiplayer on Linux/Steam Deck -- Guide"
date = 2022-11-23T11:29:08-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ryujinx/ldn_guide/cover.jpg"
tags = ["guide", "ryujinx", "nintendo switch", "steam deck", "emulation", "smash bros", "ldn"]
keywords = ["ryujinx", "nintendo switch", "steam deck", "nintendo switch emulation", "super smash bros. ultimate"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Emulation has come so far. To the point where you can actually play online multiplayer on PC and Steam Deck with Nintendo Switch games, thanks to the [LDN version of Ryujinx](https://linuxgamingcentral.com/posts/ryujinx-ldn-3/). A number of benefits come with this, including:
- no need to cough up $20/year for a Nintendo Switch Online membership
- higher resolutions than 720p/1080p
- higher framerates
- the ability to use controllers *outside* of joycons, pro controllers, etc.

So let's walk through the process of getting this set up. This guide will be using *Super Smash Bros. Ultimate* and *Mario Kart 8* as examples, but the process is similar to any other game you want to play locally or online with. Requirements are as follows:
- jailbroken Switch (the launch edition Switch is the easiest to hack)
- a PC or Steam Deck
- MicroSD card
- a dump of `prod.keys` from your Switch
- a dump of whatever game you want to play multiplayer with
- a dump of your Switch's firmware
- Ryujinx LDN build

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/ryujinx_ldn/ssbu_ryujinx_ldn.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I do NOT condone piracy of the Switch files. Don't bother asking for help if you do so and come across any issues.

# 1. Have prod.keys, a Dump of your Game, and a Dump of System FW (optionally dump game updates, DLC, and save files)
Note that you will need a `prod.keys` file, as well as a dump of your game. You'll also need a dump of your system's firmware. There's plenty of tutorials out there to jailbreak your Switch and obtain these files. [Boiling Steam](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) is a great example if you're on Linux desktop. [Deck Central](https://deckcentral.net/posts/run_switch_games_on_steam_deck_with_ryujinx/) has a guide if you're using the Steam Deck.

After you have a dump of `prod.keys` and a dump of the game of your choice, copy the `prod.keys` file to:

`~/.config/Ryujinx/system/`

Copy the dump of the game and firmware to wherever you want. On Steam Deck you may want to copy the file to `~/Emulation/roms/switch/` if you have EmuDeck set up. You may also want to dump game updates, DLC, and your save file along with these files.

# 2. Download and Configure Ryujinx LDN
Download the Ryujinx LDN build from [Patreon](https://www.patreon.com/posts/74910544). The latest version at the time of writing this is 3.0.1. This build does *not* require an active Patreon membership; it is totally free to download. There's two builds to choose from: the one with the default UI, the other, the new Avalonia UI. I recommend going with the former, as the Avalonia UI has been a bit unstable in my experience. Extract the build anywhere to your desktop/Steam Deck. The executable file should already be marked as executable; if not, do so by right-clicking it and checking the appropriate box, depending on what desktop environment you're using.

![Ryujinx LDN main menu](/images/ryujinx/ldn_guide/main_menu.png)

Once the emulator is open, you might be asked whether you want to enable Vulkan or not. In most cases, you are going to want to use Vulkan as the backend. However, I do *not* recommend using Vulkan on the Steam Deck, as this has been unstable. Use OpenGL on Deck.

If you have `prod.keys` copied over to the right place, you shouldn't be getting any more pop-ups. If you do, make sure `prod.keys` is in the appropriate place (should be `~/.config/Ryujinx/system/`, including the Steam Deck). 

Now you're going to want to install your Switch's firmware. Go to Tools -> Install Firmware -> Install firmware from ZIP or directory, depending on how your FW was dumped.

![Ryujinx LDN install fw](/images/ryujinx/ldn_guide/install_fw.png)

Locate your dump file, and install when asked.

![Ryujinx LDN install fw confirmation](/images/ryujinx/ldn_guide/fw_install_confirmation.png)

Let's configure our user profile. Go to Options -> Manage User Profiles. By default the name is set to "RyuPlayer". We're going to want to change that. Change the profile name to your choice. You can optionally set an avatar here; either a custom one or one that's supplied by the system FW. Profiles can be added as well, if for some reason you needed to do that. Click Close when done.

![Ryujinx LDN configuring user profile](/images/ryujinx/ldn_guide/user_profile.png)

Now you're going to want to direct the ROM path to the path of your game dump(s). From the main menu, go to Options -> Settings. Add your ROM filepath by clicking the "Add" button underneath the "Game Directories" section in the General tab.

![Ryujinx LDN adding ROM filepath](/images/ryujinx/ldn_guide/adding_rom_path.png)

You're also probably going to want to configure the controls. Go to the Input tab, and configure the controls to your liking.

![Ryujinx LDN configuring controls](/images/ryujinx/ldn_guide/configuring_controls.png)

In the Graphics tab, adjust the resolution scale depending on what your display's native resolution is. You may also want to configure the aspect ratio to 16:10 if you're on Steam Deck.

![Ryujinx LDN adjusting graphics](/images/ryujinx/ldn_guide/graphics.png)

Finally, let's configure our multiplayer settings. In the Multiplayer tab, configure the mode to use either "Ryujinx Ldn" (default option selected) or "ldn_mitm". If you want to play online, select "Ryujinx Ldn". If you want to play locally, select "ldn_mitm". Optionally, set up a passphrase if you only want specific people to join your lobby.

![Ryujinx LDN configuring multiplayer mode](/images/ryujinx/ldn_guide/multiplayer_mode.png)

Click "Save" to save all of your changes and close the Settings window.

# 2b. (Optional) Configure Game Updates, DLC, and Save Data
If you want the game to use the latest update and have whatever DLC was installed on your Switch, make sure these files have been dumped and copied over to your desktop/Steam Deck. Right-click the game in the main window on Ryujinx, and click "Manage Title Updates". Here you can click "Add" to add the update file. Then it should be selected by default after it's been chosen. Click "Save" to save your changes.

![Ryujinx LDN configuring updates](/images/ryujinx/ldn_guide/updates.png)

Managing DLC is similar. Right-click the game, click "Manage DLC", and then "Add" to add your DLC files.

![Ryujinx LDN configuring DLC](/images/ryujinx/ldn_guide/dlc.png)

To use your Switch's save data, right-click the game, and select "Open User Save Directory". You can then copy over your Switch's dumped save file to here. When you launch the game, it should pick the save file up automatically. You can use [EdiZon](https://edizon.werwolv.net/) on your Switch to backup your saves.

![Ryujinx LDN save file location](/images/ryujinx/ldn_guide/save_data.png)

# Playing Online
If you want to play against others who aren't part of the same network as you, make sure "Ryujinx Ldn" is set as the mode in the Multiplayer tab in the Settings menu. Then simply launch the game of your choice, and go to the Local Wireless menu within the game. If anyone else is hosting a game, it should be visible if they haven't given it a network passphrase. If they did give it a passphrase, you'll need to enter this code in the Multiplayer tab to see it.

![Ryujinx LDN MK8 online lobby](/images/ryujinx/ldn_guide/mk8_lobby.png)

You can check the [LDN status page](https://ldn.ryujinx.org/) to see who's playing what game and how many are playing it. If you want people to join your lobby, you can go to the [Ryujinx Discord](https://discord.gg/VkQYXAZ) and use the appropriate LDN channel, depending on the game you want to play. For example, if you wanted to play the new *Pokemon Scarlet and Violet*, you would go to `#ldn-pokemon` or `#ldn-pokemon-sv-raids`.

# Playing Locally
If you wanted to connect your desktop, your Steam Deck, and even your actual Switch altogether on the same network, you can do that! On your desktop/Steam Deck, make sure "ldn_mitm" is selected as the mode in the Multiplayer tab.

Launch the game. Open up a lobby within the game's local wireless mode. If you're on desktop, for example, your Steam Deck should be able to pick the lobby up, and you should be able to join it.

![Ryujinx LDN MK8 local multiplayer lobby with physical Switch](/images/ryujinx/ldn_guide/local_ldn_with_switch.jpg)

If you want to connect your actual Switch to the lobby, it's a little bit more of a process. You will need to have the `ldn_mitm` submodule loaded on your system. You can download that [here](https://github.com/spacemeowx2/ldn_mitm/releases). Extract the zip file to the root of your Switch's MicroSD card. Turn the Switch on with custom firmware enabled. Launch the game. It should pick up the lobby if your desktop/Steam Deck is hosting one, so long as the devices are connected to the same network.

# Need Help?
Join the [Ryujinx Discord](https://discord.gg/VkQYXAZ) and go to `#support`.

That should be it for this guide. Might have a video soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
