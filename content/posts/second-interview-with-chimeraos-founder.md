+++
title = "Another Interview With Alesh Slovak - ChimeraOS Founder"
date = 2023-11-01T14:14:49Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/chimeraos_2/cover.jpg"
tags = ["interview", "chimeraos"]
keywords = ["chimeraos", "chimeraos interview", "alesh slovak", "alkazar79"]
description = "More questions for the founder of my favorite project."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
About 18 months ago I had interviewed [Alesh Slovak](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/), the founder of the fantastic ChimeraOS distribution that turns whatever device you own into a console. And, because I like the guy and his crew so darn much, I wanted to interview him again to see where things are currently standing with the development of the distro. Particularly when it comes to supporting all these new handhelds that have been a struggle keeping track of.

You'll also discover in this interview what ChimeraOS needs help with the most, what makes the team satisfied when their hard work gets put to use, and some upcoming features to look forward to, including the ability to insert physical media and make the game run through the distribution.

**TL;DR**
- Alesh usually works on the Chimera web app or reverse-engineering Steam to make ChimeraOS work with it, if he's not "trying to keep on top of things"
- favorite programming language is JavaScript "because of how easy it is to ingest and manipulate data". The Chimera web app is partially written in said language
- may one day release a game on Steam
- Aya Neo 2: "high resolution screens completely kill performance on handhelds"
- TDP controls are missing on ChimeraOS on Steam Deck, so it is recommended to stick with SteamOS
- eight core team members, 10 testers, and 34 contributors
- frustrating development aspect: constant regression fixing takes time away from working on new features. On the other hand, it's gratifying seeing people enjoy using ChimeraOS
- supporting handhelds: "the trickiest part is trying to add support for hardware that we don't have on hand"
- winesapOS: "an interesting project." Luke Short, the founder, contributed some work to ChimeraOS
- favorite handheld: the Steam Deck, since it has the best performance at native resolution, best controls and feel
- what the team needs help with: **more testers**
- things to look forward to: OOTB TDP controls, and the ability to run physical Gameboy cartridges
- Alesh would like to thank the core team members, contributors, and testers, as without them "ChimeraOS wouldn't be even half of what it is"

