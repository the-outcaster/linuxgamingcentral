+++
title = "Play Sonic Adventure 2 in HD - Modding Guide"
date = 2022-12-20T12:21:41-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/sa2_modding_guide/cover.webp"
tags = ["guide", "sonic", "sonic adventure 2", "modding", "steam deck"]
keywords = ["sonic adventure 2", "sonic adventure 2 hd", "modern sonic adventure 2", "sonic adventure 2 modding", "steam deck", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*Sonic Adventure 2* -- the cult classic. Fans have gotten together to make the game moddable. From an [extended Chao World](https://gamebanana.com/mods/48840), to the ability to [play as Super Sonic or Super Shadow](https://gamebanana.com/mods/340288), to [revamped cutscenes](https://gamebanana.com/mods/48872), it's amazing to see what the modding community has been able to accomplish to make a great game even greater.

But for today's guide, we'll be focusing on giving the game a modern HD look. Not only are the character models replaced with more modern-looking ones, but the mod also contains a sound redesign. Audio no longer clips harshly, the audio balancing has been re-worked, audio's been added for karts, BGM has been replaced, you name it. Stages have also received new vertex paint, textures, lighting, fog, overlays, and grass effects. Physics have been revamped. For example, speed characters will have increased acceleration the more rings they have.

This guide is for both Linux desktop and Steam Deck users. It's mostly the same steps for each device, but I will make note if there's anything different to do if you're on Deck.

![SA2 title screen](/images/sa2_modding_guide/title_screen.jpg)

Keep in mind this mod is a bit unstable. If you load the wrong character into a stage, for instance, the game will crash due to not having the animations for that character. Story mode will crash after completing the first stage.

# Backup your Save File Before Proceeding
I recommend getting a [save file](https://gamebanana.com/mods/48903) that has 100% completion so you can use stage select. Extract the save file to `/resource/gd_PC/SAVEDATA/` in the game's installation directory. Backup your original save file if you have one in there.

# 1. Get the Mod Loader
The mod loader is available to download over on [GameBanana](https://gamebanana.com/tools/6333). After downloading, extract the archive to the root folder of your game's install directory. By default this would be:

`~/.local/share/Steam/steamapps/common/Sonic Adventure 2/`

An easy way of getting access to your install folder is by right-clicking the game on Steam -> Manage -> Browse local files.

![Browse local files in Steam](/images/sa2_modding_guide/local_files.webp)

After extracting, there should be an executable file called `SA2ModManager.exe`. Make sure Wine is installed on your system. If you're on Steam Deck, you may need to install [Lutris](https://flathub.org/apps/details/net.lutris.Lutris) and run the app this way, since it may not launch with Wine directly.

![SA2 Mod Manager](/images/sa2_modding_guide/mod_manager.png)

We will add the mods later. For now, go to the Graphics tab. Set your desired resolution. You can optionally check "Lock framerate" if you're using a monitor with a high refresh rate to keep the game from going over 60 FPS.

![SA2 Mod Manager graphics settings](/images/sa2_modding_guide/graphics_tab.png)

In the Options tab, make sure "Disable loading animation" is checked, as apparently without this the HD mod will have crashing issues. Might also be worth checking off "Skip Intro" to save yourself some time when booting the game. Note that "Enable 1-Click Install" does *not* work for getting mods, at least for me.

![SA2 Mod Manager options](/images/sa2_modding_guide/options_tab.png)

Click "Save". Note that you will probably be asked to install the mod loader when you click this button for the first time. Go ahead and do so. The application will close, but you should be able to open it back up with the mod loader installed.

# 2. Get the Mods
Now let's get our mods. In addition to getting [Modern SA2](https://gamebanana.com/mods/406063), you will also need:
- [HedgePanel](https://gamebanana.com/mods/48950) -- fixes homing attack and fast somersault
- [Character Select Plus](https://gamebanana.com/mods/33170) -- required to see Sonic's version of White Jungle
- [SA2 Volume Controls](https://gamebanana.com/mods/381193) -- fixes audio engine
- [No Model Tinting](https://gamebanana.com/gamefiles/9820) -- fixes models being tinted darker than they should be

Optional, but *recommended* mods are as follows:
- [Action Remap](https://github.com/michael-fadely/sa2-action-remap/releases) -- remaps the light dash to the Y/Triangle button
- [No Battle](https://gamebanana.com/guis/33707) and [Menu Overhaul](https://gamebanana.com/guis/34471) -- cleaner menus with "pretty coloured backgrounds"
- [Reworked Afterimages](https://gamebanana.com/mods/331030) -- enables colored, lit-up light dash models for Sonic and Shadow
- [Amy New Tricks](https://gamebanana.com/mods/354107) -- allows Amy to be a playable character, since the mod doesn't fully support her just yet

Extract all of these mods to the `mods/` folder inside the game install directory. For Modern SA2, copy and replace the `obj.pak` file from the archive into `resource/Shader/win32/`. This restores the brightness from the Dreamcast version of the game.

Your `mods/` folder would look something like this:

![SA2 mods folder](/images/sa2_modding_guide/mods_folder.png)

# 3. Configure Mods and Codes
Open the mod manager again. If the mods were extracted to the right place, they should now be showing up in the Mods tab.

![SA2 mods](/images/sa2_modding_guide/mods.png)

Individual mods can be enabled or disabled by checking off the box next to them. Note that some mods will have a configuration window available for them. If you click the mod, the "Configure..." button won't be greyed out. We're going to need to configure some of these mods, so see the screenshot below for the configuration of each one.

![SA2 mods](/images/sa2_modding_guide/mod_configuration.jpg)

So for the Reworked Afterimages mod, you would change the light dash behavior to **LoD2**. For the HedgePanel mod, you would change "Random Homing Attack Sounds" and "Bounce up after Light Attack" options to **false**. For the SA2 Volume Controls, you can change this to your liking. I have everything set to 100 except for the Music Volume; that's set to 80.

Now head to the Codes tab. Make sure "Shadow Has Bounce Bracelet" and "Squash n Stretch Bounce Effect" codes are checked off; they should be by default.

![SA2 codes](/images/sa2_modding_guide/codes_tab.png)

Click "Save" from the bottom left corner of the window when you're done.

# 4. See the Game in HD
Launch the game from Steam. Unfortunately I don't think it's possible to skip the launcher while keeping the mods intact. But feel free to let me know if there's a solution for that.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/sa2/hd_clip.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Feel free to add other mods as desired. Should you want to disable any of them, use the mod manager. You can see a video of the HD mod in action [here](https://www.youtube.com/watch?v=pgIIfWvtTD4).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
