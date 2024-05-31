+++
title = "Rest in Peace, Old Big Picture Mode"
date = 2023-02-08T19:45:34Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/retrospectives/old_bpm/cover.webp"
tags = ["retrospective", "old big picture mode"]
keywords = ["steam old big picture mode", "steam big picture mode", "steam old big picture mode", "big picture mode", "bpm", "old bpm", "new bpm", "steamos", "steam deck"]
description = "No one is going to miss you."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Valve had first announced Steam's Big Picture Mode interface [twelve years ago](https://www.pcgamer.com/valve-announces-big-picture-mode-for-steam/). Valve spokesman Doug Lombardi had mentioned: "With Big Picture Mode, gaming opportunities for Steam partners and customers become possible via PCs and Macs on any TV or computer display in the house."

Speculation had started. Did Valve want customers to buy new network-capable TVs and stream games from their PC? Or did they want users to connect their PC to the living room TV and use the PC like a console?

Geoff Keighley would visit Valve's headquarters six months later. Greg Coomer (remember, he was with Lawrence Yang back in the [Steam Deck dev conference](https://boilingsteam.com/the-steam-deck-conference-key-takeaways/)) [would tell Keighley](https://web.archive.org/web/20120821020606/http://www.nbcnews.com/technology/ingame/valve-will-put-pc-games-your-tv-fall-948682):
> You'll be able to hop into the beta, click a button and see Steam reformatted for your TV and usable with a PC game controller or a mouse and keyboard if you want to play that way. There are some games that are better made for a for controller input than others so those will be the best experiences. But everything will be there. You don't have to give up all your favorite stuff once you walk from the den to your living room.

![Welcome to Steam in old BPM](/images/retrospectives/old_bpm/welcome_to_steam.webp)

Keighley would then ask Newell, "Is your strategy more to have Steam Big Picture and then if someone wants to build a device that can hook up to a TV that can run Steam, then you're all for that?"

Newell responded, "Yeah, absolutely." He would then say that the company has been working with the "hardware guys" to make said device happen. That would eventually turn out to be the Steam Link.