![ChimeraOS on ROG Ally](/images/interviews/chimeraos_2/rog_ally.jpg)
*Image credit: [Ars Technica](https://arstechnica.com/gadgets/2023/06/the-linux-coders-turning-the-rog-ally-and-other-handhelds-into-steam-deck-clones/)*

# As founder of the project, what do you primarily work on?
It is hard to pin it down exactly. I work on a lot of different things. Half the battle at this point is just trying to keep on top of things and understand what everyone else is working on so I can figure out a release plan.

When I am actually working on features it is usually related to the Chimera web app, the OS update system, or reverse engineering Steam in order to integrate with it or fix issues caused by changes in Steam client updates.

Otherwise, I do a lot of testing to make sure every aspect of the OS is working for each release. It can get quite tedious and time consuming at times.

Really, I work on whatever is needed at the time and things I understand well enough to dive in and fix. I used to know and understand every aspect of ChimeraOS, but not so much anymore. Good thing we have all those awesome contributors!

# What language is ChimeraOS primarily developed in? What other programming languages are you familiar with? Is there one in particular that's your favorite?
ChimeraOS itself is mostly just a bunch of shell scripts and configuration files. The Chimera web app is written in Python and JavaScript.

My favourite language is JavaScript because of how easy it is ingest and manipulate data and the fact that it runs in web browsers is great as that is essentially the modern application platform.

![ChimeraOS on Aya Neo 2021](/images/chimeraos_interview/chimeraos_on_ayaneo.jpeg)
*Image credit: ChimeraOS Twitter*

I would have preferred to use NodeJS/Javascript for the Chimera web app, but that would have introduced a large amount of dependencies and made the OS install size larger. Instead, I used Python which is already included in the OS.

# Have you ever dabbled with game development before?
I have dabbled in game development before, but nothing serious. I have done quite a few game jams over the years, but nothing recently.

Ever since I was a kid I have wanted to make games and it is the reason I became so interested in computers and programming. One day I would like to release a game on Steam. I have recently been inspired to get back into game development, so who knows, maybe one day I might actually release something.

# Looks like you have an Aya Neo 2. What are your thoughts on the device?
The Aya Neo 2 shares a fatal flaw with a lot of new devices: a very high resolution screen. The marketing people love bigger numbers, but high resolution screens completely kill performance on handhelds and I don't understand the trend of including them. On top of this the Aya Neo 2 also appears to have a bug where it is not possible to change to a lower resolution.

![Aya Neo 2](/images/interviews/chimeraos_2/aya_neo_2.jpeg)
*Image credit: [ChimeraOS Twitter](https://twitter.com/ChimeraOS_Linux/status/1637998657994735617)*

The buttons are also rather low quality and tend to stick. The device itself is quite comfortable to hold though and the screen does look really nice if you ignore the performance concerns.

On the whole I prefer the Steam Deck and don't use the Aya Neo 2 for anything other than testing and development of ChimeraOS.

# In an earlier version of ChimeraOS, the Steam Deck received out-of-the-box audio support. Can users expect ChimeraOS to be as feature-full as SteamOS? Or would you recommend users to continue using SteamOS on the Deck?
**SteamOS will definitely give you the best experience on the Steam Deck.** There are still a few things missing in ChimeraOS, such as TDP controls. I personally recommend sticking with SteamOS on your Steam Deck unless there is a specific reason you want ChimeraOS. I run SteamOS on my Deck as the primary OS, but mostly as a way to keep up with any changes to SteamOS.

![ChimeraOS on Steam Deck](/images/chimeraos_interview/chimeraos_on_deck.jpeg)
*Image credit: ChimeraOS Twitter*

# Last year you told me there are about three or four active contributors to ChimeraOS, with a few that come in here and there for one-off fixes/changes. Have more people come on board to help contribute to the project?
Yes! We have had a few more folks join. There are now 8 core team members, 10 testers, and 34 contributors on the Discord server according to the assigned roles. Contributors can become core team members if we see consistent contributions, a core team member nominates them, and a vote passes.

We have also formalized things a bit and I have relinquished much of my power in favour of voting on decisions by the core team members.

This has proven to be a double-edged sword. It is good to have everyone's input and opinion, but sometimes it is difficult to make the most trivial of decisions. A while back I wanted to change the slogan on our website, but we couldn't come to a consensus and I gave up, lol.

In any case, the project is doing well, and things are moving along even when I don't have time to focus on it, which is great for both myself and the community as I am no longer a bottle-neck.

# What are some of the more frustrating aspects when it comes to development of the distro? On the other hand, what are some aspects that are gratifying?
Recently it seems we are always in panic mode. There is always some regression we are trying to track down, usually from the kernel or mesa, but sometimes of our own making. This leaves little time to work on and improve the ChimeraOS specific value-adds such as the Chimera web app.

The most gratifying thing is hearing from users about how they are enjoying ChimeraOS and seeing YouTube videos featuring our work.

![Slippi on ChimeraOS](/images/distro_reviews/chimeraos/melee.jpg)

# As PC handheld gaming is becoming more and more prolific, how has the development process been as far as supporting handhelds with ChimeraOS? Has it been a struggle to keep up?
The trickiest part is trying to add support for hardware that we don't have on hand. If a technical enough user happens by and has the hardware we can sometimes guide them to getting the answers we need, but often we just have to wait.

If the issue is something common, such as screen rotation, it can be very easy to fix even without access to hardware. However, if the issue is something novel, like say the problems with the ROG Ally speakers, it can be difficult even with hardware on hand.

There are still handhelds out there that have poor support, such as the new OneXPlayer models that still have speaker troubles.

# Thoughts on winesapOS?
I have never used it, but it seems like an interesting project with a very different goal and approach. It appears to be focused on Apple hardware, which I am not personally interested in.

![Luke Short, William, and Derek](/images/interviews/chimeraos_2/group_selfie.jpeg)
*Image credit: [Luke Short](https://twitter.com/LukeShortCloud/status/1672357785454153730)*

Luke, the winesapOS founder, joined us for our anniversary event in August and recently contributed some work to ChimeraOS. It is great to have him around. Thanks Luke!

# Out of all the handhelds you own, which is your favorite, and why?
Definitely the Steam Deck. It easily has the best performance at native resolution of any handheld I own, and has the best controls and feel overall, even if there are things I don't like such as the extremely slippery thumbsticks and the difficult to use back buttons.

# What areas in particular does ChimeraOS need help with?
Testing! There are often very few of us doing testing the release candidates. There always seems to be some new issue that crops up on some particular hardware that none of the developers own. **Getting more folks helping with testing would help catch those issues earlier.**

# What are some things we can look forward to with the next version of Chimera? Any ambitious plans for the future?
There are always things brewing. One of the big things is our plan to **switch to the Steam + OpenGamepadUI overlay session by default so that we can provide working TDP controls (among other things) out of the box.**

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/chimeraos_interview/gb_operator.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

I am also excited about a feature which will allow you to run GameBoy carts directly using the [GB Operator](https://www.epilogue.co/product/gb-operator).

# Anything else you want to share with us?
I would like to give a shout out to all the core team members, contributors, and testers. ChimeraOS wouldn't be even half of what it is without all of you! Thank you so much!

Also, I finally recently organized all my handhelds, controllers and other hardware for ChimeraOS development, check it out.

![Alesh's handheld collection](/images/interviews/chimeraos_2/handhelds.jpg)
*Image credit: Alesh*

For more information regarding ChimeraOS, check out my [review](https://linuxgamingcentral.com/posts/chimeraos-review/) from earlier this year, or visit the [official website](https://chimeraos.org/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
