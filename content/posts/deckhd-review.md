+++
title = "DeckHD - A Wonderful Screen Upgrade for your Steam Deck"
date = 2023-12-29T16:17:22Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/accessories/deckhd/cover.jpg"
tags = ["hardware review", "deckhd", "steam deck", "steam deck lcd"]
keywords = ["deckhd", "steam deck"]
description = "The color quality is nice - but is the resolution upgrade worth it?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A little over a month ago the folks at FX Technology Limited shipped the DeckHD. Set at the same price as the anti-glare coated Steam Deck screen over on iFixit ($100), this DIY screen upgrade multiplies the Steam Deck's native 800p resolution by one-and-a-half times, to 1920 x 1200. It also increases the color gamut (or sRGB coverage) from 67% to 87%, making the colors -- at least from my point of view -- come pretty close to that of the Deck OLED. The [official website](https://www.deckhd.com/) also advertises that it has improved touch panel responsiveness and less flicker at 40 Hz.

While it was pretty ironic that they shipped the screens right around the same time as the Deck OLED, at first I thought it was bad timing. But then I thought about it. A stock LCD 64 GB Steam Deck currently costs $350 on Steam. You get this screen for $100, you're still saving $100 at the end of the day versus buying the lowest-tier OLED, which is $550. You get close to the same color quality, a higher resolution, and support for [overclocking](https://linuxgamingcentral.com/posts/overclock-lcd-steam-deck-guide/) on older firmware. You just won't get the better battery life, storage size, or other QoL improvements on the OLED.

# Installation
The DeckHD is a DIY screen upgrade for the Steam Deck LCD model. The black box that you get is quite nice and minimalistic. The contents of the box, aside from the screen itself, is a suction cup (for taking the old screen out), a couple of picks (to get underneath the bezels), a pair of tweezers (for disconnecting the ribbon cables), adhesive strips (for keeping the new screen in place), a Phillips screwdriver, a pointy stick (for getting rid of the guck from the old adhesion), a spudger, and a ribbon cable for connecting the DeckHD to the mobo. Foam keeps the screen intact while it ships.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/deckhd/installing.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

The install process is basically as follows:
- (optional but recommended) discharge your Deck to 25% or below, to prevent the battery from exploding if it gets accidentally punctured
- (optional) put the Deck into battery storage mode via the BIOS to prevent it from turning on when you press the Power button
- remove any MicroSD cards that may be inserted to prevent it from being split when you take the back shell off
- unscrew the screws to the back shell and take it off
- unscrew the screws to the heat shield and take it off
- disconnect the battery cable and the ribbon cable going into the motherboard
- unscrew the screws holding the mobo in
- gently lift the mobo up and disconnect the ribbon cable for the display
- turn the Deck around, apply some heat to the bezels of the screen, then gently pry out the screen with the provided suction cup
- apply adhesive strips to the edges where the screen will go
- put the screen on, making sure it's at the right angle
- turn the Deck back around, lift the mobo, and connect the new display cable from the display to the mobo

