+++
title = "An Interview with Kyle, Author of the CryoUtilities App"
date = 2023-03-02T15:36:02Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/kyle/cover.jpg"
tags = ["interview", "cryoutilities", "steam deck", "cryobyte33"]
keywords = ["cryoutilities", "cryoutilities 2.0", "cryoutilities developer", "cryoutilities interview", "cryobyte33"]
description = "An interview with the dev of what is arguably the best Steam Deck app of all time."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you own a Steam Deck and haven't used [CryoUtilities](https://linuxgamingcentral.com/posts/cryoutilities-2.0/), do yourself a favor and use it. I guarantee you won't be disappointed.

And so, I had an opportunity to interview the primary developer (there's 12 contributors altogther) behind the excellent app -- Kyle (AKA CryoByte33). Watch out; he's not afraid to boast that he's in the top 5% of users who have the most knowledge about Linux. But that knowledge has been put to good use -- otherwise, I would tend to think CryoUtilities wouldn't have the performance benefits that it has. His YouTube channel has garnered almost *30K* subs, and some have said that Valve should hire him.

They *should*.

**TL;DR**
- DevOps engineer, 18 years of Linux experience
- CryoUtilities: it fine-tunes the kernel on the Deck for increased gaming performance, while also freeing up storage space (leftover Steam compatdata or shader cache)
- "top 5%" of users who are familiar with Linux
- prefers Arch with GNOME
- CryoUtilities uses Go for "rapid prototyping" and "dependency management"
- the Steam Deck: "the biggest innovation in gaming in a long, long time"
- how to help: contribute to the code if you're knowledgeable of the Go language, report bugs, contribute financially

# Explain who you are and what you do.
My name is CryoByte33, or Kyle, and I'm a DevOps engineer for my day job. I manage the software of hundreds of Linux servers every day, and the hardware of dozens more. 

I have 18 years of Linux experience, and my hobbies are gaming, homelabbing, 3D printing, and tinkering with tech. Nowadays I mostly tinker with the Steam Deck!

# For people who aren't aware, can you explain what CryoUtilities is and why a person should use it on their Steam Deck?
CryoUtilities is a utility that I developed which has two main categories of functionality:

First, it performs **very low-level kernel tweaks in order to tune the kernel for maximum performance in games**. The default Steam Deck configuration is very focused on throughput rather than latency, which harms gaming performance a lot of the time. My tweaks swap that around, which results in higher gaming performance.

![CryoUtilities 2.0](/images/steam_deck/cryoutilities/2.0/cover.webp)

Second, it has some **storage management features** for the Steam Deck. They allow you to clean up data that Steam leaves behind after uninstalling games, or move the compatdata and shadercaches to the same drive where the game is installed. **I've heard of savings of up to 40GB on the internal drive!**

# How familiar are you with Linux? Do you have a "go-to" distro and desktop environment?
I'd say that I'm more familiar than the majority of Linux users. I don't think anyone besides Linus himself can claim to be an expert in every facet, but **I'd consider myself to be in the top 5% of users, knowledge-wise.**

As for my go-to distro, it depends on the use case. For my desktops and gaming machines, I almost always use an Arch derivative or Arch itself. Currently, my desktop is running [Nobara](https://linuxgamingcentral.com/posts/nobara-project-impressions/), though I'm missing the AUR quite a bit and will probably move to EndeavourOS.

![Nobara Project](/images/nobara/version_37.webp)

For homelab use, I prefer CentOS/AlmaLinux for the rock solid stability. 

If I use a DM, I prefer GNOME for the workflow management and stability. KDE Plasma is a close second, but I still have some issues with multiple monitors from time to time.

# Did you develop CryoUtilities on desktop or on Deck? If on desktop, was it on Windows, Mac, or Linux?
I did most of the development on my 14" M1 Pro Macbook Pro, but all of the testing on the Deck itself. Until just the other day I only had a single Deck, so I couldn't "pollute" the OS too much without affecting test results. Now that I have a second Deck, I'll be doing most development from the Deck itself!

# What's your favorite IDE?
I use [Jetbrains IDEA](https://www.jetbrains.com/idea/) with their language plugins for just about everything, although I might swap to [Fleet](https://www.jetbrains.com/fleet/) when it leaves early access. I find that the code completion and refactoring is much better than the competitors, and I don't need to tinker with a ton of plugins to do it.

![Jetbrains IDEA](/images/interviews/kyle/idea_ide.webp)

# Besides the speed benefits of the Go language, was there any other reason for switching to said language for CryoUtilities?
Rapid prototyping, dependency management, and I wanted to learn Go. I actually started the latest version in Rust, but prototyping was going slowly and the GUI frameworks aren't quite there yet. That said, Go has its own struggles so who knows what we'll see in version 3.

# With the new 2.0 release, how has reception been so far?
Beyond my wildest dreams. My [channel](https://www.youtube.com/@cryobyte33) has gained an extra 50% in subscribers, people are mentioning it on ProtonDB, my [Discord](https://discord.gg/ySe8WGVNPv) has quadrupled in size, and there is very active development happening on it! When I made the original swap resizer script, I was just trying to keep *GTA:V* and *RDR2* from crashing, it's come a LONG way.

# Speculation time: do you think Valve will eventually incorporate some of the features of CryoUtilities into SteamOS?
It's very possible! Everything except for the swap size is "free" in terms of resources, so there's nothing keeping them away. That said, page lock unfairness could cause a decrease in "general computing" performance like code compilation or Blender renders, although I haven't been able to confirm any perceptible differences.

![CryoUtilities 2.0 CLI](/images/steam_deck/cryoutilities/2.0/cli.webp)

# What are your thoughts on the Steam Deck?
I think that it's the biggest innovation in gaming in a long, long time. It's a bit rough around the edges, but **this is the first glimpse we've had at a true console competitor that allows for user serviceability, tweaking, and upgrading.**

On a macro scale, I think that the gaming industry has been moving in this direction for a while. Mid-generation refreshes and "pro" controllers are meant to appease the hungrier consumers, with the "Elite" controllers allowing for even more customization. The Steam Deck took that idea and ran with it, for the better.

# How can the community help with the growth of the project?
There are three main ways that you can help:
1. If you know development, especially in Go, feel free to contribute! I'm a bit picky about what makes it in to the final product, but I'd love to see your ideas.
2. Report any issues you may have in the [repo](https://github.com/CryoByte33/steam-deck-utilities). Myself or another contributor can work on fixing it. We're also open to improvement suggestions!
3. Of course, [financial support](https://patreon.com/cryobyte33) helps. The GitHub sidebar has a few places you can donate, and every dollar helps tremendously for me spending more time on CryoUtilities.

# Have you laid out any plans for the 3.0 release, if any?
Not yet, but I have some ideas and tweaks in mind. I don't think that we've hit the limits of what the Deck can do, and I'm going to do my best to hit that limit.

# Anything else you want to share with us?
I have a LOT of plans for both CryoUtilities and the channel, so definitely follow along if you're interested!

Kyle is available at the following places:
- [Website](https://cryobyte.io/)
- [YouTube](https://www.youtube.com/@cryobyte33)
- [Mastodon](https://mastodon.cryobyte.net/@cryobyte33)
- [Discord](https://discord.gg/ySe8WGVNPv)
- Support him on [Patreon](https://www.patreon.com/cryobyte33) or [PayPal](https://www.paypal.me/cryobyte33tv)
- [CryoUtilities on GitHub](https://github.com/CryoByte33/steam-deck-utilities)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
