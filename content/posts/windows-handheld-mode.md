+++
title = "So, about that Windows Handheld Mode..."
date = 2023-04-13T19:25:48Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/windows_handheld_mode/cover.jpg"
tags = ["news", "opinion", "steam deck", "microsoft", "windows"]
keywords = ["windows handheld mode", "windows handheld gaming mode", "microsoft hackathon"]
description = "No, just no."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Supposedly Microsoft held an internal hackathon way back in September 2022. And it appears that as of today, the [video](https://www.youtube.com/watch?v=eO3uQ7B4ZXk) has been leaked. In it, the developer admits Windows' problems when it comes to having a gamepad-friendly user interface, and the steps Microsoft has been trying to work on:
> We looked at taking some of the first steps of creating a truly optimized Windows experience for the handheld PC market,
which is really just starting to grow right now due to a device called the Steam Deck.

The dev acknowleges the following issues with Windows on Deck/other PC handhelds:
- "pretty rough" with basic drivers
- lack of controller support outside of Steam
- poor display interpretation
- "trouble accessing the VRAM" -- some games won't even start
- poor optimization for the Windows virtual keyboard, as well as the UI and UX

![Windows gaming shell](/images/windows_handheld_mode/gaming_shell.webp)

Microsoft has been looking into some solutions for this:
- "Handheld sprint" by Dorothy Fang -- "she explored all the things that ultimately we want in a handheld"
- touch keyboard that "can be navigated by control"
- new taskbar "that's optimized for panels"
- the use of [Steam Deck Windows Controller Driver](https://github.com/mKenfenheuer/steam-deck-windows-usermode-driver) to allow the Deck's controls to be usable
- "Gaming Shell" by Hayden McAfee, which "gives us a quick way to launch games"

Windows Handheld Mode seeks to combine some of these projects into one solution. It will install the necessary drivers and services on your system, restart, and then it will live inside the taskbar. From there you can change "basic settings" including:
- master switch toggle - turning this off may help with issues in Steam games
- a way to customize what each button is mapped to
- power settings
- a way to check for updates

They've reported as a result of this, the controller works, and the foundation for a launcher is in place. The dev reports that their goals "seem feasible as long as we have the right specialists" and "the right expertise":
> Everyone working on this project really feels that this is something that that Windows users need, they deserve to have, and it's something that we all want to see eventually. If we can truly dial in this handheld experience we could also see new revenue streams and a lot of goodwill in the PC gaming community.

![Handheld mode options](/images/windows_handheld_mode/handheld_mode_options.webp)

It's a noble effort. I think we can all agree Windows at the moment is a pretty bad experience for PC gaming handhelds, and this effort -- provided that it actually becomes a reality -- will be one step in the right direction. Companies that refuse to support the Deck -- such as Bungie with *Destiny 2* -- their games will be playable.

Still, I see a lot of flaws with this move.

For one, it's still *Windows*. You still have all that crap running in the background -- antivirus, spyware, constant pings to Microsoft's servers while checking for updates. Using up precious RAM and battery life.

Second, I understand this project is still in its infant stages, but notice how the video doesn't address the issue with VRAM, better driver support with such things as the Deck's APU, and display orientation. Do they have any plans on addressing that?

![Hackathon results](/images/windows_handheld_mode/hackathon_results.webp)

Third, Valve has little to no control as far as driving the development of Window's AMD drivers. That would be entirely up to AMD and Microsoft. So, Valve wouldn't be able to configure the drivers in a way that are specific to the Deck or other PC handhelds.

Fourth, what about customizing the TDP limit, GPU clock speed, CPU speed, etc? Is there even going to be a Quick Access Menu for that?

And keep in mind this is a "hackathon." Meaning, something that Microsoft is just *hacking* together for a solution. Why not just use the foundation that Xbox has already provided and make an Xbox handheld instead? The controller-driven interface is already there.

![Handheld mode issues to overcome](/images/windows_handheld_mode/issues.webp)

These are the issues I can think of on top of my head. I'm sure if I were to mull it over, I could probably think of several other reasons why you should just stick to SteamOS instead of Windows.

Maybe I'm being a little too harsh I this though. I'd like to know what you think. Is Windows Handheld Mode a good idea? Would you switch over to Windows if it actually becomes a reality?

*All images used are credit of Microsoft*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
