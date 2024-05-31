+++
title = "Tuxedo Pulse Gen 2: Not Worth Your Time"
date = 2022-08-23T06:37:41-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/tuxedo_pulse/cover.jpg"
tags = ["hardware review", "laptop", "tuxedo computers", "pulse"]
keywords = ["tuxedo pulse", "tuxedo computers"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Pulse by Tuxedo Computers is a thin, quiet laptop that boasts a great battery life. Improvements over the last-generation model include a larger screen with a higher refresh rate, as well as a USB-C port with DisplayPort 1.4 support. Unfortunately as far as the positive traits go, that's just about it. It's probably one of the most broken, frustrating laptops I've ever had to deal with.

# Specs
The second-generation Pulse comes in a 15.6" screen and has a resolution of 2,560 x 1,440 pixels. Interestingly enough, even though you can't get a discrete GPU with it, the refresh rate is 165 Hz. Wonder why they added that. Wi-Fi 6 and Bluetooth 5.2 is included. The chassis is apparently made out of magnesium, and the battery is 91 Wh.

Weight is 1.5kg (3.3lbs) with dimensions of 356.4 x 233.73 x 16.8mm (14 x 9.2 x 0.7in).

![tuxedo pulse 2 top side](/images/tuxedo_pulse/top.jpg)

The only processor you can get with the Pulse Gen 2 is the Ryzen 7 5700U with Radeon RX Vega 8 graphics, configured at 35 W (eight-core, 16 threads, 1.8-4.3 GHz). The minimum amount of RAM and hard drive space you can get is 8 GB and 250 GB respectively. This configuration would cost **1,164 EUR ($1,156.83 USD)**. The Pulse with maximum specs would have 64 GB of RAM and 4 TB of Samsung 980 Pro NVMe storage -- this would cost **2,139 EUR ($2125.82 USD)**.

My configfuration costs **1,399 EUR ($1390.38 USD)** and comes with 32 GB RAM and 1 TB of NVMe. Should you want to add your own components, it's totally possible; there's two SO-DIMM slots for replacing the DDR4 RAM (up to 3,200 MHz), and there's two 2280 slots for replacing the M.2 drives.

Ports are as follows:

Left:
- Kensington lock
- Ethernet jack
- USB 2.0 type A
- USB 3.0 type A
- headphone jack
- MicroSD card slot

![tuxedo pulse 2 left side](/images/tuxedo_pulse/left_side.jpg)

Right:
- USB-C, capable of DisplayPort 1.4
- USB 3.0 type A
- HDMI port
- barrel jack

![tuxedo pulse 2 right side](/images/tuxedo_pulse/right_side.jpg)

# Turning it on for the First Time
My review unit shipped with Tuxedo OS 22.04. For those of you who aren't aware, Tuxedo OS is Tuxedo Computer's fork of Ubuntu. Version 22.04 uses KDE Plasma. Upon turning the device on, right off the bat I get a message saying the computer is not connected to Internet, and it's not plugged in. I connected to Wi-Fi, and plugged the laptop in. Neither message went away. I proceeded to go through the installation and first-time setup anyway. After configuring my user account details, I waited for the installation to finish. I get this:

![error after install](/images/tuxedo_pulse/install_failed.jpg)

Okay. Now the only way I can shutdown the computer is by holding the power button. There's no icon for it on the taskbar. Upon turning the computer back on, the login screen appears. Not matter how carefully I try to type in my password, the computer just refuses to let me log back in.

My only choice now? Re-install the OS.

# Re-installing Tuxedo OS
I still find it baffling that Tuxedo *still* hasn't made their OS available as a direct download. You still have to use their supplied USB drive and install the distro that way. I had asked about this almost a year ago, back when I was writing the [Tuxedo Stellaris](https://boilingsteam.com/tuxedo-stellaris-the-meanest-laptop-money-can-buy/) review on Boiling Steam, and they had told me they were not only going to push the source code to GitHub, but they were going to have an ISO "in the medium term." Nothing has happened on either front.

So, you've got a proprietary distro, and the only way you can install it is with *their* specially-marked USB drive, *and* you need to be connected to the Internet via Ethernet in order for the installer to even work. Heck I wouldn't be surprised if the distro includes that weird performance boost that you can't get with other distros.

And boy, believe me, that's just the tip of the iceberg for the problems. Did you know how many times I've had to re-install the OS before it *finally* installed successfully? I've just had to do trial and error, hoping the "You're not connected to the Internet" and "The laptop is not charging" messages would be gone. Literally nothing else I could do.

![cat in box](/images/tuxedo_pulse/tuxedo_box_with_cat.jpg)

After re-installing Tuxedo OS for the third or fourth time, the installer *finally* was successful. I was able to reboot and login. Able to update the system's software packages, able to install software, etc.

When I sent Tuxedo a couple of photos of the errors that I came across during installation, they told me that they weren't able to replicate the issue "but I got the information that something has changed in our packages in the last week. Therefore, our request to you to install the device again." Of course, they didn't get back to me until *after* the installation went through.

# Screen Doesn't Come Back On (Or, at least it didn't)
When closing the lid to the laptop and opening it back up, the screen remains black. Tuxedo told me they're aware of the issue and asked me to send them the contents of `lspci -nnvv`. I sent this to them as a text file. Bam. Issue no longer exists. The screen actually turns on after the system got updated.

![left screen side](/images/tuxedo_pulse/screen_left.jpg)

![right screen side](/images/tuxedo_pulse/screen_right.jpg)

Let me just say I'm glad I didn't pay for this laptop -- I shouldn't have to help them with things like this. This is unacceptable, especially for legit paying customers.

# I Bricked my System...
Whatever you do, don't add a PPA on Tuxedo OS. You're going to end up bricking your system because apparently some packages will need to be removed.

I had wanted to install [CoreCtrl](https://launchpad.net/~ernstp/+archive/ubuntu/mesarc) so I could change the CPU governor to performance, but that requires adding the mesarc PPA. So I added it, ran `sudo apt update` and `sudo apt upgrade`...and the system couldn't install any of the new packages. Even specifying the PPA to only get CoreCtrl installed didn't help. Removing the PPA didn't help either. So when I wanted to run a benchmark with Phoronix Test Suite, there were missing dependencies that the program couldn't install.

The suggestion was to run `sudo apt --fix-broken install`. Boy, what a mistake that was. The terminal ended up uninstalling several programs -- and key ones, at that. While the programs were uninstalling, the screen went blank. Done. Now the computer wouldn't turn on.

And so I had to go through the nightmare of re-installing Tuxedo OS once more...

# The Keyboard
Notice how I haven't even talked about problems on the hardware side yet. Take a look at the keyboard:

![tuxedo pulse gen 2 keyboard](/images/tuxedo_pulse/keyboard.jpg)

You'll notice:
- "y" and "z" keys have been swapped
- some of the characters on the right side aren't English

Uh...what exactly was the purpose of this?

Typically I would be typing these kind of reviews with the laptop I was provided. Not so much in this case. Can't tell you how many times I put in a "=" when I meant to put in a "-".

# Decent Battery Life
The one redeemable quality the Pulse 2 has is its solid battery life. Tuxedo claims it lasts 10 hours with medium brightness and Wi-Fi on. I ran this test myself, looping a 4K 60 FPS video with MPV, and it lasted roughly **nine hours.** That's pretty good.

# Kernel Compile Time
I was hoping I could get more benchmarks in rather than just kernel compile time, but the laptop has been so unnecessarily frustrating to use that this is all I could really settle for. Kernel compile time is **180 seconds.** This puts it right around the 26th percentile rank on [openbenchmarking.org](https://openbenchmarking.org/test/pts/build-linux-kernel-1.14.0) and matches neck-and-neck with the Intel Xeon E5-2620.

![tuxedo pulse gen 2 underside](/images/tuxedo_pulse/back.jpg)

# Don't Get It
As much as I like how quiet and thin the Pulse 2 is, it's not worth your money. There is just *so* many problems with it, especially on the software side, that prevent me from wanting to recommend it to anyone. It's broken; chances are Tuxedo OS isn't going to work out-of-the-box for you, you'll have to re-install it three or four times with their USB drive, and then you'll end up bricking your system anyway because you tried to add a PPA. If you do end up getting it for some unfortunate reason, at least *don't* use Tuxedo OS; install a different distro. I almost guarantee half of your issues will disappear.

Tuxedo Computers still hasn't released the Tuxedo OS ISO, nor have they released the source code. Sorry, this just sounds *way* too fishy for me.

**TL;DR**

The good:
- decent battery life
- thin and quiet

The not-so-good:
- messed-up keyboard with mixed letters and symbols
- the most broken operating system I've ever had to deal with, with countless re-installs
- still no news on Tuxedo OS ISO being available; still has to be installed via USB drive

*Review unit sent courtesy of Tuxedo Computers.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
