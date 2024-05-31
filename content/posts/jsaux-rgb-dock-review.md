+++
title = "JSAUX RGB Docking Station Review"
date = 2023-10-12T14:58:08Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/accessories/rgb_dock/cover.jpg"
tags = ["hardware review", "accessory review", "steam deck", "jsaux", "docking station"]
keywords = ["jsaux rgb docking station", "steam deck docking station", "usb c dock", "rgb dock", "jsaux", "steam deck"]
description = "Pretty lights can come at the expense of build quality."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A little bit of a backstory regarding this dock: about a year ago, JSAUX was in the process of adding a layer of RGB lights to their 6-in-1 docking station. A rival company had access to their plans, and they started making their own docks with the same idea in mind. Per JSAUX's [blog post](https://jsaux.com/blogs/steam-deck/statement-on-product-leaks-and-the-new-rgb-dock):
> This product was completely developed by our team JSAUX, and we put a lot of work into it. It is difficult for us to accept that the factory leaked our development program to another company. The rival company managed to sell this product in their logo but using our product solution. It is an outrage given how many efforts our R&D personnel cost and how long our fans are waiting.

JSAUX "terminated the cooperation with that factory" and "abandoned the mold," but said they'd come back with a completely new idea. That idea came to fruition by means of the very dock they sent to me a few weeks ago.

# Model Differences
When you're on JSAUX's website, you'll see two different models of this dock. One is an 8-in-1 and the other is 12-in-1. The 8-in-1 is priced at **$60** and comes with the following:
- HDMI port (4K @ 60 Hz)
- two USB type A 3.0 ports (5 Gbps)
- one USB type A 2.0 port (480 Mbps)
- gigabit Ethernet port
- three USB-C ports (5 Gbps), one of which is dedicated to PD

![12-in-1 ports](/images/steam_deck/accessories/rgb_dock/ports.jpg)

The 12-in-1, as you might have guessed, adds more ports to the dock, while also upgrading the refresh rate capability and the speed of the USB ports. In addition to the ports of the 8-in-1, it also adds a DisplayPort (4K @ 120 Hz), a 3.5mm headphone jack, a full-size SD card reader (480 Mbps), and a MicroSD card reader (480 Mbps). The HDMI port refresh rate gets doubled to support 120 Hz, and the USB 3.0 ports get upgraded to 3.2 with double the transfer rate at 10 Gbps. The Ethernet port gets moved to the side of the dock rather than in the back. The 12-in-1 is priced at **$90**.

JSAUX sent me the 12-in-1.

# Box Contents
Inside the box, besides the dock itself, is:
- product overview manual
- warranty manual
- stickers to put on top of the dock
- USB-C to USB-C cable for connecting the dock to whatever device you want to use

I'm not sure why the stickers don't come pre-applied. I guess they wanted to give you the choice whether or not you want to add a red accent to the dock. I definitely did so, because, if you couldn't tell from the colors of this website, I dig black and red.

![RGB dock contents](/images/steam_deck/accessories/rgb_dock/contents.jpg)

The picture on the box could have used a little more work. It's telling me the specs of the 8-in-1 rather than the 12-in-1.

# First Impressions - Not Great
Frankly I didn't have a great out-of-the-box experience. For starters, the stand for putting in your Deck or other handheld. You push this in with your thumb, and a plastic tray comes out to which you can place your Deck. This stand feels flimsy and cheap. And there's no sort of mechanism to keep the Deck in place. It would have been fine had this side of the dock been flat, but since the edges are angled, you can't really keep your device secure. Lastly, when you put your Deck on the stand, it will cause the dock to lean up a little bit, since the weight of the Deck outweighs the dock. There should have been some counterweight added inside the dock to keep itself from getting tipped.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_dock/dock_stand.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Next is the USB-C cable suppied. While it's great that they made the connection detachable, you may want to look into using a different one than the one provided. The end of the cable that connects to the Deck is shaped in a way that goes sideways. You either have to block access to the power button, or turn it the other way and have some of the vent holes partially covered from the cable. Not a great choice. It would have been better had this end of the cable be a 90-degree connector and not get in the way of anything.

Third, your Deck is going to get in the way of the RGBs. Since the Deck goes in front of the dock, the LEDs get partially hindered. It kind of defeats the whole purpose of getting a dock with RGBs. One workaround that I found is turning the dock around and putting the Deck in reverse. This way the RGBs are fully exposed and I have easy access to all the ports in front. But now I've got two problems:
1. I need to lean the Deck against my fridge so it doesn't fall over, as you can see from the cover photo.
2. The supplied USB-C cable isn't long enough to go around to the back of the Deck, so now the cable looks weird, if that makes sense.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_dock/usb_c_cable.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Pay Attention to Resolution and Refresh Rate Support
I never paid attention to the numbers as far as resolution and refresh rate that docks support until now. Because, what happened when I connected the DisplayPort to my 1440p, 165 Hz monitor, nothing showed up on the screen. At first, I thought the DisplayPort was faulty. After doing a little bit of troubleshooting, I could finally get the display working after forcing the Deck to use a safe resolution when connected to an external monitor. From there I gradually upped the resolution until it stopped working again. Turns out the DisplayPort doesn't support 165 Hz. After setting the resolution to 1440p, 144 Hz, I was good to go.

