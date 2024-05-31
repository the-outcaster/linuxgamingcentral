+++
title = "Overclock Your Steam Deck For Increased Performance"
date = 2023-12-08T19:13:28Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/overclocking/cover.jpg"
tags = ["guide", "steam deck", "overclocking"]
keywords = ["steam deck overclocking", "smokeless umaf", "steam deck firmware downgrade", "powertools decky"]
description = "Lots of testing and patience required."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
So, you decided to keep your LCD Steam Deck. Well good. We gonna overclock this son of a biscuit so we can squeeze a couple of extra FPS in during our gameplay sessions. Keep in mind that, for the time being, the Steam Deck OLED is NOT overclockable, and even though the LCD Deck is still capable, the firmware on the device will need to get downgraded first.

We'll be going over how to overclock the CPU, GPU, and TDP. Technically it's possible to overclock the RAM, depending on the memory manufacturer, but I will NOT be covering that in this guide. I almost ended up bricking my own Deck trying to OC it to 6400 MT/s; the only way I could recover the device was by resetting the CMOS.

For your convenience, since this guide is quite lengthy, I've added a table of contents, so you can quickly jump to the section of your choosing.

# Table of Contents
**FAQ**
- [Is overclocking dangerous?](#is-overclocking-dangerous)
- [Is overclocking worth it?](#is-overclocking-worth-it)

**Guide**
- [Prerequisites](#prerequisites)
- [Keep your Deck cool](#keep-your-deck-cool)
- [Get PowerTools](#get-powertools)
- [Downgrade the FW](#downgrade-the-firmware)
- [Boot into Smokeless](#boot-into-smokeless)
- [Undervolting](#undervolt-for-increased-battery-life)
- [Disable updated fan control, increase swap/UMA, manually set power control](#disable-updated-fan-control)
- [Increase TDP limit](#overclock-the-tdp)
- [Overclock CPU/GPU](#overclock-cpu-and-gpu)
- [Testing your numbers](#testing-testing-and-some-more-testing)
- [Troubleshooting](#what-to-do-if-the-deck-doesnt-turn-on)

# Is Overclocking Dangerous?
It can be, if you set the numbers too high. If the Deck becomes too hot (think 90+ degrees C), it will do one of two things:
1. Throttle the temperature down temporarily. Both the CPU and GPU will go to their lowest speed until the APU cools down, causing the game to run like a slideshow.
2. If the Deck doesn't throttle the temperature, it will shut off to protect itself from overheating.

In my case, I was able to overclock to the following numbers:
- CPU: 4 GHz
- GPU: 2 GHz
- TDP: 25 W

While also being able to undervolt the CPU, GPU, and SoC to -40mV.

Note that 25 W is a bit on the extreme side; I only set this number since I have the JSAUX cooling fan on. A safer number would be 20-21 W.

[Back to top](#table-of-contents)

# Is Overclocking Worth It?
Depends on the game you're playing. In general I'm seeing about a 10% performance boost across the board. So, for example, if a game is running at 60 FPS on stock settings, it will jump to 65-66 FPS with overclocking applied. Some heavy-hitting AAA titles will certainly benefit from the overclock.

![Horizon Zero Dawn benchmarks - stock vs. overclocked](/images/steam_deck/overclocking/hzd_stock_vs_oc.jpg)

That being said, overclocking is going to drain the battery very quickly -- as little as an hour in some of my tests. If your numbers are too high you're also going to experience the Deck shutting itself off because it gets too hot, or throttling the temperatures to keep itself cool, causing the game to run very slowly for a minute or two.

Whether you want to put up with that hassle for a few extra FPS is going to be up to you. You're going to need a lot of patience playing around with numbers while constantly rebooting the Deck to test for new values.

[Back to top](#table-of-contents)

# Prerequisites
Some things you'll need to get started:
- USB-C dock
- USB keyboard
- USB flash drive, formatted as FAT32, with [Smokeless_UMAF](https://github.com/DavidS95/Smokeless_UMAF) installed on it
- (recommended) some cooling solutions, be it thermal paste, Steam Deck backplate with aluminum heat dissipation, a cooling fan, etc.

On the software side:
- [Decky-Loader](https://github.com/SteamDeckHomebrew/decky-loader) with [PowerTools](https://git.ngni.us/NG-SD-Plugins/PowerTools) installed
- SteamOS firmware downgraded to 116 or below with [Steam Deck BIOS Manager](https://github.com/ryanrudolfoba/SteamDeck-BIOS-Manager)
- (recommended) 4 GB UMA frame buffer size, with recommended settings from [CryoUtilities](https://github.com/CryoByte33/steam-deck-utilities) (16 GB swap with swappiness of 1)

We'll be going over these steps along the way, so don't worry about applying these changes now.

[Back to top](#table-of-contents)

# Keep your Deck Cool
As a prerequisite, **I highly recommend looking for some cooling solutions prior to starting the overclock process.** Some things that you can do:
- open your Deck up, remove the existing thermal paste on the APU, and upgrade it to a different paste that can sustain higher temperatures
- change the backplate to something that uses a different thermal profile. The [JSAUX backplates](https://linuxgamingcentral.com/posts/jsaux-rgb-backplate-review/), for example, uses aluminum to keep the APU temps down, while also providing a cutout for the fan exhaust. I've noticed the APU is an entire 10 degrees C cooler with the JSAUX backplate on
- add some cooling fans. You could try the [JSAUX cooling fan](https://linuxgamingcentral.com/posts/jsaux-modcase-for-steam-deck-review/#cooling-fan) (it's designed to work with their ModCase accessory but you can also use the fan itself without the ModCase). This can lower APU temps -- at least during my testing -- by 14 degrees C. Alternatively you can just get a [docking station that has a cooling fan attached](https://www.amazon.com/LISEN-Docking-Station-Charging-Ethernet/dp/B0BQRB7X9V)

![JSAUX cooling fan](/images/steam_deck/overclocking/cooling_fan.jpg)

[Back to top](#table-of-contents)

# Get PowerTools
If you don't already have [Decky-Loader](https://github.com/SteamDeckHomebrew/decky-loader), install it. Installation is incredibly simple; just go to the GitHub page in Desktop Mode, click the Download button, and run their installation script.

Go back to Game Mode. A plugin icon should appear in the Quick Access Menu. Select it, go to the shopping icon on the top-right, and install PowerTools from the plugin store. PowerTools will allow us to override the TDP limit once we've set some values in Smokeless.

![PowerTools from Decky-Loader store](/images/steam_deck/overclocking/powertools.jpg)

[Back to top](#table-of-contents)

# Downgrade the Firmware
If you have recently updated SteamOS on your LCD Deck, chances are it's running firmware 119. **To have overclocking options available to us, we first need to downgrade the firmware to 116 or below.** An easy way to downgrade is by using [Steam Deck BIOS Manager](https://github.com/ryanrudolfoba/SteamDeck-BIOS-Manager) from 10 Minute Steam Deck Gamer.

Go to Desktop Mode. Open a terminal. Clone the repo and run the program:
```
git clone https://github.com/ryanrudolfoba/SteamDeck-BIOS-Manager.git
cd SteamDeck-BIOS-Manager
chmod +x steamdeck-BIOS-manager.sh
./steamdeck-BIOS-manager.sh
```

Enter sudo password when prompted. Select DOWNLOAD from the menu and click/tap OK. This will download all of the available firmware, including 116. Next, select FLASH from the menu, and select `F7A0116_sign.fd` from the list of downloaded FW. You'll be asked if you want to backup your current BIOS. Please do so.

![Download Steam Deck BIOS](/images/steam_deck/overclocking/download_bios.png)

Your Deck will restart and install the older firmware. Note that if you have the DeckHD installed, you will need to re-run their [flashing script](https://www.deckhd.com/flashing-bios) to use the entire screen again.

After the FW has been flashed, go back into Desktop Mode. Re-run the Steam Deck BIOS Manager. This time, select BLOCK to prevent SteamOS from upgrading the FW. Then, select SMOKELESS so we can have access to the overclocking options in Smokeless_UMAF.

![Block BIOS updates](/images/steam_deck/overclocking/block_bios_updates.png)

[Back to top](#table-of-contents)

# Boot into Smokeless
Plug in a USB flash drive to a computer (or your Steam Deck via a USB-C dock). Format it as FAT32. Go to the [Smokeless_UMAF GitHub page](https://github.com/DavidS95/Smokeless_UMAF), download the UniversalAMDFormBrowser under the Download section, extract the files to the flash drive.

Connect a USB-C dock to your Steam Deck. Connect a wired keyboard along with the flash drive. While the Deck is off, hold the Volume- button while turning the device on. This will bring you to the boot menu. Select your flash drive from the list.

You should now be in Smokeless, and if everything went well, there should be two options under Device Manager: AMD PBS and AMD CBS. We can ignore AMD PBS; we won't be using that in this guide. Note that the display is sideways because the Steam Deck's display is set up to run in portrait mode by default.

![Smokeless on Deck](/images/steam_deck/overclocking/smokeless.jpg)

Please be aware that, at least during my testing, if you hold down the Up or Down arrow keys for too long, the device will freeze for some odd reason. Just hold the Power button to turn it off, then try booting back into the flash drive.

[Back to top](#table-of-contents)

# Undervolt for Increased Battery Life
The first thing we'll want to do while in Smokeless, is **[undervolt the Deck](https://linuxgamingcentral.com/posts/steam-deck-undervolting/)** if we can. This will not only keep the Deck running at a cooler temperature while providing the same performance, but also marginally increase the battery life. Per the explaination from [CryoByte33](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/):
> Chip manufacturers have to provide an amount of voltage that every chip is guaranteed to run with, but some can use far less power to do the same amount of work. Undervolting is the process of providing those chips with less voltage. Your Deck will typically run a lot cooler, which will keep the fan quieter. Undervolting can help maintain higher speeds for longer, which can improve performance. It usually even improves the battery life of the Deck!

Using your keyboard in Smokeless, go to Device Manager -> AMD CBS -> SMU debug options -> SMU feature config limits. **Change SVI3 voltage control to Manual.** New entries should now be displayed:
- VDDCR_VDD - CPU
- VDDCR_SOC - SoC
- VDDCR_GFX - GPU

Change **VDDCR_VDD voltage offset sign to Negative. Set the VDDCR_VDD voltage offset to 10.** This will undervolt the CPU by 10 mV. **Repeat this process with VDDCR_SOC and VDDCR_GFX.** The CPU, GPU, and SoC should now all be undervolted by 10 mV. Now keep pressing Escape on the keyboard to back out of the menus. When Smokeless asks if you want to save your settings, press Y. Go back to the main menu, select Continue, and you should be good to go.

![Undervolting the CPU, GPU, and SoC with Smokeless](/images/steam_deck/overclocking/undervolting.jpg)

Run a few games. See what happens. If you don't get any visual artifacting, or don't see games randomly crashing, you're safe. Now you can keep going into Smokeless and decreasing the CPU, SoC, and GPU voltage by 10 mV. Save settings, keep testing, and once you get random crashing, that's going to be your limit.

In my case, I have been able to safely undervolt the CPU, SoC, and GPU to -40 mV.

[Back to top](#table-of-contents)

# Disable Updated Fan Control
While your Steam Deck is on, go to Settings -> System -> Go all the way to the bottom. **Disable the updated fan control toggle.** The new fan curve prioritizes sound over thermal performance and can cause overheating if enabled. You're going to have a louder fan, but you've got headphones, right?

![PowerTools from Decky-Loader store](/images/steam_deck/overclocking/updated_fan_control_off.jpg)

Now go into Desktop Mode. Download and install [CryoUtilities](https://github.com/CryoByte33/steam-deck-utilities). **Apply CryoByte33's recommended settings, applying 16 GB of swap space, and a swap tendency of 1.**

![CryoUtilities - recommended settings](/images/steam_deck/overclocking/cryoutilities.png)

Turn the Deck off. Access the BIOS by holding Volume+ while turning the device on. Go to Setup Utility -> Advanced. **Set power control to manual. Ensure both the "Fast PPT" and "Slow PPT" limits are set to 15000.** We can't overclock the TDP limit in Smokeless otherwise.

While you're here, I *strongly* recommend **setting the UMA frame buffer size to 4 GB** if you haven't already. This will improve graphics performance in games.

![Manual power control in BIOS](/images/steam_deck/overclocking/manual_power_control.jpg)

Press the Back button to save your changes.

[Back to top](#table-of-contents)

# Overclock the TDP
Turn the Deck off again. Boot into Smokeless. With your keyboard, navigate to Device Manager -> AMD CBS -> SMU Common Options. **Set TDP control and PPT control to manual. Set your desired max TDP into the TDP, Fast PPT Limit, and Slow PPT Limit fields, followed by three zeroes.** For example, if you wanted to set the max TDP to 18 W, you would type in 18000 for all three fields.

I recommend starting off with 18 W, then gradually increasing this value if you're feeling confident and your Deck doesn't throttle itself or shut itself off during gameplay. In my case I've been able to push 25 W, but frankly this is a bit overkill, and the only reason why I've been able to get away with it is because of the backplate I'm using along with the JSAUX cooling fan. A safer option would be 20-21 W.

![Increasing TDP limit with Smokeless](/images/steam_deck/overclocking/increasing_tdp_limit.jpg)

Keep pressing Escape until you're asked to save your changes. Press Y. Exit Smokeless.

Run a game. Open the QAM -> Decky -> PowerTools. Go down to PowerPlay Limits and toggle it on. Set both the Fast and Slow PPT limit to what you had set in Smokeless. So if you set the TDP to 18 W in Smokeless, you would also set this in PowerTools. Closely observe the APU temperature (you can set the performance overlay to 4 so you can see these numbers). If either the CPU or GPU gets over 90 degrees C, that's when you need to lower the TDP limit so the Deck doesn't throttle itself. On the other hand, if the temperatures are in a relatively safe range, you can gradually increase the TDP limit in Smokeless until you start seeing erratic behavior in-game.

![PowerPlay Limits applied](/images/steam_deck/overclocking/overclocking.jpg)

Do NOT use Steam's built-in TDP limiter in the QAM. If you toggle this on, it will override your TDP limit settings in PowerTools.

[Back to top](#table-of-contents)

# Overclock CPU and GPU
Once you've played around with the TDP limit and found a good number, we can also overclock both the CPU and GPU.

Boot back into Smokeless -> Device Manager -> AMD CBS -> SMU Debug Options -> SMU Feature Config Limits. **Go down to "CclkFmaxOverride Control" and set it to manual. Set the max CPU frequency, in megahertz, next to the "CclkFmaxOverride" option.** By default, the max frequency set on the Deck is 3500 MHz (3.5 GHz). Set it to your desired value. Setting this to "3600" would be a good starting point. I wouldn't go past 4000 MHz.

While you're here, you can also increase the GPU clock frequency. By default, the Deck's GPU is set to 1600 MHz (1.6 GHz). **Set "GfxclkFmaxOverride Control" to manual, then enter the desired frequency next to "GfxclkFmaxOverride".** A good starting point would be 1700 MHz.

![Overclocking CPU and GPU with Smokeless](/images/steam_deck/overclocking/ocing_cpu_and_gpu.jpg)

Keep pressing Escape on the keyboard until Smokeless asks if you want to save your changes. As usual, press Y to save settings, then select "Continue" to boot into SteamOS.

[Back to top](#table-of-contents)

# Testing, Testing, and Some More Testing
Keep running some games. Keep an eye on the APU's temperature. If at some point the Deck throttles the temperature, or shuts itself off, that's when you know you pushed the numbers a little too far. Keep adjusting the TDP limit, CPU and GPU frequencies in Smokeless, until you've found a decent number where you can get more than 10 minutes of gameplay without any interruptions. Make sure you also toggle on "PowerPlay Limits" in PowerTools so you can take advantage of the TDP limit you set in Smokeless.

As a reminder, I've been able to set my numbers as follows. Keep in mind you may *not* be able to reach these numbers yourself, depending on how well you scored with the "silicon lottery" and what you have available for cooling solutions:
- TDP limit: 25 W
- CPU frequency: 4000 MHz (4 GHz)
- GPU frequency: 2000 MHz (2 GHz)
- CPU, GPU, and SoC undervolted to -40 mV

![Avatar Frontiers of Pandora with OC'ing applied](/images/steam_deck/overclocking/avatar.jpg)

Nice. After about a couple dozen reboots, you should be good to go. Enjoy your overclocked machine! Note that since the battery drains more quickly with the overclock, it might be worth docking the Deck and using it as a console (I've noticed the Deck is less likely to shut itself off when the charger is plugged in as well).

[Back to top](#table-of-contents)

# What to Do if the Deck Doesn't Turn On
This shouldn't normally happen, so long as you play it safe with your numbers, but in the event the Deck doesn't turn on, you can reset the CMOS to restore the factory BIOS settings, which should allow the Deck to turn back on.

While the device is off, hold the Volume- button and the QAM button, then press the Power button. Keep holding the buttons down until a symbol appears on the screen. This will revert all your changes to the BIOS, TDP limit, CPU/GPU freq, etc.

Thanks to **CryoByte33** for the [original guide](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/).

[Back to top](#table-of-contents)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
