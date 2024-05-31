+++
title = "Xbox Game Pass: Is It Worth Your Time?"
date = 2023-06-22T20:45:42Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/xbox_game_pass/review/cover.webp"
tags = ["game review", "xbox game pass", "steam deck"]
keywords = ["xbox game pass", "xbox game pass ultimate", "xcloud", "xbox cloud gaming", "xbox game pass review", "xbox game pass on steam deck", "xbox game pass on linux desktop"]
description = "It's going to depend on a few things."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I have to admit, being able to stream an Xbox to your device, whether it be a Steam Deck or a Linux desktop, is pretty neat. It's something that Sony's tried to do with PlayStation Now, but their selection of games isn't *anywhere* near as decent. And far be it from Nintendo to allow you to play any of their games outside of their native hardware, nevermind stream them.

This is possible thanks to Xbox Game Pass. Or, more accurately, Xbox Cloud Gaming (formerly xCloud), that is a part of the Xbox Game Pass Ultimate subscription. For $15 a month, you get access to nearly *400* games. And these aren't just any kind of games: some of them are the big, AAA hits. Some of them are available to stream the same day they're released in physical format.

Some titles you may find noteworthy -- at least at the time of writing this -- include:
- *Among Us*
- *Assassin's Creed* series
- *Banjo and Kazooie* series
- *Cassette Beasts*
- *Coffee Talk* series
- *DIRT 5*
- *DOOM* series, including *Eternal*
- *Dead Cells*
- *Deep Rock Galatic*
- *Fortnite*
- *Forza Horizon 4* and *5*
- *Gears of War* series
- *GoldenEye 007*
- *Grounded*
- *Hot Wheels Unleashed*
- *Halo* series
- *Hi-Fi Rush*
- *High on Life*
- *Minecraft Dungeons* and *Legends*
- *Monster Hunter Rise*
- *Persona* series
- *Psychonauts* series

![Family-friendly titles on XCG](/images/xbox_game_pass/review/family_friendly_titles.webp)

And besides this still *plenty* of others; from some of your favorite indie hits, to family-friendly titles like *New Super Lucky's Tale*, strategy, simulation, shooters, fighting games, etc. Some games have DLC included. Needless to say, I think there will be at least one game that someone will like. Though there's not many of them, there's even some games from the original Xbox and Xbox 360 generations that are available to stream.

New games come in every month. For example, this month, *Need for Speed Unbound*, *Amnesia: The Bunker*, *Car Mechanic Simulator 2021*, and a couple of other lesser-known titles were added. A caveat that you have to be aware of, however, is that as some games come in, others leave. Right now, under the "Leaving soon" category, is *Road 96*, *Matchpoint: Tennis Championships*, *Empire of Sin*, and a few others.

The question arises, though: is it worth paying the $15/month for?

