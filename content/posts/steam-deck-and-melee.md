+++
title = "Steam Deck: How Does it Melee?"
date = 2022-06-21T12:20:15-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/photos/melee/steam.jpg"
tags = ["steam deck", "melee", "slippi", "smash bros", "guide"]
keywords = ["ssbm", "super smash bros.", "melee", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
One of the first things I wanted to do after getting my Steam Deck was test *Super Smash Bros. Melee*. Not just to see how well it performs, but also examine online play and see how the controls feel in my hands.

# How to Get Melee/Slippi Working on Deck
If you're looking at getting online play set up on Linux, you can refer to the [guide](https://linuxgamingcentral.com/posts/slippi_guide/) I wrote a few months back. The Steam Deck in particular though requires a few extra steps. Slippi is still not available as a Flatpak at the time of writing this, unfortunately. [EmuDeck](https://emudeck.com) doesn't support Slippi just yet either. So we have to do a manual process:
1. I transfered my ISO and [Slippi AppImage](https://github.com/project-slippi/Ishiiruka/releases) from my desktop rig to a USB drive. I then connected a USB-C dock to the Deck, connected the flash drive to one of the USB ports, went to Desktop Mode, and copied the files to the desktop. 
2. I made sure the AppImage was marked as executable by right-clicking the file -> Properties -> Permissions -> Checking the box for "Is executable."
3. Open Steam in Desktop Mode, add a non-Steam game from the lower-left corner, then locate the AppImage. From here you can add a custom icon and banner if you don't want the ordinary gray color.
4. Go to Gaming Mode on the Deck and launch Slippi from there. Set the ROM path to where your ISO is.
5. Configure the controls by tapping the arrow on the right side of the screen and going to "Controllers."
6. Under Port 1 set the controller to "Standard Controller" if you're using the Deck's built-in buttons, otherwise keep it on "GameCube Adapter for Wii U" if you have a Mayflash adapter connected. Now tap "Configure."
7. Under Device set it to "Microsoft X-Box 360 pad 0" if you're using built-in controls, then tap on each button to configure them
8. Configure the game to use 16:10 by going to the Graphics window, under the General tab. Also check the box for "Use Fullscreen." You may also want to uncheck "Show FPS" if you're using MangoHUD.
9. You may want to enable the widescreen hack. I haven't been able to do this in Game Mode; you'll have to go to Desktop Mode, right-click the game, go to Properties, then check the appropriate box under the Gecko Codes tab.
10. Launch the game, log in to your Slippi account, see how well things go.

Sorry if this process seems a little convoluted; I'm sure there's an easier process for this. If you're a Steam Deck owner and have some tips and tricks, definitely let me know.

Note that if you're looking to play *Melee* offline without the intent of playing against others, all you need to do is run the [EmuDeck script](https://www.emudeck.com/#download) and place the ISO in `/home/deck/Emulation/roms/gc/`. The game should now be available in Steam:

![melee on Steam](/images/steam_deck/photos/melee/melee_on_steam.jpg)

# Performance
I'm sure many of you are curious as to how well *Melee* runs on Deck. **It's 60 FPS with the default resolution scaling (2x/720p), for the most part.** There are occasional dips here and there. MangoHUD might report 60 FPS but the dip is certainly noticeable. That being said, I haven't had any disconnects with any of the opponents that I played against, even in doubles. They were still willing to play with me after a couple of rounds. They might have a different story to report on their side though; they may have experienced rollback or poor framerates.

Just do yourself and everyone else a favor: make sure your USB-C dock has an Ethernet port and play that way. (I really wish Valve had added an Ethernet jack to the motherboard.) Don't tell the people who I initially played with that I was using Wi-Fi. 

I tried using a couple of different flavors of *Melee* besides the vanilla ISO: I used [Animelee](https://www.animelee.xyz/) and [Diet Melee 64](https://diet.melee.tv/). For the most stability, I'd recommend going with the latter. Animelee definitely makes the game look nice though.

The fan is quiet as a mouse while playing. Then again, I have the Huaying fan, so the Delta fans may be a different story.

Now obviously, if you put a 30 FPS cap on the game, it will just play in slow motion. So even if you were looking to play offline, thinking that you can save yourself some battery life by cutting the framerate in half, don't do it. The game will play *horribly*.

# How do the Deck's Controls Feel?
The million-dollar question. Normally on my desktop I use a DualSense. But when it comes to fighting games and different gamepads, there's always a few days of adjustment to get used to. Getting used to the placement of the face buttons and the thumbsticks on the Deck certainly required some time.

After those few days had elapsed, I had no trouble with the controls. I'm able to easily L-cancel with the right trigger, and input smash attacks/aerial attacks with the right thumbstick. Wavedashing isn't that difficult to achieve either. Give me a few more days and I can probably play just as well on Deck as with my PS5 controller. I have configured the back buttons to use shield and grab, but I don't really make any use of them. I can't comment much on the D-pad either, since all I use that for is taunting (for humor, of course, such as if I KO my teammate by accident).

There are occasions where my palm accidentally presses against the right trackpad, which, by default with Steam Input, acts as the C-Stick. I inadvertently put in a back air attack when I might have planned on doing something else. It's not that big of a deal though, and I can easily disable the right trackpad by configuring the Steam Input. (The left trackpad mimics the D-pad by default.)

![diet melee on steam deck](/images/steam_deck/photos/melee/diet_melee.jpg)

I played this game in bed, and I will admit my hands started to feel numb after an hour or two of gameplay. That's because my arms are resting on the mattress. If I held the Deck up I probably wouldn't get that problem, but you have to keep in mind the Deck has it's weight to it, so you're probably going to feel discomfort no matter what after a few hours.

I should also note **the buttons and overall ergonomics of the Deck feel *way* better than the stock joycons on the Switch.** The face buttons aren't flat, the thumbsticks feel pretty decent and are larger, and there's analog triggers. The rounded grips on the left and right also help make the Deck feel better in my hands.

All of this being said, the Deck is a PC; if you want to use other gamepads, whether through Bluetooth or you have a Mayflash adapter for your wired GameCube controller, that's totally an option.

# Battery Life
Surprisingly I haven't noticed much of a difference in battery consumption between vanilla *Melee*, Animelee, and Diet Melee 64. They all consume from somewhere at 7 watts to a minimum, and 10 at most. Diet Melee, of course, is going to have the greatest benefit here, but even then it's only a watt or two difference than with Animelee.

If you're in training mode with one other CPU, it's going to consume 7-8 watts *without* a USB-C dock connected. With a dock connected, the Deck obviously needs to supply power to that, so it's going to use a few more watts (but like I said, you're going to want that dock connected so you can play via Ethernet). If you play online, however, especially with doubles, the wattage will increase to about 10. It shouldn't go any higher than that, even with a USB-C dock connected.

If we divide the Wh battery life of the Deck -- which is 40 Wh -- with these numbers, we can assume we'll get **4 hours at worst. I think it's safe to say you can probably squeeze 5, maybe even 6 hours of battery life.** Of course, this is all going to depend on whether Wi-Fi/Bluetooth is enabled or disabled, the screen brightness, etc. You could probably sneek in another half-hour or so by lowering the internal resolution (the graphics won't upscale when FSR is enabled, though).

# A Video...Soon to Come
I *really* wish I could record myself playing *Melee* on Deck, but I don't know what happened to my tripod and I currently have no decent way of showing the camera, other than using my hand. I ordered a new tripod and should be expecting it tomorrow or Thursday. That way, you can actually *see* what it's like playing *Melee* with an oversized Switch Pro. But once I get my tripod I'll definitely have some footage if you'd rather see this in action rather than just reading a large text post.

# Other Notes
I'm grateful for the Deck's slightly larger screen in contrast to my Switch (7" as opposed to 6.2"). But at times I still have difficulty seeing everyone on screen while playing doubles (I especially have this problem when playing *Smash Ultimate* on my Switch in portable mode). If you find the screen to be too small, just dock the Deck and connect an external monitor.

![Switch vs. Deck](/images/steam_deck/photos/melee/switch_vs_deck.jpg)

I've noticed Steam's on-screen keyboard randomly pops up while playing. Not sure what's causing that, and it's a nuisance. It only appears in the game's menus though.

**TL;DR**
- performance is decent for the most part, with *occasional* frame dips
- you generally shouldn't have too much of a problem playing online, provided you're using an Ethernet cable
- controls on Deck take a while to get used to but I don't have much of a problem with them now
- 4-6 hours of estimated battery life
- use a USB-C dock for Ethernet (and optionally for connecting an external monitor)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
