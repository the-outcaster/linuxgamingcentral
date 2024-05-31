+++
title = "JSAUX RGB Backplate for Steam Deck - Review"
date = 2023-10-10T18:56:08Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/accessories/rgb_backplate/cover.jpg"
tags = ["steam deck", "accessory review", "hardware review", "jsaux", "backplate"]
keywords = ["steam deck accessories", "steam deck", "jsaux backplate", "steam deck backplate", "steam deck rgb"]
description = "Is the backplate worth upgrading for the RGBs?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
JSAUX makes some *excellent* Steam Deck accessories. I'd argue that they're the ones who are the *king* when it comes to accessorizing the Deck.

However, just because you're getting the RGB lights, doesn't necessarily mean they're worth getting.

**Installation and demonstration video available on [YouTube](https://youtu.be/9O93uI4FhvQ).**

# Box Contents
This is the latest backplate from JSAUX. It has RGB lighting. And for some reason, they include these rubber grips that go on both ends of the Deck. There's also:
- a set of custom back buttons
- a Philips screwdriver for taking the back screws off
- a pick
- a spudger
- five short screws (for the inner screws for the backplate)
- five longer screws (for the outer screws)
- eight screws for securing the back buttons in place
- those condom-like finger gloves
- USB-C cable for charging the LEDs
- a warranty booklet
- a booklet containing instructions on how to replace the back shell

![Box contents](/images/steam_deck/accessories/rgb_backplate/contents.jpg)

It's nice that they provide some extra screws. I had lost a few of mine after my cat scattered them across the floor, so the screws that were supplied came in handy.

# Installation
Installation is very easy. First, make sure your Deck is off. Second, remove any MicroSD cards if they're in. Third, remove the screws from the backplate with the provided screwdriver. Pry it off with the pick or the spudger if you need to. Remove the plastic covering the thermal paste. Put the new backplate on, securing it with the screws provided or the ones you have from the original backplate. Done.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_backplate/installation.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

If you want, as with other JSAUX backplates, you can replace the back buttons with a different set. The ones pre-installed are the stock back buttons that are very similar to the back buttons on the vanilla backplate. Two sets of back buttons are provided -- one that's slightly higher, and one that's even higher. Installing these is as simple as unscrewing the screws housing the RGB PCB, putting it out of the way, putting the new back buttons on, then securing it back in with the screwdriver. 

If you want you can even use one set of the high buttons and one set of medium buttons at the same time, since the buttons are separate. The stock buttons, however, *aren't* separate for some reason. You can easily split them with a pair of scissors though. This will allow even further customization, and allow you to decide whether you like the medium buttons or the high set.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_backplate/back_buttons.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Cooler Temperature and Lower Fan Speed
The backplate -- similar to the purple one I received some time ago -- has an updated thermal design. Thermal paste gets put over the heat shield. If you want, you can apply some heat to this with a hair dryer, but I haven't found this to be necessary. There's also a vent towards the center, right where the fan exhaust is. It's a little off-center to where the fan is located, but center in conjunction with the inner screws, if that makes sense. In any case, the vent is still large enough to have an opening for the fan.

I've been reading some other reviews of this backplate, and they noted that the fan doesn't run anywhere near as fast as compared to the original backplate. They also noted the fan is much more quiet. To see if their claims were true, I ran [*Witchfire*](https://linuxgamingcentral.com/posts/witchfire-review/) on Medium settings for about 10 minutes. Here are the stats with the original backplate:

![Fan speed with OG backplate](/images/steam_deck/accessories/rgb_backplate/fan_with_og_backplate.jpg)

And here are the stats with the same game, same area, same settings, with the RGB backplate:

![Fan speed with RGB backplate](/images/steam_deck/accessories/rgb_backplate/fan_with_rgb_backplate.jpg)

It's pretty close to a 1,500 RPM difference. Since I have the Huaying fan, I don't really notice the noise with the orignial backplate, but for those of you who have the Delta fan, you probably are going to notice a pretty big difference in the noise. You might have also noticed both the CPU and GPU are running a whole 10 degrees Celcius cooler with the RGB backplate. So yeah, a quieter fan and a cooler APU are definitely a big plus.

# Easily See the Internals
The crystal clear plastic allows you to easily see your Deck's internals. I can definitely see the internals a lot more clearly than I can with the purple shell. But now the clear shell obviously doesn't match up with the purple front. I'm wondering if I can transfer the PCBs from the clear shell onto the purple shell. Then just cut out a hole for the button and the USB-C port. That way, I can have the RGBs while still retaining an all-purple look. Probably wouldn't be that difficult of a task.

# RGBs
Towards the top-right of the backplate, right above the battery and where the PCB for the volume buttons/headphone jack is, is a button and a USB-C port. Holding the button down for roughly one second will turn the lights on. Holding the button down again will turn them off. The LEDs will emanate from the left and right where the grips are. Pressing the button again will switch between colors or patterns.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_backplate/rgbs.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Available colors/patterns are:
- breathing red
- breathing green
- breathing blue
- breathing purple
- a pattern that breathes between a variety of different colors, including white, yellow, and cyan
- a solid pattern that doesn't change brightness but changes color in a vertical pattern

The LEDs can be charged via the USB-C port. According to JSAUX, charging the LEDs takes about two hours, and the battery expectancy is also two hours. A little red LED lights up underneath the headphone jack to indicate it's charging. It will turn green when charging is complete. 

The charging mechanism is a little clumsy. Unless you have an available kickstand, you sort of need to have the Deck laying down on its face in order to charge the LEDs, or lean it against a wall. I would have preferred the USB-C port to be somewhere on the side where the grips are, but to be honest I'm not even sure if that's possible with how the PCBs are designed.

![Charging the LEDs](/images/steam_deck/accessories/rgb_backplate/charging.jpg)

That's about it as far as RGBs. You can't control the brightness, how fast or how slow the LEDs breathe, or how the glowing patterns work. You also don't know how much longer it's going to take for the LEDs to charge, or how much juice they have left before they suddenly turn off. And frankly I found the RGBs to be a little too bright with the lights off in my room. I'm wondering if it is somehow possible to control the RGB behavior with OpenRGB.

# Rubber Grips - Why?
Then you have the rubber grips. To me, this was an odd inclusion. The gray color -- which, for some reason, is pictured as black on the box -- is an ugly color contrast with the purple front that I have. And the Steam and QAM are quite large. I mean, if the front of my Deck was clear, the gray color would be a good fit. And I suppose the grips give the Deck some protection should it drop. But it was just an odd addition to the shell. You can still see the LEDs with these grips on, but obviously the color is hindered somewhat. Besides, I still have the [ModCase](https://linuxgamingcentral.com/posts/jsaux-modcase-for-steam-deck-review/) for keeping the Deck protected, and the black is a much better contrast than the gray.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_backplate/grips.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Just Get A Regular Transparent Backplate
The RGBs are nice. They'll definitely help light up the room if it's dark. But I don't think it's worth the extra $10 for the RGB LEDs and the grips. The grips, to me, just don't make sense, and with the purple front shell, the color contrast is ugly, and the LEDs are partially covered. I also find the LEDs to be too bright in the dark with the grips off, and the lack of customization as far as how bright these can get is a bit of a downer. You also have no way of knowing when the LEDs will suddenly shut off when they lose battery.

If JSAUX decides to make an updated backplate, I'd like the following:
- have the ability to customize the brightness and color patterns with something like OpenRGB, just like their RGB dock, while also being able to monitor the battery life
- put the charging port in a place where it's not going to be awkward, such as the side, so you don't have to lay the Deck down if you don't have a kickstand
- make a purple edition of the RGB backplate, so that the color matches with the front. Better yet, offer a DIY kit so anyone can do it for any backplate
- don't include the grips. Make it an optional accessory, and have them available in different colors
- have the stock back buttons separated

**TL;DR**

The good:
- pretty RGBs!
- clear shell allows you to easily see the Deck's hardware
- thermal grease and vent hole allows the Deck to run at a cooler temperature
- customizable back buttons that are easy to install
- everything is included to get you to easily install the backplate, including a screwdriver, a pick, and extra screws

The not-so-good:
- rubber grips are unneccesary and an ugly color contrast to my purple front plate, while also hindering the LEDs somewhat
- RGBs can't be customized as far as their brightness, how fast or how slow they breathe, etc.
- RGB battery can't be monitored
- awkward placement of the USB-C port
- RGBs are a little too bright in the dark

The RGB backplate is available on [JSAUX's website](https://jsaux.com/products/transparent-back-plate-for-steam-deck-pc0106-rgb-vents?variant=44007924203740) for $40.

Thanks to JSAUX for sending this over.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
