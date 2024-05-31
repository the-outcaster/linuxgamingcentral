+++
title = "You Don't Need a NVIDIA GPU to Use NVIDIA GameStream (Steam Deck Tutorial)"
date = 2022-10-31T13:10:15-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/sunshine_moonlight_guide/phone/ggst.jpg"
tags = ["guide", "steam deck", "moonlight", "sunshine", "streaming"]
keywords = ["steam deck", "guilty gear strive", "melee", "super smash bros", "ssbm", "moonlight", "sunshine", "nvidia", "nvidia geforce experience", "nvidia gamestream"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you haven't noticed, NVIDIA has a tendency of locking quite a few of their features behind a paywall. For instance, if you want to make use of DLSS, you have to have a RTX GPU. If you want to use their cloud streaming service, the host must be using a NVIDIA GPU *and* have the GeForce Experience app installed...which is only available on Windows.

However, no one has to get frustrated at this. Leave it up to the community to come up with workarounds. Not only can [FSR 2.1 be used in replacement of DLSS across any GPU vendor](https://linuxgamingcentral.com/posts/dlss-unlocker-for-various-games/), but we can use NVIDIA GameStream *outside* of Windows. On top of this, we don't need a NVIDIA GPU either! This is all thanks to an app called [Sunshine](https://docs.lizardbyte.dev/projects/sunshine/en/latest/about/overview.html).

NVIDIA GameStream is arguably *the* best game streaming solution. In my opinion it's the most stable, has the least amount of latency, and the streaming quality is great. It sure beats the pants out of Steam's built-in streaming service. Parsec could be a decent alternative...*if* the host version was available for Linux.

![Streaming Slippi from my Deck](/images/sunshine_moonlight_guide/phone/melee.jpg)

# Get the Host Set Up
Based on a [poll](https://mastodon.technology/@linuxgamingcentral/109226471670076713) I had recently conducted on Mastodon, the majority of users don't even know what Sunshine is. It's an [open-source](https://github.com/LizardByte/Sunshine/) alternative to GeForce Experience/NVIDIA GameStream and available for Linux. It takes the NVIDIA GPU requirement away for the host system, while still reaping all of the benefits of GameStream.

For this guide, we'll be going over setting up the Steam Deck as the host. Of course, you can use any device outside of this if you prefer.

Head over to the [Releases](https://github.com/LizardByte/Sunshine/releases) page on your Deck in Desktop Mode and download the latest AppImage. You could technically install the Flatpak, but I don't recommend this for two reasons:
1. It will break Discover. Every time you try to access the "Installed" section, it will cause the app to crash
2. You will need to [configure](https://docs.lizardbyte.dev/projects/sunshine/en/latest/about/usage.html#setup) uinput to create mouse and gamepad events. The AppImage takes care of this for you

Copy the AppImage to a convenient place, such as `~/Desktop`. Right-click it, go to Properties, and make sure the AppImage is marked as executable in the "Permissions" tab:

![Making Sunshine an executable](/images/sunshine_moonlight_guide/host/setting_appimage_as_executable.png)

Run it. It will appear as if nothing happened. But launch your web browser and point the URL to:

[https://localhost:47990/](https://localhost:47990/)

You'll probably get a warning about an insecure connection. If you're feeling insecure yourself at this point, then I honestly don't know what to tell you. The only way you're going to be able to proceed is if you proceed. On Chrome/Chromium-based browsers, click "Show advanced" and then "Proceed to localhost (unsafe)".

![Browser warning](/images/sunshine_moonlight_guide/host/proceed.png)

You should now be presented with Sunshine's login interface. Create a username and password. Please write this down before logging in, as you won't be able to recover this otherwise if you forget.

![Sunshine first time login](/images/sunshine_moonlight_guide/host/login.png)

The page will reload. Enter the credentials in the pop-up window to proceed.

![Sunshine logging in](/images/sunshine_moonlight_guide/host/signing_in.png)

If everything went well you should now be greeted with the main interface.

![Sunshine main interface](/images/sunshine_moonlight_guide/host/interface.png)

We're all set for now. Now we'll need to get the client set up.

# Get the Client Set Up
Moonlight, like Sunshine, is [open-source](https://github.com/moonlight-stream/moonlight-qt) and available for Linux as an AppImage or a portable tarball. It's also available in the [AUR](https://aur.archlinux.org/packages/moonlight-qt). Download it by whatever means you prefer and get it running. 

Here I'm running the application on my desktop. Note that the app probably won't pick up the host automatically; you'll need to manually enter the IP address of the host. Click "Add PC manually" on the top-right.

![Moonlight main interface](/images/sunshine_moonlight_guide/add_pc_manually.jpg)

Then enter the local IP address of the host:

![Moonlight adding PC manually](/images/sunshine_moonlight_guide/adding_ip_address.jpg)

On Deck, if you're not sure what the IP address is, you can click the Wi-Fi/Ethernet icon on the taskbar, clicking the connection you're using, then clicking the "Details" tab. Take note of the IPv4 address.

![Getting IP address of host](/images/sunshine_moonlight_guide/host/getting_ip_address.png)

After adding the IP address with Moonlight, your host should now be showing up.

![Moonlight Steam Deck added](/images/sunshine_moonlight_guide/deck_added.jpg)

You'll notice there's a lock icon on it though. To enable streaming to the Deck (or whatever you're using as host), click the device. You'll be shown a four-digit PIN:

![Moonlight PIN prompt](/images/sunshine_moonlight_guide/pin_instructions.jpg)

Quickly go back to your host, go to the "PIN" tab in the Sunshine interface, then add the PIN. If you don't do this within, say, 60 seconds, the connection will time out and you will have to generate a new PIN.

![Sunshine adding client via PIN](/images/sunshine_moonlight_guide/host/pin_pairing.png)

If you did it in time, the lock icon for the device in Moonlight should now be gone.

![Moonlight lock icon removed](/images/sunshine_moonlight_guide/lock_icon_removed.jpg)

You're pretty much all set from here. You can now stream your host to your client device. Note that the Steam option did not work in my case, and it probably won't for you either. But you're free to stream the host's desktop.

![Streaming my Deck's desktop](/images/sunshine_moonlight_guide/phone/desktop.jpg)

# Adding Specific Games
I don't really recommend adding individual games to stream from the host, as in my experience it has been a little buggy. But if for some reason you were worried about the client having access to the entire system of the host machine, and only wanted to make specific games streamable, you can do that.

Here I'll be adding *Guilty Gear -Strive-* as an example for adding a Steam game. On the host, go to the "Applications" tab in the Sunshine interface. Click the "Add New" button. In the new list of options that appear, give the application a name. Under the "Detached Commands" section, add this:

`steam steam://rungameid/<game-id>`

In *Guilty Gear*'s case, the app ID would be `1384160`. Of course, you can replace this with the app ID of any game that you want to add.

![Sunshine adding Guilty Gear -Strive-](/images/sunshine_moonlight_guide/host/adding_ggst.png)

Click the "+" icon to add it. Other than that that's about it. Note that I have *not* been able to figure out how to give each application a banner. Click "Save" at the bottom when done.

If you want to run an emulator, for example, the commands are a little different. You would have to add the path to the executable file under "Command" and then add the working directory under it. Here you can see an example of me trying to add [Slippi](https://linuxgamingcentral.com/posts/steam-deck-and-melee/).

![Sunshine adding Slippi](/images/sunshine_moonlight_guide/host/adding_slippi.png)

If everything went well these applications should now be showing up in Moonlight.

![Moonlight library](/images/sunshine_moonlight_guide/library.jpg)

Try launching these applications and see what happens. You may need to mess around with the settings a little bit in order to get them to properly stream.

# Tips
There's a big Settings menu that you can access in Moonlight. Here you can adjust many different options, including resolution, framerate, v-sync, audio, input, video codec, etc.

By default the resolution is set to 720p, and the FPS to 60. I recommend keeping it this way if your host is the Deck. Increasing the resolution will make the stream quality look better, but it comes at the downside of lag. Not input lag, but lag as in framerate. On the other hand, if the host *isn't* the Deck, and is capable of rendering games at a higher resolution than 720p, then be my guest.

I would also recommend connecting the host to the Internet via Ethernet, so as to minimize as much latency as possible. However, I've surprisingly had a decent experience streaming from my Deck via Wi-Fi. Just keep in mind there is a subtle, *very* subtle hint of input lag. Most games should still be fine, but for fighting games and other games that are fast-paced, you may want to opt in for Ethernet instead.

![Moonlight settings](/images/sunshine_moonlight_guide/settings_menu.jpg)

If you're streaming from a Deck, Game Mode will probably not work. On my end it just ended the stream. So just stream your games in Desktop Mode.

It *should* be possible to stream outside of your local network, but I have not tested this yet. If I happen to figure out how to do it, I will update this guide.

Finally, sometimes you may get an error trying to stream from the host. The error might say something along the lines of not having the proper ports forwarded to your client. If this happens, you will need to go into your router settings and forward the necessary ports to your client. Based on my testing so far I've had to forward these ports:
- 47998: UDP
- 48000: UDP
- 48010: TCP/UDP

Accessing your port forwarding settings is different depending on what router you're using. You'll generally need to enter the local IP address of the router in a web browser, log in (use the default credentials if you haven't changed this...you can find this info by a quick Google search), and going into the Advanced section. Here I'm providing an example of my setup with my TP-Link router:

![Moonlight settings](/images/sunshine_moonlight_guide/port_forwarding.jpg)

Set the internal IP to the IP address of your client.

A big thank you to all the developers behind both Sunshine and Moonlight for making quality streaming like this possible!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