# General Experience
It's real easy to get started with Xbox Cloud Gaming. Just use a Chromium-based browser, sign-in to your Microsoft account ([sign up](https://login.live.com/) if you don't already have one), get yourself an active [Xbox Game Pass Ultimate subscription](https://www.xbox.com/en-US/xbox-game-pass/ultimate), plug in your gamepad, direct your browser to [Xbox Cloud Gaming](https://www.xbox.com/en-US/play), and get going.

It's a small detail, but I like the looks and sounds of the interface. You can browse through the catalog of games with your gamepad, and the browser will actually play the sound effects of the main menu on the Xbox console as you're scrolling. Install Xbox Cloud Gaming as an app, put it in fullscreen, and it almost feels like you own an actual Xbox. It's even more nostalgic with the achievements -- the same graphics and sound effects play as on console. You can browse games by category, or use the search function at the top. You can quickly jump to the Search bar with the Y button.

![NFS Unbound on XCG](/images/xbox_game_pass/review/game_description.png)

Upon selecting a game, pressing the A button will bring up more details for that game. Here you can see the description of the game, the ESRB rating, the languages the game supports, and a few other specifics. You can then press the green "PLAY" button when you're ready to stream the game. Give it a few moments, and then the game will boot. When you exit the game, it will appear under the "Jump back in" section at the top of the main menu. Pressing A will stream the game without needing to see the description page.

On desktop, pressing the Guide button on your gamepad will bring up the Xbox menu. Here you can see your Xbox "friends" list, start a party (invite people to join your session), see your achievements, and quit the game. On Deck, you'll need to tap the top-left part of the screen to make the Xbox icon visible, then tap it to bring it up. If you click or tap the three-dotted button next to the Xbox icon, you can enter or exit fullscreen, turn your mic on or off, or provide feedback to Microsoft. You'll also be asked for feedback when quitting a game -- whether you thought the experience was good or bad. You'll then be asked what specifically you liked or you didn't. Of course, providing feedback is always optional.

![Hi-Fi Rush achievements](/images/xbox_game_pass/review/achievements.webp)

Note that, in addition to logging into your Microsoft account, some games will need one more login. For example, you won't be able to play *Redfall* without logging in to your Bethesda account. You won't be able to play *Battlefield 2042* without logging in to your EA account. *Sigh*, yeah, always leave it to companies like EA to throw in that monkey wrench.

# Linux Desktop
If your browser is installed as a Flatpak, you'll need to run the necessary command to give it udev permissions. Otherwise, your gamepad won't work. For instance, if you're using the Brave browser, you'd need to run:

`flatpak --user override --filesystem=/run/udev:ro com.brave.Browser`

`com.brave.Browser` would need to be replaced with the appropriate name for whatever other browser you may be using.

Xbox controller? Who said you needed an Xbox controller? I mean, the in-game button glyphs will obviously be Xbox-oriented, but there's nothing stopping you from using a PlayStation gamepad or any other gamepad for that matter. I played several games with my DualSense, and I had no problems whatsoever. In fact, if you add Xbox Cloud Gaming as a non-Steam app, you can then configure your controller's gyro to mimic the analog stick. Useful for first-person shooters. Xbox controllers don't have that feature.

![New Super Lucky's Tale on XCG](/images/xbox_game_pass/review/nslt.webp)

So how's the streaming experience itself? Not bad. I'm using a wired Ethernet connection, and to date I have yet to find audio desyncs or any sort of connection struggle. As far as input latency is concerned, well, I don't have all the tools necessary to "measure" that. From the naked eye, however, it's not very noticeable. I was able to play the rhythm-heavy *Hi-Fi Rush* and land my combos in sync with the beat of the tune without much trouble. I am using my DualSense via a wired connection, though, so using a gamepad via Bluetooth may be a different story.

The one caveat I will throw in here, however, is if you're using a monitor with any resolution higher than 1080p, your video quality is going to suffer. On my 1440p monitor the video quality, while not terrible, isn't that great either. The game looks slightly pixelated; you can tell with the screenshots I've posted here. Last year I had reported that [users had to use an agent switcher on Linux](https://linuxgamingcentral.com/posts/xbox-game-pass-quality-throttled-on-linux/) and trick Xbox Cloud Gaming into thinking that their browser was using Windows 10 in order for the video quality to improve. I can now say that hack is no longer required. I have compared screenshots of my browser with and without the Windows 10 user agent string on Brave, and there is absolutely no difference whatsoever. This is likely due to Microsoft releasing a ["set of performance improvements...via browser on Linux and ChromeOS devices."](https://www.gamingonlinux.com/2022/11/microsoft-upgrades-xbox-cloud-gaming-for-linux-and-chromeos/) Still, 1440p, and certainly 4K, is a no go.

There's also the so-called ["clarity boost"](https://www.gamespot.com/articles/how-to-use-clarity-boost-for-xbox-cloud-gaming/1100-6498433/) that Microsoft tried to offer exclusively for their Edge browser. Fact: again, during my testing, I have noticed no difference at all between Brave and Edge. Maybe there's a specific setting that needs to be toggled in Edge to activate this feature, but I haven't found it anywhere. So, not really any point in using Edge if anyone thinks there is, well, an *edge* using this browser over others.

![Hi-Fi Rush on XCG](/images/xbox_game_pass/review/hifi_rush.webp)

# Steam Deck
The process of getting Xbox Cloud Gaming working on Steam Deck is a little more involved than desktop. In addition to having a Chromium-based browser installed, you'll also need to run the appropriate terminal command in Desktop Mode to get the integrated controls to work, install Xbox Cloud Gaming as an app, add it to Steam, and append a fullscreen parameter in the launch options. Still, it's not that hard; have a look at my [guide](https://linuxgamingcentral.com/posts/how-to-set-up-xbox-game-pass-on-deck/) if you want to get that set up.

Since the Deck's resolution is only limited to 800p, video quality obviously isn't an issue here. The quality looks just fine. If you're planning on connecting the Deck to an external monitor, don't use a resolution higher than 1080p. Anything higher than that, and the picture will look like crap.

![Forza Horizon 5 on Deck via XCG](/images/xbox_game_pass/review/on_deck.jpg)

Even through Wi-Fi, I've had very little fuss over the connection breaking. The connection has always been very stable for me. So, whether you want to use a wired connection or wireless, you shouldn't have any issues with either one.

# The Positives
Games these days take up large portions of your hard drive. Ones that take over 100 GB of space aren't all that uncommon. Depending on your connection speed, they may take several hours to download as well. Not only this, but updates happen as well, day-one patches, and all that jazz. Taking up more of your hard drive *and* your time to download. This is true whether you're a PC gamer or you're on console.

Xbox Cloud Gaming eliminates that. You have *instant* access to 300+ titles, and they're ready to play in just a few moments. No need to wait several hours for a game or update to download. They're all immediately playable and automatically have the latest updates installed.

There aren't that many exclusives, but, if you only play on Linux and Steam Deck, you have access to titles that otherwise aren't able to be played on these platforms. *Fortnite*, for example.

![Supraland 6 Inches Under on XCG](/images/xbox_game_pass/review/supraland.webp)

How about cost? You give your wallet a little bit of breathing room this way...depending on how long you choose to keep your subscription active. If I had the choice between paying a full $70 on a day-one release on Steam, or playing the same game through Xbox Cloud Gaming that becomes available to stream the same day, I'm going with the latter. Yeah, the video quality might not be as good, but I'm paying *less than a quarter* of the price for that game than a native Steam release.

# The Drawbacks
The monthly subscription service is probably the biggest drawback. Paying $15 for one month isn't all that bad. But if you keep your subscription active, you've paid $60 by the end of four months. That's the same price of owning a AAA game on Steam that you can keep forever. In 12 months, you paid $180. That would get you three games. If you're playing a lot of different games on XCG, perhaps the money would be worth it. But if you're solely focused on maybe two or three games out of the entire catalog and playing them for several months, you would be spending more money on those games than just owning them on Steam.

Another disadvantage is, you can't download these games. You need to have a constant Internet connection in order to play. So, unless you've got a phone plan with unlimited tethering data, you're not going to be able to tame that turtle in *ARK* while you're on the go with the Deck.

![Minecraft Legends on XCG](/images/xbox_game_pass/review/minecraft_legends.webp)

Say there's a game that you *really* like. You enjoy that game, and you've invested a lot of time with it. And then you log in one day, only to discover it's now in the "Leaving soon" category. Ouch. What are you going to do? Are you now going to be forced to buy the game somewhere else in order to keep playing it? And what are you doing to do about your save data? Can you resume where you left off if you own the game on Xbox? That will already be out of the question if you buy the game on PlayStation or Steam; you can't export your save data.

A few other things that I can think of:
- bad video quality at 1440p and above, as I had alluded to earlier
- you can't add mods to any games

# The Choice is Up to You
There's both good things and bad things that come with XCG. Instant access to a wide variety of titles, no need to download any updates, games that are available to you that may not be playable on Linux/Steam Deck. On the other hand, you also have to consider the fact that you're paying a fairly hefty $15/month (and the price is unfortunately [only going to get higher](https://www.pcgamer.com/xbox-is-hiking-game-pass-prices-but-sparing-pc-game-pass-at-least-for-now/)), you need an Internet connection at all times, a game that you may be heavily invested in may soon leave, bad video quality at 1440p and above, lack of mod support.

![Coffee Talk on XCG](/images/xbox_game_pass/review/coffee_talk.webp)

Whether you want to use XCG is going to depend on how many games you're willing to play, whether you're willing to spend that monthly fee, whether you're okay with needing a stable Internet connection at all times, what resolution you're planning on using, whether you're okay without having mod support, whether you're okay with basically being locked in to the Xbox platform as far as save data is concerned. Personally, I won't be keeping my subscription active. I'd rather own my games on Steam, be able to mod them, play them natively on my hardware at 1440p, and not keep paying $15/month. I have enough monthly bills to pay as it is.

**TL;DR**

The good:
- plenty of titles to choose from, from a wide variety of genres
- instantly playable; no need to download or install the games themselves, updates, or DLC
- works great on Deck
- games that may not run on Linux or Steam Deck, such as *Fortnite*, are playable
- access to a few original Xbox and Xbox 360 titles

The not-so-good:
- Internet connection required at all times
- $15/month subscription quickly adds up, and this price is going to get higher soon
- not meant for resolutions higher than 1080p
- games may get added every month, but others get removed
- save data can't be exported
- no mod support

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
