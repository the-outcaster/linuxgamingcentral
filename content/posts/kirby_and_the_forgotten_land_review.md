+++
title = "Kirby and the Forgotten Land: An Unforgotten Experience"
date = 2022-03-25T10:32:50-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/kirby_review/cover.jpg"
tags = ["game review", "switch", "emulation"]
keywords = ["ryujinx", "kirby"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Time to shake things up a bit and talk about a Nintendo Switch game: *Kirby and the Forgotten Land*. If you prefer Linux-exclusive news, just let me know in the comments. But do note I played the entirety of this game on Linux, thanks to [Ryujinx](https://ryujinx.org).

Haven't played a Kirby game in a long time. I think the last one I played was *Kirby Air Ride* for the GameCube. Something struck out to me when I was watching the trailer for this game though. I think it has to do with the vibrant color, rich graphical detail, and...well, this is Kirby's first game where he *isn't* in a side-scroller. A fully 3D environment in which the pink marshmellow can move around in. According to the developers, it took them [over *20 years*](https://www.nintendo.co.uk/News/2022/March/Ask-the-Developer-Vol-4-Kirby-and-the-Forgotten-Land-2187039.html) to successfully transition Kirby into the 3D landscape. 

But the effort definitely paid off.

So, just a little trivia about Kirby before I move on. In case you're not aware, Kirby was created by Masahiro Sakurai at the age of 19. Sakurai is also director of the *Super Smash Bros.* series. Kirby was named after the lawyer who helped Nintendo win the [court case against Universal City Studios](https://en.wikipedia.org/wiki/Universal_City_Studios,_Inc._v._Nintendo_Co.,_Ltd.) in 1984, the latter of which claimed that *Donkey Kong* was an trademark infringement of *King Kong*. Kirby has been around since '92 with *Kirby's Dream Land* for the Game Boy.

![kirby about to get grabbed by an ape](/images/kirby_review/ape.jpg)

Kirby makes his way across plenty of different areas, including a desert, a snowy biome, a lush forest, among others. Each stage has a plethora of enemies and objects that can be inhaled. Kirby's goal is to make it to the end of the stage while rescuing as many Waddle Dees as possible. A certain number of them are required in order to proceed to the final stage and boss of each area. There will be three-to-five Waddle Dees hidden in a cage somewhere in the stage. Touching the cage will set the Waddle Dee free. Additional Waddle Dees can be rescued by discovering secret areas, walking past a certain type of flower, defeating a boss without taking damage, among other circumstances.

The more Waddle Dees are saved, the more workshops open up in the Arrival area. Such workshops will allow Kirby to upgrade his abilities, participate in boss tournaments, buy food items to go, watch previously played cinematics, and lots more. 

If you have played a Kirby game before, you'll likely be familiar with Kirby's abilities, depending on who he inhales. The swordsman returns, as well as the snowman, the bomb thrower, you get the idea. Some enemies don't offer abilities when inhaled, but Kirby can instead spit the enemy out like a projectile. There's exactly one dozen different abilities total. These abilities can be upgraded later on by finding the appropriate blueprint, then spending coins and a few rare stones. As an example, the sword ability upgrade will extend the reach of the sword, allow it to be charged for a stronger attack, and adds one additional attack to the standard combo. Very useful to do, because you will find yourself repeating the same courses over and the upgraded ability will come in handy.

![kirby about to throw a bomb](/images/kirby_review/battle.jpg)

What's new to the Kirby formula this time, is Mouthful mode. If you had a fetish for a really fat Kirby, well, your desires have been granted here. Kirby can inhale an entire car, a cone, a lightbulb, a fan...heck, he can swallow an entire staircase. Inhaling these objects allows even more unique abilities than the enemies. The water mode allows Kirby to spit out water, similar to how FLUDD works in *Super Mario Sunshine*. The cone allows him to bust through a partially-cracked floor. The lightbulb allows him to see in the dark. All these modes further increase the strategy mechanic in order to move on to the next part of the stage. It's both brilliant and disturbing at the same time. (If Kirby can inhale an 18-wheeler, I don't understand why he can't inhale an ape the size of King Kong.)

Combat isn't that bad. A lot of enemies can be defeated by simply mashing the attack button, and they'll flinch and won't have enough time to counter-attack. Kirby does have a guarding and rolling mechanic though if in case he picks a fight with a tougher enemy. Rolling just before an attack strikes puts the game in slow motion. Kirby can more quickly charge an attack during this phase, making counter-attacks more intuitive. Even in Wild Mode (the tougher difficulty level in this game), the game honestly doesn't present much of a challenge. Kirby kicks the socks out of his opponents like it's nothing. Even bosses can be defeated pretty quickly once you become familiar with their attack patterns. I still enjoyed the game though, and some people prefer a more "story-like" difficulty anyway.

Unlocking the stones for ability upgrades can be a bit annoying. It requires accessing a special stage on the map, then clearing said stage within a time limit using one of Kirby's abilities. This is very frequent and I wish the developers had toned this down a bit.

![kirby in cone mode on special stage](/images/kirby_review/cone_mode.jpg)

Music is pretty good, for what it's worth. It strikes a decent balance between gentle, relaxing tunes and more hardcore tones depending on what stage Kirby is in.

Game length is roughly ten hours. But that can definitely add up. You probably won't rescue all the Waddle Dees on your first run on a stage, so there's replayability there. There's also a Boss Rush mode and some other goodies that I don't want to spoil.

# How Does it Ryujinx?
The Switch can't get the framerate any higher than 30 FPS. Objects in the distance will have a choppy framerate, then move normally once in range. It's kind of expected for a device using a seven-year-old chipset. That being said, fortunately someone made a [60 FPS patch](https://cdn.discordapp.com/attachments/835681932703563826/956590597085487154/KFL_60FPS.7z) that remedies the headache you might get with 30 FPS. (I don't know who made the mod; let me know who you are so I can credit you.) But even on my GTX 1660 Super with threaded optimization and [GameMode](https://github.com/FeralInteractive/gamemode), there are some busy areas that just can't reach 60 FPS. Areas with a lot of enemies can be a painfully slow 20 FPS. If you were on AMD or Intel, you could use [GameScope](https://github.com/Plagman/gamescope) and enable FSR, but sadly that's not an option on NVIDIA. Well, [not yet](https://www.gamingonlinux.com/2022/03/nvidia-working-with-valve-to-get-gamescope-working-on-their-drivers/) anyway.

I recorded some gameplay footage here at 1440p resolution. I wasn't aware of the 60 FPS patch at the time of recording though, so unfortunately it's at 30 FPS.

{{< youtube "R0Lrr74saG4" >}}

**TL;DR**

The good:
- Good graphics quality
- Rich color
- Decent soundtrack
- Good controls
- Interesting story

The not-so-good:
- Poor framerate
- Easy difficulty
- Repetitive special stages

![kirby in mouthful stair case mode](/images/kirby_review/stair_mode.jpg)

*Kirby and the Forgotten Land* is pretty great. The color, lighting, and graphical detail is amazing, the controls are fluent, the combat is easy but fun, and there's plenty to do in the story mode. Good game to pick up if you want a fun and relaxing experience.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