I had a similar issue with HDMI. No OOTB support for my monitor because the refresh rate is not supported. I ended up getting a light blue screen with no sound, and when HDR was enabled, the screen was constantly flickering. I had to downsample the refresh rate in Steam's display settings to 120 Hz.

![Setting lower refresh rate in Game Mode](/images/steam_deck/accessories/rgb_dock/resolution.jpg)

So, when you're looking at a dock to purchase, pay attention to those numbers. If you have a monitor that has a higher resolution or refresh rate than what the dock supports, you will have to downsample them until your display is working.

The thing is, this can be a bit cumbersome. So while my workaround worked in Game Mode, it didn't in Desktop Mode. When I connected the DisplayPort, I got nothing. As far as I can tell, there's no way to tell Plasma to support a lower refresh rate *prior* to connecting the external display. So I'm kind of stuck there. I got the same light blue screen with HDMI as I did with Game Mode, but I could still lower the refresh rate in Plasma's settings and get proper HDMI support. I'm probably making your head spin at this point as I'm trying my best to explain this situation.

# RGBs
RGBs are great, right? And I won't lie; they do look nice on this dock. A LED strip is placed on the bottom of the dock and encircles the entire station. By default these RGBs move around in a circle. If you want to turn the LEDs off, just hold the button down in the center of the dock for about one second. To turn it back on, do the same thing.

Unlike the RGB backplate, you can customize the behavior of the RGBs of the docking station with OpenRGB. Upon opening the application up for the first time on Steam Deck in Desktop Mode, you'll get a warning saying that udev rules aren't installed. No need to worry; installing udev rules aren't necessary for this docking station.

OpenRGB should automatically pick up the docking station. From here you can customize the RGB colors and patterns. I'm not going to go over every mode, as there's quite a few different options available, but there's this mode called "Stacking" which will gradually fill the LED strip with a solid color until the entire strip is lit up. After that it will reset and move on to a different color. You can control how fast or how slow the pattern moves, and whether you want the colors to move to the left or to the right.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/rgb_dock/rgbs.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

If you want you can also just have a solid LED that has no behavior. Whatever color you want, OpenRGB probably has it. A neat thing is you can apply colors on a side-by-side basis. So, if you wanted red on one side of the dock, and blue on the other, that's totally possible. Modes like this also allow you to control how bright each LED is.

Do note that, once you've disconnected the dock, the LEDs will reset. You will need to save a profile on OpenRGB with the settings that you want, then apply this every time you re-connect the dock.

# Not the Best Dock Out There
I'm kind of wondering since this dock is advertised for multiple handhelds, rather than just the Steam Deck itself, that that took some of the quality away. JSAUX makes some *excellent* Deck accessories, but this is one of those few times where I was left a little disappointed, particularly the build quality. The stand for the Deck is cheap and flimsy, the dock leans over when the Deck is placed in said stand, there's not really a secure way of keeping the Deck in place, the way the dock is designed hinders the RGBs somewhat when the Deck is put in, the USB-C cable supplied gets in the way of the power button.

I mean, I was able to type this review on my Deck with this dock. All of the ports work as expected. Customizable RGBs are a plus. But just be mindful that your monitor *may* have a refresh rate that's higher than what this dock supports, and you may be in for a struggle trying to figure out how to lower the refresh rate. Particularly with Desktop Mode.

![RGBs with lights off](/images/steam_deck/accessories/rgb_dock/lights_off.jpg)

I had no issues with the [JSAUX dock for the ModCase](https://linuxgamingcentral.com/posts/jsaux-power-bank-and-steam-deck-dock-review/). I had great OOTB support for that, including the refresh rate support, and a nice bonus with that dock is I can just slide that dock in with my ModCase and take it with me wherever I go. That may be a better choice for now, and it's $30 cheaper than the RGB 12-in-1, while still retaining many of the same ports. Really, the only thing you'd be missing at that point is the RGBs. So, that's up to you. I personally don't think it's worth spending the extra money just to have the RGBs.

**TL;DR**

The good:
- RGBs that can be customized via open-source software
- detachable USB-C cable
- plenty of ports with the 12-in-1
- a cheaper version of the dock is available should you not need so many ports

The not-so-good:
- cheap stand
- dock leans over when a device is put into the stand
- supplied USB-C cable will either block the power button on the Deck or one of the vent holes
- RGBs are hindered when the Deck is placed on the stand
- may need to force safe mode when an external monitor is connected, depending on what resolution/refresh rate your monitor supports

The JSAUX RGB docking station is [available](https://jsaux.com/products/rgb-docking-station-for-steam-deck) as an 8-in-1 or a 12-in-1, priced at $60 and $90 respectively.

Thanks to JSAUX for sending this over for review.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
