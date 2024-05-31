+++
title = "Sonic Frontiers - Updated Steam Deck Modding Guide"
date = 2022-12-26T12:55:34-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/frontiers.webp"
tags = ["guide", "sonic", "sonic frontiers", "steam deck", "modding", "steamtinkerlaunch"]
keywords = ["sonic frontiers", "linux", "steam deck", "hedge mod manager", "steamtinkerlaunch", "modding"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**UPDATE (12/29/2022): this guide has been updated to make sure HMM runs! I also have a [video](https://www.youtube.com/watch?v=66B9K-wSqTo).**

I guess many of the people who have tried adding mods to *Sonic Frontiers* on Deck have [had trouble](https://www.youtube.com/watch?v=FJs1FADQI08). And up until this point I've had no idea how to help troubleshoot the various issues they've encountered. Fortunately SolarNyan came to the rescue with an [updated guide](https://github.com/thesupersonic16/HedgeModManager/issues/219#issuecomment-1363093591). I'll explain their steps here with pictures and videos.

If you're on Linux desktop, you should still be able to make use of my [older guide](https://linuxgamingcentral.com/posts/sonic-frontiers-modding-guide/).

All-in-all you're going to need at least an hour to get all of this set up; many of the installs will take a while.

*Disclaimer: there's still a chance you won't be able to get mods to work for X, Y, or Z reason. If you follow these steps and still have issues, I will NOT be able to help you any further; please file them [here](https://github.com/thesupersonic16/HedgeModManager/issues/219). But hopefully this should be the last guide you'll ever need.*

**I recommend connecting a keyboard and mouse, as some of these steps will require your hands to get dirty with the terminal. Also, make sure you're on SteamOS 3.4 or later. And quick tip: pressing TAB while in the terminal will autocomplete your commands and file paths. Saves you some time!**

# 1. Configure Your Deck's Power Settings
Go to Desktop Mode on your Deck. We'll need to make sure the Deck doesn't go to sleep at all during this process; the last thing we want to happen is for the sleeping mode to trigger while we're in the middle of installing `dotnet48`.

Launch "System Settings" from the taskbar. Scroll down to "Power Management" under the Hardware section. From the "Energy Saving" section, uncheck "Suspend session" on both the "AC Power" and "Battery" tabs. Click "Apply" when done.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/changing_power_settings.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

You may also want to disable screen locking. Click the left arrow on the top-left of the window to go back to the main menu for System Settings. Scroll up to the "Workspace" section and click "Workspace Behavior". Click "Screen Locking". Uncheck "Lock screen automatically" and click "Apply" when finished.

# 2. Use Proton 5 to Generate Proton Prefix
Obviously, make sure *Sonic Frontiers* is installed. Open Steam while in Desktop Mode, right-click the game -> Properties... In the new window that opens, go to the Compatibility tab. Check off "Force the use of a specific Steam Play compatibility tool". In the dropdown menu that will appear, click it and select Proton 5.0-x ("x" should be 10). Steam will download this version of Proton (or it may download when you click "PLAY"). Close the window, then launch the game. This will generate the Proton prefix needed for Hedge Mod Manager to run, which would include `dotnet40` and `dotnet48`.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/switch_to_proton5.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Give it a few minutes. The game won't launch (Steam will try quite a while but nothing will happen), but the prefix should be generated. Close the game through Steam.

# 3. Install Protontricks and DotNet40/48
Install Protontricks via the Discover app. Alternatively you can bring up a terminal window with `CTRL + ALT + T` and install with:

`flatpak install flathub com.github.Matoking.protontricks`

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/install_protontricks.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Add an alias to Protontricks via the terminal (this will allow you to run Protontricks with just `protontricks`, rather than `flatpak run com.github.Matoking.protontricks`):

`echo "alias protontricks='flatpak run com.github.Matoking.protontricks'" >> ~/.bashrc`

Close the terminal, then open it up again for the change to take effect.

Now we'll run Protontricks with *Sonic Frontiers*:

`protontricks --no-background-wineserver 1237320 --force dotnet48`

"1237320" in this case is the game ID for *Sonic Frontiers*. "--force dotnet48" will install said tool, which is what we need for Hedge Mod Manager to run. Also, you'll be installing `dotnet40`.

![Dotnet install](/images/guides/sonic_frontiers_modding/updated_guide/dotnet.png)

Give it some time. By "some time" I mean upwards of thirty minutes. Make yourself a cup of coffee. After that, the installers for `dotnet40` and `dotnet48` should appear. Let them install. Again, be patient, it'll take a while.

If for some reason `dotnet` was installed previously, just select "Repair" and proceed with the install.

After installing `dotnet40`, you'll be installing `dotnet48`. You may run into an installer error. Just click "Continue" to proceed with the installation. Click "Finish" when...it's finished. If you get asked to reboot, you shouldn't need to.

![Dotnet error](/images/guides/sonic_frontiers_modding/updated_guide/dotnet_error.png)

There *may* be a chance that after all this work the next steps won't. Hopefully that won't happen, but if it does, you'll have to go back to steps 2 and 3. If the installs went well you should be able to close the terminal without issue.

# 4. Backup the Proton Prefix
It's important to have backups, in the event anything goes wrong. Let's back up the Proton prefix for *Sonic Frontiers*. This folder would be located in `~/.steam/steam/steamapps/compatdata/` and will be labeled "1237320" (the tilde "~" is short for `/home/deck/`). Back this up to wherever you want. Somewhere where you'll have convenient access to it in the event that you *do* need it.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/backup_prefix.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

An easy way of backing this up to your desktop would be:

`cp -r ~/.steam/steam/steamapps/compatdata/1237320/ ~/Desktop/`

# 5. Get SteamTinkerLaunch (STL) with ProtonUp-Qt
STL will allow us to run Hedge Mod Manager. And to install STL, we can use ProtonUp-Qt. Get it from the Discovery app, or install with:

`flatpak install flathub net.davidotek.pupgui2`

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/install_protonup-qt.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

After that's installed, you should be able to launch it from the Start Menu. Go to the "Utilities" section and look for "ProtonUp-Qt".

When the window opens, click "Add version". Under the "Compatibility tool" dropdown menu, select "SteamTinkerLaunch". Make sure the version is **12** or later (at the time of writing this, [v12](https://linuxgamingcentral.com/posts/steamtinkerlaunch-v12/) just released over the weekend). Close ProtonUp-Qt.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/installing_stl.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

If Steam is open, exit and then re-open the client for the changes to take effect.

# 6. Make Hedge Mod Manager (HMM) use Proton 5.0-10b
In Steam, right-click *Sonic Frontiers*, and force the game to use STL from the dropdown menu on the Compatibility tab. Launch the game. Quickly click "Main Menu" once the STL dialog box opens before it launches the game. Click "Global". Under the HMM section, force HMM to use Proton 5.0-10b from the dropdown menu (this option should be listed since we previously forced the game to use said version of Proton). Click "Save", then close the STL window.

![HMM forcing Proton 5](/images/guides/sonic_frontiers_modding/updated_guide/forcing_hmm_to_use_proton5.png)

# 7. Run HMM
Note that currently we can't run HMM through STL directly. So we have to launch it via the command line.

In a terminal, navigate to `/home/deck/stl/prefix/`, where our STL executable file is located:

`cd ~/stl/prefix/`

As of version [7.9](https://github.com/thesupersonic16/HedgeModManager/releases/tag/7.9), HMM supports *Sonic Frontiers*. So we don't need to run the latest nightly release anymore. Run the latest stable release of HMM with:

`./steamtinkerlaunch hmm start`

This will take a while on first run. If you get an error about rundll32.exe, just click "No" to continue.

Nothing will happen. This is normal. Now we need to force HMM to use a newer version of Proton.

# 8. Use a Newer Version of Proton for HMM
Repeat the process from step 6, but this time, force HMM to use a newer version of Proton, such as Proton Experimental or GE-Proton.

![HMM forcing GE-Proton](/images/guides/sonic_frontiers_modding/updated_guide/forcing_hmm_to_use_ge_proton.png)

# 9. Run HMM Again
Repeat the process from step 7. Hopefully HMM should now open.

You shouldn't need to modify any of the settings under the "Settings" tab -- although you may need to use the Light theme in order to properly see the codes from the "Codes" tab. Under said tab, select whatever codes you want by checking them off. New codes are added daily, so if you get an update prompt, go ahead and do so.

![HMM codes tab](/images/guides/sonic_frontiers_modding/updated_guide/hmm.png)

Codes I'd recommend enabling:
- fix resolution resetting on launch
- disable challenge marker scanner
- disable Guardian interactions
- disable power boost cutscene
- disable umbrella camera lock-on
- disable framerate limiter in cutscenes (renders cutscenes at 60 FPS rather than 30)
- disable in-game letterboxing
- disable fixed camera notifications
- hide skip button in cutscenes

Under the "Mods" tab, there shouldn't be anything there. Download mods from [GameBanana](https://gamebanana.com/mods/games/15779). Extract these mods to the "Mods" folder inside your game's installation directory. To get access to this folder, right-click the game in Steam -> Manage -> Browse local files.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/adding_a_mod.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

1-Click install *technically* works if you open up a terminal and run `xdg-open <1-click-mod-url>` but it's more hassle than it's worth, so I'd recommend downloading mods manually.

![HMM mods tab](/images/guides/sonic_frontiers_modding/updated_guide/hmm_mods.png)

After you've extracted the mods to the appropriate location, click "Refresh List" in HMM under the "Mods" tab. These should now be showing up. To enable them, simply tick the checkbox next to the mod name. Some mods may have the settings cog icon not greyed out; you can click this to further configure the mod.

# 10. Save Settings and Run
After checking off the mods and codes that you want, click "Save". Don't click "Save and Play"; we need to configure a different Proton version for use with *Sonic Frontiers*.

Go back to your Steam library, right-click the game -> Properties... Go to the Compatibility tab, and force a newer version of Proton, such as Proton Experimental or GE-Proton (you can obtain GE-Proton with ProtonUp-Qt).

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/sonic_frontiers_deck_modding_guide/change_to_ge-proton.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Launch the game and see if your mods/codes worked... (praying no one has any issues)

That *should* be it. Again, I have a gut feeling someone is going to run into an error along the way, and if that happens, I really, *really* don't know what to tell you. This is admittedly a janky way of getting mods to work, and there's so many different variables at play that I wouldn't even know how to get started helping someone with the troubleshooting process. Submit your bugs [here](https://github.com/thesupersonic16/HedgeModManager/issues/219) if you run into any issues.

Should you want to run HMM again, it should be available under "Games" from the Start menu. If for some reason it won't run, run `./steamtinkerlaunch hmm start` inside of `~/stl/prefix/`.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