Then follow these steps in reverse to put the Deck back together. You can see my installation video on [YouTube](https://www.youtube.com/watch?v=TvbjmaoMMRs).

Unlike the [official setup guide](https://www.deckhd.com/installing-deckhd), you don't actually have to take out the SSD, heatsink, fan cable, speaker cable, Wi-Fi connectors, or the ribbon cable for the daughterboard. Taking all of these out will make it easier to access the display cable, but it's a lot more work.

I'd say the only difficult part of the installation process is not knowing how long you should apply the heat to the bezels. I think I had to stand there for 10 minutes, constantly moving the hair dryer from bezel to bezel, before I could finally take out the screen. Guess I need some better equipment to get a better idea of how long I should apply the heat.

# Flash BIOS
Since the DeckHD comes with an upgraded resolution, it won't work out-of-the-box when you turn it on. Per the [setup guide](https://www.deckhd.com/flashing-bios):
> Since the DeckHD display is a completely custom device for the Steam Deck, we need to customise the original BIOS to include the correct display initialisation commands and to let the OS know that we’re booting up with a 1200p display instead of the default 800p. This will ensure compatibility between the computer and the display. Please rest assured, all changes made in our custom BIOS are purely on the Analogix MIPI Receiver's configuration side, and we do not tinker with any other components that can affect the stability of the Steam Deck.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/deckhd/turning_it_on_for_the_first_time.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

While at first closed-source, the BIOS Maker is now available on [GitHub](https://github.com/DeckHD/BiosMaker).

For the time being, any time Valve ships out a new firmware update for the Deck, users will need to re-flash their BIOS in order to make proper use of the DeckHD. If you downgrade your firmware for overclocking purposes, you'll need to re-run the flashing script again there too. Hopefully Valve will ship a FW update in the future that includes native support for the DeckHD.

So, you'll have to head into Desktop Mode with the tiny part of the screen that actually works on the lower-left corner, download their flashing script, open it, enter your sudo password, and the flashing will proceed from there. It shouldn't take long. Then the Deck will restart, and hopefully, you'll be able to make use of the entire screen from that point forward.

From there you can adjust the [Steam Deck UI scale](https://www.deckhd.com/changing-steamdeck-display-scaling), since the icons in Steam will be a little smaller now. I haven't personally seen the need to do this but it's good to know for those who may have to squint a little bit to read the text.

They actually managed to modify the splash screen when you first turn the Deck on to their own logo. It's quite nice.

![DeckHD splash screen](/images/steam_deck/accessories/deckhd/logo.jpg)

# Nice Colors
As soon as I turned my Deck on with the DeckHD, even before flashing the BIOS, I noticed the color difference. And holy crap, it looks *a lot* better than the stock LCD screen. My phone camera just will *not* be able to do it justice here. It's one of those things that you'll have to see for yourself in person to notice the difference. Like I had mentioned before, the color quality comes close to that of my limited edition OLED model.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/deckhd/hzd_comparison.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Higher Resolution
While having a higher resolution is nice, the problem is, the Deck has a hard enough time as it is playing some of the more demanding titles out there. A higher resolution is only going to decrease the performance while also increasing the rate at which the battery is consumed. Macho Nacho Productions made a [video](https://www.youtube.com/watch?v=X4ct6K5I744) not too long ago comparing the performance of *Cyberpunk 2077* and *Shadow of the Tomb Raider*. At 800p, *Cyberpunk 2077* was running at a solid 30 FPS during benchmarking. At 1200p, that framerate went down to around 24-25 FPS. *Shadow of the Tomb Raider* was running at a solid 60 FPS at 800p, but tanked to 40-45 FPS at 1200p.

Running some of my own benchmarks with *Horizon Zero Dawn*, I've noticed the game takes an eight FPS dip while running with Ultra quality settings, going from 29 FPS at 800p on average to 21 at 1200p. Although, interestingly enough from both tests it seems like the power draw was 30 W during benchmarking.

![HZD - benchmark at 1200p vs. 800p](/images/steam_deck/accessories/deckhd/hzd_comparison.jpg)

I guess it's a good thing that we have upscalers like FSR and NIS, to lower the in-game resolution while still reaping the benefits of a 1200p display. Overclocking definitely comes in handy as well.

One thing that is a bit of a PITA, is that you'll have to manually set the resolution to 1920 x 1200 for *each* game in Steam in order to use the DeckHD's higher resolution. I know I'm not the only one who has complained about this. Let's just hope Valve does something about this in the future so that we can set the resolution on a *global* basis as opposed to per-game. (Fun fact: ChimeraOS already has this feature, unlike SteamOS.)

![Setting resolution with Ratchet & Clank](/images/steam_deck/accessories/deckhd/setting_resolution.jpg)

# Less Flicker and Improved Touch Responsiveness?
Supposedly there's less flicker on the DeckHD when you run a game at 40 Hz. The only thing I have going for this test is my video. But since the phone only captures at 30 FPS, I'm not even sure if it's possible to notice the difference. Now that my DeckHD is installed, I don't have a stock LCD Deck to compare with. Neither can I comment on whether the touch panel responsiveness has been improved. In my search for other DeckHD reviews, none that I've seen so far talk about either of these subjects. DeckHD has a [video](https://www.youtube.com/watch?v=N7StBdfHYpo) comparing the DeckHD with a stock LCD screen at 40 Hz. But since the video is from them, take the results with a grain of salt.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/deckhd/40hz_comparison.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I will say this though: when playing a game at 40 Hz with the DeckHD, I haven't personally found any significant difference from my naked eye as far as flicky-ness.

# Same Price, Better Features
The DeckHD is a fun DIY upgrade that costs the same as the 512 GB anti-glare screen on iFixit at $100. It still has the anti-glare coating, has better color quality, and a higher resolution. Supposedly there's also "improved touch panel responsiveness" and "flicker-free image on all refresh rates" but I am unable to confirm these at the moment. The increased color range in of itself is worth getting the upgrade for.

Only gripes are as follows:
- you need to run their flashing script every time Valve ships a FW update, or if you downgrade the FW yourself, in order to make use of the entire screen
- the resolution needs to get set on a per-game basis

Valve has probably heard the complaints already. Just gonna have to wait on Valve Time and see whether or not they'll actually do something about it.

Some might even view the increased resolution as a downside, since it's going to have a performance hit in demanding games. I will argue though that users can just set the in-game resolution to something lower than the native res while making use of Gamescope's FSR/NIS scaling techniques. Overclocking on the LCD models is also an option.

**TL;DR**

The good:
- same price as 512 GB anti-glare screen on iFixit
- much better color quality
- higher resolution
- a fun DIY upgrade

The not-so-good:
- flashing script needs to get run after installation, and needs to be re-run any time Valve ships a FW update
- resolution needs to get set on a per-game basis in the game's properties menu in Steam

You can buy the DeckHD on the [official website](https://www.deckhd.com/) for $100.

*Review sample sent courtesy of the folks at DeckHD.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
