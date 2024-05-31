+++
title = "Slippi: Getting it Set Up on Linux"
date = 2022-03-16T12:28:50-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://pbs.twimg.com/media/E2FjrmxWEAI9mNV?format=jpg&name=4096x4096"
tags = ["slippi", "emulation"]
keywords = ["linux", "slippi", "emulation", "gamecube"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*Super Smash Bros. Melee*. The game I will cherish to time indefinite. I won't spend this article on my fascinations with this game (although I may do that in a separate post); let's get right to the point. Let's get this game set up on your Linux machine (and maybe your Steam Deck?) so you can start playing the game online with others...with rollback netcode! The process really isn't that complicated, but this guide should give you some tips on how to get the best experience.

# A Note If You're Coming from Smash Ultimate
If you've played *Smash Ultimate*, *SM4SH* for Wii U/3DS, or *Super Smash Bros. Brawl*, and have never played *Melee*, please know *Melee* is a more fast-paced, technical game, with more advanced gameplay mechanics that will take some time getting used to (which is why the competitive players love it so much). If you're new to *Melee*, there's *plenty* of [tutorials](https://www.youtube.com/playlist?list=PLoU3TQBakHOrE9yYdNlsmG74LEB0Mf3h8) out there to get you started.

# Getting Started
I assume everyone reading this has a legal copy of the disc. I have mine right here:

![ssbm japan disc](/images/slippi_guide/disc.jpg)

It's the Japanese version but it works just fine on both my region-unlocked Wii in the US and with Slippi, and I can change the language to English in the Options menu. Otherwise it's pretty much exactly the same as the US version, albeit for character names and a different title screen; the character balances are identical. Japanese copies sell for a lot less than their US counterparts. US discs hover around $60-$80 used on eBay at the time of writing this. So hopefully you already have a disc that you've had around for the past 20 years or so...otherwise you're going to pay a pretty penny (unless you buy a Japanese version). I don't think I need to tell anyone that I do *not* condone piracy of the game.

*Note: don't buy the European version; [the balance adjustments to characters are different](https://smashboards.com/threads/ssbm-version-converter-patcher-32-bit-beta-released.295223/) than the US/Japan copies and will likely cause desyncs.*

You're also going to need a device that can dump the game. A Wii is your best bet. You can easily install custom firmware on it and get the necessary homebrew app to dump it. An example of an app is [CleanRip](https://wii.guide/dump-games.html). Technically, you can rip GC discs on a computer, but this requires a DVD drive which is capable of reading the disc. You can check the [Dolphin Wiki](https://dolphin-emu.org/docs/guides/ripping-games/) for more details on that.

I also need to note **the disc needs to be version 1.02**. If it's not, problems can potentially arise with other players due to balance patches that are different from one version to the next and can cause sync issues. You can find out the game version by looking at the disc's back side and noticing the numbers across the top:

![ssbm japan disc back](/images/slippi_guide/disc_version.jpg)

If you zoom in very closely (may need to open the image in a new tab), you can see across the top above the disc hole is `DOL-GALJ-0-02`. The `J` tells me it's a Japanese copy. The `02` tells me the disc is version 1.02. If it's `00`, it's version 1.00. If it's `01`, then it's version 1.01. In your case it might be `DOL-GALE-0-02` if it's the NTSC version.

That being said, if your disc isn't using 1.02, don't fret. You can use this [converter](https://smashboards.com/threads/ssbm-version-converter-patcher-32-bit-beta-released.295223/) after you dumped the disc to change versions. That thread is over 10 years old though, and the program was designed for Windows XP...so I've got no idea whether it even runs through Wine or not.

**An Ethernet connection is strongly recommended.** Wi-Fi introduces latency and packet loss. Not only will your experience suffer, but so will your opponent's. If you don't have close access to your router, you can use a [powerline ethernet adapter](https://www.amazon.com/s?k=powerline+ethernet+adapter&crid=3T7JGDKV2XJ7T&sprefix=powerline+ethernet+adapte%2Caps%2C85&ref=nb_sb_noss_2). This way you can insert an Ethernet cable from your PC to an adapter on the wall. That adapter will then communicate to the other adapter that's connected to your router, giving you an Ethernet-like experience. They're not that expensive, depending on the model you get. Only downside there is your connection speed won't be as high as it would with a straight connection from the PC to the router, but it will certainly provide a much more stable online experience.

As for PC requirements, Dolphin is emulating a game that's more than 20 years old...you really don't need anything big. You don't even need discrete graphics. That being said, if you're using a device that *still* can't handle *Melee*, you can use [Diet Melee](https://diet.melee.tv/), which will reduce the poly count and make the game playable on older hardware. I haven't tried, but Diet Melee could probably run on a Raspberry Pi 4.

![slippi singles](/images/slippi_guide/singles.jpg)

For your Linux distro, it honestly doesn't really matter, as thankfully Slippi -- a fork of the Dolphin emulator designed specifically for *Melee* -- is provided as an AppImage since version 2.20. All the dependencies for Slippi are built into the AppImage, so this tutorial is pretty much distro-agnostic. That being said, you can also compile Slippi from [source](https://github.com/project-slippi/slippi-launcher) or get it through the [AUR](https://aur.archlinux.org/packages/slippi-launcher) if you're an Arch user, but I won't be covering those methods here. Slippi is not available as a Flatpak at the time of writing this, but it should still be possible to run on the Steam Deck with the AppImage.

Next up, you'll need to create an account for Slippi. Just click the top-right icon on the [Slippi home page](https://slippi.gg/) to get started. All you need is an email address, a password, and a name that will be shown to your opponents during a match.

You will generally see the top players use a GameCube controller. I don't find it strictly necessary myself; I switch between an Xbox Series gamepad and a DualSense and they both work just fine for me. You can also use a keyboard if you'd like.

So, for a quick checklist, here's what you need to get started:
- a legal copy and dump of Melee (v1.02) that *isn't* the PAL version
- a PC with an Ethernet connection, with any Linux distro
- a Slippi account
- controller or keyboard

# Get Slippi and Configure Settings
You can download an AppImage of the Slippi Launcher right on the project's home page. It should automatically detect what operating system you're using. Download it, copy it to a convenient location, then mark it as executable by either right-clicking the AppImage and going to your DE's properties menu, or navigating to the folder containing the AppImage with a terminal and entering this:

`chmod +x Slippi-Launcher-<version_number>-x86_64.AppImage`

Now, when I said the word "launcher," that probably made some of you cringe. If so, you don't actually need to use a launcher for Slippi; you can just download the [fork of Dolphin](https://github.com/project-slippi/Ishiiruka/releases) and use Dolphin's GUI to launch the game. However, I recommend using the launcher, as not only does it provide an easy way to launch the game, but it also checks for updates, you can read the patch notes, read Tweets from the project creator, manage and watch your replays, and more.

Launch the launcher. Some stuff will get downloaded in the background, then you will eventually be presented with a login screen.

![slippi launcher login](/images/slippi_guide/login.jpg)

Since you've already created an account earlier, go ahead and enter your login details. If not, click "Create an account". After logging in you'll be asked to select your *Melee* ISO. The window will say "NTSC" but my Japanese ISO works just fine. The launcher will then try to verify to make sure that it will work online; if not, it will give you a warning.

After that you should be good to go. Click PLAY and *Melee* will immediately launch.

![slippi main menu](/images/slippi_guide/launcher_main_menu.jpg)

You're probably going to want to configure your controls first; chances are your gamepad will not work out-of-the-box. So after you've verified that the game runs, close the game window, and go into Slippi's settings menu (just click the cog icon on the top-right). On the Game tab, configure the play button action to launch Dolphin instead of Melee. Dolphin should now open.

![dolphin main menu](/images/slippi_guide/dolphin.jpg)

From the Options menu, click Controller Settings. If you're not using a GC-to-USB adapter, change the controller to "Standard Controller" on port 1. Now click Configure. Configure your gamepad as desired. You may want to save the controller profile by giving it a name, then selecting Save. You will now be able to load this profile at any time, in case you change the controller settings again.

![dolphin controller configuration](/images/slippi_guide/gamepad_config.jpg)

Most other settings for Dolphin, you're not going to want to change. You may want to increase the interal resolution of the game by going into Dolphin's graphics settings to your monitor's native resolution or change the aspect ratio, but that's about it. Later on you may want to force a netplay port for doubles, but for now, leave the rest of the settings as is.

You can configure Gecko codes to optionally enable widescreen 16:9 support, disable screen shake, aligh the HUD for one-on-ones, flash red on failed L-Cancels, show friendly player indicators, or boot straight to the CSS (character selection screen). You can enable or disable these codes by right-clicking the game in Dolphin and selecting Properties, then going to the "Gecko Codes" tab. Note that the first three codes in the list are required for online play, the next two are recommended, and the rest are optional. The required and recommended codes are already checked.

![slippi gecko codes](/images/slippi_guide/gecko_codes.jpg)

# Test Your Settings
While it may be tempting to immediately start playing, the first thing you're going to want to do is ensure the game runs at a buttery-smooth 60 FPS, without any dips. Hit the Training mode, pick a character, pick an opponent, pick a stage, then start testing. Legal stages include:
- Final Destination
- Battlefield
- Dream Land
- Yoshi's Story
- Pokémon Stadium
- Fountain of Dreams

When I say *legal*, I mean stages that are permitted in tournaments. The more competitive-like stages where the playing field is balanced. So basically a flat plane with maybe a couple of platforms. Not like the Temple stage where there is completely uneven terrain. That being said, non-legal stages are permitted in doubles.

Make sure your controls are to your liking, and make sure the FPS counter in the top-left stays at a stable 60 FPS. Rare dips to 58 or 59 FPS shouldn't be *too* much of a problem while playing online, but if the framerate gets any lower than that, decrease the internal resolution or make sure your graphics drivers are up-to-date. Again, Diet Melee is also an option here if your PC is *really* old.

![slippi training mode](/images/slippi_guide/screenshot1.jpg)

If you want to play doubles, you may also want to add a few CPU opponents in the Training menu and make sure the framerate is stable with four players.

# Singles (Unranked and Direct)
After ensuring the game runs smoothly, now you can start playing online. Online play is accessible from the 1-P mode menu. Options include:
- unranked singles
- direct (play against a specific person with their tag)
- teams

Ranked multiplayer isn't here yet.

With unranked, just pick a character, then press Start. The game will try to find an opponent. Generally it only takes a few seconds to find someone to play with, regardless of the time you start playing. The stage will be a random legal stage. **Each player has four stocks, and the game length is eight minutes**. After a round you can send the opponent quick messages with the D-pad, and whenever you want to disconnect from them, hold the Z button.

If you prefer to play against a specific person, you can do so with Direct mode. Pick a character, and when you press Start, you will be asked to enter the opponents's connect code. In my case, my connect code is `COW#938`.

![slippi CSS connect code](/images/slippi_guide/connect_code.jpg)

So I would send my opponent my connect code and he would send his to me. I would then put in his connect code and start searching.

While playing, take note of the opponent's ping. It's under the FPS counter. I've seen pings as low as 20; that's a *really* good connection. Sometimes it might be around 50, other times it can be more than that. If it's over 100, you'll probably notice some lag. That's when you're going to want to find someone else.

# Doubles
Doubles is pretty fun, but keep in mind friendly fire is on. If you don't have anyone to partner with, you can just search `EC`, `MW`, `WC`, or some other area code depending on where you are. In my case I'm in the east coast in the US, so I would search `EC`. Anyone else that's searching for `EC` at that moment will be put together into a match. Assuming everyone is red, teams will be assigned at random.

By default your team color is red. You can change the color of your team by moving the cursor to where it is in the screenshot and pressing A.

![css team color](/images/slippi_guide/team_color.jpg)

Colors besides red include blue and green.

If you have three other people, you can use any code. You could use `MELEE` for example. Anyone that searches `MELEE` will be put into that specific match.

A good way to find other people to play with is by going to the `#doubles` channel on the [Melee Online Discord](https://discord.gg/KczB6au). Generally, it's difficult to get four people together during the day in the east coast, but at night, I've found that it's a lot more likely I'll find others to match up with.

One thing that you want to keep in mind with doubles, is that **you're generally going to want everyone in the same region**. If you have three people in the east coast and one person in the west coast, generally it shouldn't be *too* bad of an experience. If their ping is over 100, though, you may want to find someone else.

Another thing with doubles is you should **enable port forwarding**. If this isn't enabled, there's a good chance that when you do find a match, you'll get an error and won't be able to connect. Enabling this requires going into the Dolphin Configuration menu, going to the Slippi tab, and checking the box for "Force Netplay Port". By default the port number will be 2626. You're going to want to go into your router settings and forward this port to the IP address of the computer that you're using to play *Melee*. That, however, is outside the scope of this guide. I may cover it in a separate guide though if there are enough requests.

![slippi force netplay port](/images/slippi_guide/port_forwarding.jpg)

# Other Tips
While playing, you might have noticed there's no music. This is because it will break the rollback netcode. But you don't need to suffer. You can use a tool called [M'Overlay](https://github.com/bkacjios/m-overlay/wiki/Stage-music-for-Project-Slippi) to get in-game music that will change depending on the stage or where you are in the menus. You can add your own music, but if you want the music that was included on the disc, you can find the instructions on [Reddit](https://www.reddit.com/r/SSBM/comments/i2z6xo/melee_music_for_slippi_online_using_moverlay/).

Diet Melee doesn't just help older computers emulate the game; you can also find a neat N64-style mod for it that makes the graphics reminiscent of the N64 game. Diet Melee also drastically reduces the ISO file size -- from 1.35GB to something like 236 MB. Useful if you want to transfer the ISO between flash drives and computers. Just keep in mind Diet Melee only works with the legal stages, and accessing the Adventure mode, Classic mode, or anything like that will crash the game.

Besides all those things, you can check [blippi.gg](https://blippi.gg) for a *ton* of useful resources for *Melee*, including an HD mod pack, look up character frame data, find a coach, find more tutorials, view documentaries on the development of *Melee* and *so* much more.

![slippi doubles](/images/slippi_guide/doubles.jpg)

That should do it for this guide! Let me know in the comments if you have any questions.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
