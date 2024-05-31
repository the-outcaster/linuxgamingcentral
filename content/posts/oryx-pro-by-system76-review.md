+++
title = "Oryx Pro by System76 -- A Great Gaming Laptop"
date = 2022-09-15T16:23:34-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/system76/oryx_pro/review/cover.jpg"
tags = ["hardware review", "system76", "laptop", "oryx pro"]
keywords = ["system76", "oryx pro"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Oryx Pro is a laptop from System76 that features an Alder Lake processor and a powerful RTX 30-series GPU. Per my conversation with [Adam Balla](https://blog.system76.com/post/647907158482092032/system76-spotlight-with-adam-balla), media relations manager at System76, all of System76's laptops are named after African fauna. In this particular case, the Oryx Pro is named after the antelope, which, according to the [African Wildlife Foundation](https://www.awf.org/wildlife-conservation/oryx), "are a true desert animal, with a thick, horse-like neck; a short mane; and a compact, muscular body."

I can see why they named this laptop after the animal. It's compact, and it's "muscular" when it comes to powerful hardware. The "Pro" comes afterwards, not because it's the successor to a previous model, but rather it's one of System76's higher-tier models, aimed towards professionals. Not only is it great for gaming, but it's also useful for AI or machine learning. I played and wrote my review of [*Destroy All Humans! 2 - Reprobed*](https://linuxgamingcentral.com/posts/destroy-all-humans-2-reprobed-review/) with this.

The Oryx Pro comes loaded with the company's Pop!_OS distribution, utilizing Ubuntu as it's base while retaining cutting-edge software. It also incorporates [Coreboot](https://github.com/system76/coreboot), an open-source alternative to the proprietary BIOS that are in many computers today. Here's my thoughts after two weeks of use.

# Specs
In case you're not familiar with how System76's shopping experience works, when selecting a hardware product, you can customize the hardware in it. For example, with the Oryx Pro, I can choose what GPU I want in it, the screen size, as well as the amount of RAM and storage.

![Oryx Pro box contents](/images/system76/oryx_pro/review/contents.jpg)

The Oryx Pro at minimum specs -- at the time of writing this -- is **$1,899** and comes with the following:
- RTX 3070 Ti (8 GB VRAM)
- 15.6", 144 Hz, 1080p screen
- i7-12700H (4.7 GHz, 14 cores/20 threads)
- 8 GB DDR4 RAM clocked at 3,200 MHz
- 240 GB PCIe Gen3 storage, with a read and write speed of 2,400/900 MBs

At fully maximized specs, the laptop will cost **$4,100** and will have:
- RTX 3080 Ti (16 GB VRAM)
- 17.3", 144 Hz, 1080p screen
- i7-12700H
- 64 GB DDR4, clocked at 3,200 MHz
- 4 TB of PCIe Gen4 storage, with a read and write speed of 7,000/5,100 MBs

My configuration came at **$3,477** with the following:
- RTX 3080 Ti
- 17.3" screen
- i7-12700H
- 32 GB DDR4
- 2 TB PCIe Gen4

![Oryx Pro bottom](/images/system76/oryx_pro/review/bottom.jpg)

Funny, just a couple of weeks ago the price for my configuration was around $3,900. I guess this is a good sign that [the crypto business for GPUs is getting less lucrative?](https://www.pcgamer.com/reasons-to-be-cheerful-gpu-mining-is-dead-less-than-24-hours-after-the-merge/) (Or, you know, it could just be the fact that the laptop is on sale right now.)

In addition to hardware specs, you can also choose what operating system you want, order accessories to go along with the laptop, and/or extend the device's warranty. Should you feel more comfortable using Ubuntu rather than Pop!_OS, you can specify that when ordering. All of System76's devices come with one year of limited parts and labor warranty, but should you want to extend that period, that's possible at an additional cost.

Here's what the Oryx Pro has for ports. Left side:
- two USB 3.2 ports
- headphone and microphone jacks

![Oryx Pro left side](/images/system76/oryx_pro/review/left_side.jpg)

On the right:
- MicroSD card slot
- USB-C; supports DisplayPort 1.4
- Gigabit Ethernet

![Oryx Pro right side](/images/system76/oryx_pro/review/right_side.jpg)

On the back:
- barrel jack
- USB-C; supports Thunderbolt 4
- HDMI 2.1
- Mini DisplayPort 1.4
- Kensington lock

Nothing on the front other than a few LED indicators for hard drive activity and such. As far as the webcam goes, it's 2MP/1080p/30 FPS.

The battery is 6-cell and 80Wh. The dimensions with the 17" screen are 40cm x 26cm x 2cm (16" x 10" x 1"; keep in mind these numbers are rounded to the nearest whole number) and weighs 2.3kg (5 lbs). Most of the chassis consists of aluminum, albeit for the front cover for the LCD panel, which is plastic.

![Oryx Pro metallic hint](/images/system76/oryx_pro/review/metallic_hint.jpg)

There's the System76 logo on the top. A product information sticker, a Thunderbolt sticker, and an HDMI sticker are on the bottom. That's it. The chassis isn't cluttered with unneccesary branding. Nice, clean, and simple. I also like the subtle metallic hint that they put towards the back of the chassis and along part of the LCD panel (assuming it is metallic; I don't know what material it is). You do get a couple of S76-themed stickers in the envelope that's provided with the enormous box that they ship out to you if you do want to decorate it.

Speaking of the box, while it might be big, I thought it was pretty clever for the company to make good use of the inside with drawings. It looks mostly space-related, with a rocket taking off and a couple of planets behind it. An astronaut and a fish are seen on the left side of the box. If you were feeling creative you could probably take the drawing a step further by coloring it, since it's in black and white (S76 recently [Tweeted](https://twitter.com/system76/status/1570065358819852290) a photo of a small child coloring the picture with crayons; it's adorable).

![Oryx Pro box](/images/system76/oryx_pro/review/box.jpg)

# General Experience
**Pop!_OS**

Pop!_OS already comes with the NVIDIA drivers. So it was nice not having to install that as soon as I got the laptop. At the same time it's also nice that Pop! is pretty minimal when it comes to software out-of-the-box. I don't like distros that come bloated with software that I don't need.

Pop!_OS uses a fork of the GNOME desktop environment known as [COSMIC](https://news.itsfoss.com/system76-cosmic-panel/). There's a dock at the bottom containing your favorite applications. It's kind of similar to Mac OS. You can configure this dock to only appear when your mouse cursor is hovering over it, or where it's located. There's a launcher menu that you can access with the Super key, which allows you to quickly launch applications by typing in the first few characters of the app that you want to use and selecting it from the list that appears. This, combined with *tons* of touchpad gestures, make navigating and getting your work done on desktop a smooth and swift experience. I really like it. Plus, it comes with a dark theme right out of the gate, making the screen easier on your eyes, but you can easily switch to a light theme if you prefer.

![Pop!_OS desktop](/images/system76/oryx_pro/review/desktop.jpg)

But this desktop experience will only get better. System76 is currently in the process of [making their own Rust-based DE](https://linuxgamingcentral.com/posts/system76_new_de_written_in_rust/), which -- according to the VP of customer care at S76, Emma Marshall -- should lead to an even faster desktop experience while being less demanding on your computer's RAM. If all goes well we should be seeing an alpha release of this DE sometime next summer.

**Hybrid Graphics**

There's the sweet power of hybrid graphics. This is used by default on the Oryx Pro. Pop!_OS will use the CPU in most cases when running an application. However, should you want to use the discrete GPU for a certain app, you can do so with a [simple command line](https://support.system76.com/articles/graphics-switch-pop/). This gives the Oryx Pro the best performance to battery life ratio, saving battery when using the CPU, but giving the meat and potatoes to the apps that  really need the hardware boost. The nice thing is that the dGPU is already set to be used when running Steam, so there's no need to use this command when running games.

**Screen Glare**

Shifting the laptop from side-to-side, there's a *tiny* bit of glare but it's not significant by any means.

![Oryx Pro screen left side](/images/system76/oryx_pro/review/display_left_side.jpg)

![Oryx Pro screen right side](/images/system76/oryx_pro/review/display_right_side.jpg)

**Gaming**

As far as gaming goes, well, there's not much to say there. The Oryx Pro certainly does it's job. It's great to see games like *Horizon Zero Dawn* running at around 85 FPS on the highest settings. Combined with the 144 Hz refresh rate, it makes animations look super smooth. And keep in mind that's at *native* resolution; with FSR you could probably downscale the game at 720p while still retaining some of the same quality, while reaping even higher framerates. I should note the laptop gets pretty loud depending on the load it's taking in, but that's to be expected. Also, framerates will tank if the laptop isn't connected to the AC adapter (expect around 6 FPS in *Destroy All Humans! 2 - Reprobed*); presumably this is to keep the laptop from overheating, or to prevent it from consuming too much battery life.

**Webcam**

Actually kind of surprising to see an upgrade to the webcam's resolution. Most of the laptops shipped by S76 are 720p. This one comes in 1080p. Still 30 FPS, but that doesn't matter too much. The [HP Dev One](https://linuxgamingcentral.com/posts/hp-dev-one-review/) has a physical shutter for the webcam. I would like to see the same when it comes to S76's laptops. Adam told me he would 'pass this feedback along to the team.'

**Keyboard and Touchpad**

The built-in keyboard is nice. I like the font, I like the size, I like the feel when I push down on the keys. It's a relatively smooth typing experience. Plus, you can customize the backlight color with either the Function keys or S76's [keyboard configurator app](https://github.com/pop-os/keyboard-configurator). I personally prefer blue or red. At this time, saving the keyboard backlight color when restarting the laptop doesn't exist; it will just revert back to white. Adam told me that there are "some hurdles" in getting this to actually work, but "it's something that we're working on." In the meantime I guess I can just make a script that will save the backlight color for me.

![Oryx Pro running DAH2](/images/system76/oryx_pro/review/dah2.jpg)

When typing on this, keep in mind the right Shift key is very small. Very often I've accidentally bumped one of my fingers to the Up arrow key when I meant to hit right Shift. I would like to see a longer Shift key in a future revision, although I suppose they would have to re-design the whole keyboard since the arrow keys are right there. Also, be aware that there's no Caps Lock or Num Lock indicators. Something as simple as a small LED right on the key when it's on would be nice. Or they could put it on the front of the laptop where the power/hard drive activity LEDs are. And if they can't do either, at least have some sort of visible icon on the taskbar in Pop!_OS. But right now there's neither, so don't be surprised if you unknowningly hit the Caps Lock key and start typing an email in caps.

The touchpad is pretty huge. There's no buttons on it, but you can still "click" by pressing your finger down. Other than that there's not much else to say about it, other than it feels pretty smooth.

**Issues**

As a gamer, I like to see the stats as far as how my computer's hardware is being pushed when playing games. GOverlay makes it easier for me to customize what I want to see with MangoHUD. But in order to use GOverlay on Pop!_OS or any other Ubuntu-based distro, you have to manually compile MangoHUD from source and install all the dependencies that it requires. Otherwise, if you try to install GOverlay from the Pop! Shop, you'll get this in the terminal when trying to run it:

`can't get libdl.so`

I've passed my notes on to Adam and told him it might not be a bad idea to add the MangoHUD dependencies in the next release of Pop!_OS. He responded: "We're looking into the MangoHUD issue. I don't have a timeline for you but it's something we're investigating."

![Oryx Pro magenta keyboard backlight](/images/system76/oryx_pro/review/keyboard_backlight.jpg)

Probably the biggest gripe that I have with the Oryx Pro is, for a laptop with this kind of hardware, why go with a 1080p screen rather than 1440p? To which Adam responded:

> A lot of our Oryx users actually like to connect their machines to higher resolution and higher refresh rate displays than what most laptop manufacturers use. I do agree with you though. A 1440p panel would be really nice. I can't say too much other than we're constantly listening to feedback from our customers. We know there is a significant demand for a higher-resolution display. Keep your eyes on this space. :)

If I had paid for this laptop I would have been more than happy to shell out an extra couple of hundred dollars for a larger resolution. 1080p with an RTX 3080 Ti doesn't make much sense.

# Right to Repair
I've always commended System76 for their right-to-repair stance, and I will continue to do so. With the Oryx Pro, it's no different. You can freely check their [documentation](https://tech-docs.system76.com/models/oryp9/internal-overview.html) to understand where each individual component is on the inside of the laptop, instructions on how to take the laptop apart, and how to replace individual components, such as RAM and storage. There's even instructions on how to replace the cooling fan and speaker.

![oryx pro bottom panel off](/images/system76/oryx_pro/review/components-highlighted.webp)
*Image credit: System76*

This is incredible! It's *rare* that any manufacturer will offer any kind of instructions like this. They usually keep it locked down and force you to buy a new laptop if your hardware becomes outdated. Not the case with System76.

# Battery Duration
The battery, mentioned earlier, is 6-cell and 80Wh. **In integrated graphics mode, the battery lasts about four-and-a-half hours**. This was tested with the keyboard backlight off, screen brightness set to 50%, Wi-Fi and Bluetooth on, while looping a 1080p 60 FPS video via VLC. Testing under the same circumstances again **in discrete GPU mode, the battery lasted for two hours**. So, obviously not great, and you're definitely going to want to make sole use of the CPU where circumstances permit. You may want to have a look at the [Lemur Pro](https://system76.com/laptops/lemur) if you're looking for a laptop with better battery life.

# Benchmarks
Keep in mind benchmarks were recorded under the following circumstances:
- CPU governor set to "performance"
- NVIDIA driver 515.65.01
- kernel 5.19
- gaming benchmarks were made with Proton 7.0-4 and captured at 1080p, vsync off

Kernel compile time is **92.199 seconds**. This places the Oryx Pro around the 56th percentile rank on [openbenchmarking.org](https://openbenchmarking.org/test/pts/build-linux-kernel-1.14.0) and competes very closely with the Ryzen 7 5800X, which also has the same timing.

![oryx pro kernel compile time](/images/system76/oryx_pro/review/benchmarks/kernel_compile_time.jpg)

x264 encoding with Bosphorus at 1080p is **107.79 frames per second**. This would place it around the [63rd percentile rank](https://openbenchmarking.org/test/pts/x264&eval=eb54c6df8f4d5cf1f110ac2c4fd373453a43e1d1#metrics). It does a tiny bit better than the Xeon Gold 6226R, and just one frame behind the Ryzen 7 3800XT.

![oryx pro x264 encoding FPS](/images/system76/oryx_pro/review/benchmarks/x264_encoding.jpg)

Benchmarking *F1 2020* resulted in an average of 177, 167, and 131 FPS on Low, High, and Ultra settings respectively. Strangely that was all the results I got from this; normally I get a lot more data from Phoronix Test Suite on these kind of tests. Maybe I input the wrong number? But I hope this data will suffice.

![oryx pro F1 2020 average FPS](/images/system76/oryx_pro/review/benchmarks/f12020.jpg)

*GRID (2019)* is looking seriously impressive, scoring an average of 100+ FPS on the highest settings (this test isn't available via PTS; this was recorded manually).

![oryx pro GRID (2019) average FPS](/images/system76/oryx_pro/review/benchmarks/grid2019.jpg)

*Horizon Zero Dawn* was a bit odd. It seemed like every time I benchmarked the game I got different numbers. So you might want to take these results with a grain of salt, especially considering that for some reason the High graphics preset was getting a higher average FPS than Medium. Still, these numbers are looking pretty good (this also isn't availble on PTS).

![oryx pro Horizon Zero Dawn average FPS](/images/system76/oryx_pro/review/benchmarks/hzd.jpg)

# Wrap Up
I'm very impressed with the hardware inside this thing. When it comes to gaming, you really don't need to look at anything further than the Oryx Pro. The framerates are really good, the build quality is excellent, it's powered by open-source firmware, and it's using one of the best Ubuntu-based distributions out there. The keyboard and touchpad are pretty solid, the screen quality is decent, you have the right to repair it, and overall it's just a really good laptop. Not just for gaming, but for AI and machine learning as well.

A couple of caveats you have to keep in mind, however, is the 1080p resolution, which is frankly disappointing for a laptop with this kind of hardware, and if you're planning on using an app like GOverlay you'll have to build MangoHUD from source. Your fingers will also need to take some time for adjustment with the small right Shift key while typing, and be prepared to suddenly type in caps because one of your fingers inadvertently slipped on the Caps Lock key and there's no way of knowing about it until you start typing. Battery life is also pretty short, and when you're gaming you're going to need the device plugged in and charging, otherwise your framerates will tank.

![Oryx Pro Horizon Zero Dawn ultra benchmark](/images/system76/oryx_pro/review/benchmarks/hzd_ultra.jpg)

**TL;DR**

The good:
- beastly hardware packed in a compact form factor
- decent keyboard and touchpad
- utilizes Pop!_OS, which is a great choice
- powered by open-source firmware
- documentation is provided for opening the laptop up and replacing individual components
- minimal branding
- hybrid graphics balances battery life with performance when needed

The not-so-good:
- 1080p screen
- small right Shift key, no Caps Lock/Num Lock indicators, keyboard backlight color isn't saved on restart
- MangoHUD needs to be compiled from source in order to use GOverlay, although this is a problem with any Ubuntu-based distro
- relatively short battery life, even when using integrated graphics mode
- you can't do any serious 3D gaming without the AC adapter plugged in

Special thanks to **Adam Balla** for answering the dozens of questions that I had while writing this review (heh, he even offered to call me at one point with all the questions that I had). The Oryx Pro is available to order on [System76's website](https://system76.com/laptops/oryx), and it's on sale!

*Review unit sent courtesy of System76.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