The public beta of the old BPM first showed up September 2012. It would then be incorporated into the stable Steam client in [December](https://www.pcmag.com/archive/valve-takes-steams-big-picture-gaming-mode-public-305625) of that year. Evidently there would be a controller-friendly Steam sale that same week.

![Old BPM System](/images/retrospectives/old_bpm/system.webp)

You might recall this was right around the same time Valve was working on the Steam for Linux client, which -- guess what? -- rolled out as stable just a few days shy of [ten years ago](https://www.gamedeveloper.com/business/steam-box-phase-one-complete-steam-s-linux-client-is-out-now). I'm not going to rehash Newell's statements about Windows 8 at the time; you all know he reported said OS as a "catastrophe."

So Valve goes all-in with Linux by making the original [SteamOS 1.0](https://www.pcgamer.com/download-steamos/), based on Debian with GNOME, and this included the BPM booting up when the PC turned on, effectively turning said PC into a living-room console. This was rolled out as beta in December 2013.

I think we can all agree that, despite Valve's efforts to push Linux gaming forward, SteamOS and Steam Machines were [as much of a catastrophe as Windows 8](https://boilingsteam.com/why-i-ended-up-ditching-steamos/). No need to explain that part any further, as this has been reported on *hundreds* of times already. On top of this, BPM was just becoming outdated; bugs were rarely ever addressed, and new features just never made it. (I can't even access the "Chat" tab at the moment since it loads indefinitely.)

![Old BPM Sonic Adventure 2 game view](/images/retrospectives/old_bpm/sa2.webp)

But hear me out: **the first public beta of SteamOS, along with its Big Picture interface, is what got me invested to Linux in the first place.** I was fascinated with the idea of being able to transform my computer into a living-room console, without ever having to touch the keyboard or mouse.

Of course, the reality was much different. As I had mentioned, BPM had its' numerous issues, and there were times where you *did* need to connect a keyboard, or a mouse at the very least, if you were running a game (which, by the way, the number of games to play was very limited, since they had to have a native Linux client) and got some kind of error along the way. There wasn't any way to close the game without M+K. It was kind of a mess. Distros like [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos/) would greatly improve Valve's work and make PC/console hybrid gaming a much more palatable experience.

Fast forward to the Steam Deck, and Valve finally has a reason to update the BPM. It's much cleaner, more modern-looking, more responsive. On top of this, this makes the work between the desktop Steam client and the Deck client more "unified," so whenever the desktop client gets an update, so will the Deck client. I recently conducted a [poll](https://mastodon.social/@linuxgamingcentral/109818344083011302) over on Mastodon, and unsurprisingly, almost *no one* is going to miss the archaic BPM. Only 7% of voters, out of 70 who participated, said that they will. It makes sense; I'm honestly glad to see it finally getting replaced with the new BPM myself.

![Old BPM controllers screen](/images/retrospectives/old_bpm/controllers.webp)

But for what it's worth, while the old BPM might have needed a lot of work, it paved the way to making PCs more controller-friendly. To this day none of the other "big guys" (EA, Ubisoft, Epic, etc.) have tried to re-invent the wheel in this area. They haven't made a ten-foot interface, let alone an operating system. So, despite all the crap I throw at Valve, I give them kudos in this area, as without their efforts, we might still be stuck with using a keyboard and mouse, even on portable systems.

CryoByte33, author of the excellent [Cryoutilities](https://linuxgamingcentral.com/posts/cryoutilities/) app for the Deck, mentioned [this](https://mastodon.cryobyte.net/@cryobyte33/109813414678391594):
> I've been using BPM since it released, almost daily. I've honestly interacted with it more than the normal client on everything from the NVIDIA Shield Tablet to an 82" QLED, and it was always rock solid. I'm really happy that it's finally getting an update since it definitely had its quirks and was a product of its time, but *I'll always have a fondness for the mildly annoying background audio while idling in old BPM* 🥲

Another Mastodon user [told me](https://fosstodon.org/@ticktok/109813703007231797) that they will miss the controller interface:
> The old one wasn't great but it was faster to navigate to different sections and the loss of number values for certain sliders and some options out right missing kinda sucks. I get that it was made for the small Deck screen first but a "less compact mode" for larger screens would be nice.

![Old BPM library](/images/retrospectives/old_bpm/library.webp)

So, there will be *some* things that will be missed. As for the old BPM ambiance, I actually have a backup of the `tenfoot` folder found in Steam's installation directory; in it contains the audio files and the BGM. That way, when old BPM finally does get retired for good, I'll have this backup as a reminder. I might actually upload it for the [Audio Loader plugin](https://linuxgamingcentral.com/posts/customize-steam-deck-theme-music-and-sfx/) so you can have that creepy ambiance running in the background on your Deck, if for some reason you wanted to be reminded of the old BPM days.

Back in October, when the Deck UI first rolled out as [beta](https://linuxgamingcentral.com/posts/steam-deck-ui-now-available-on-desktop/), I had reported that the UI navigation was terribly sluggish on NVIDIA. I'm not sure if that's the case anymore, but if it's still there, well, I'm going to feel bad for you NVIDIA users. Who knows when NVIDIA will decide to actually fix it. On AMD the UI navigation on desktop is just fine.

Why am I writing about this? Well, this article, as well as the various screenshots scattered throughout it, will serve as a reminder of the old days. When old BPM is removed entirely, it might not be possible to recover it ever again. And while I know the majority of you are looking forward to old BPM being done away with, I will actually miss it, in a way.

![Old BPM on Deck](/images/retrospectives/old_bpm/on_deck.jpg)

When will old BPM be gone for good? According to Valve's [Steam Deck client update](https://store.steampowered.com/news/app/1675200/view/3635002625425792684) on February 1st, it says nothing more than "this functionality will be removed in a future update." If I were to take a guess, it will probably be the next stable Steam desktop/Steam Deck client update. For now, you can use the `-oldbigpicture` flag if for some reason you want to keep using the old BPM.

What are your thoughts? Is there anything that you will miss from old BPM? Or can you just not wait for it to be buried in the grave? And for those of you on NVIDIA, has the UI navigation with the new BPM been improved at all? Or is it still sluggish?

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
