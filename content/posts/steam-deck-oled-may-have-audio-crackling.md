+++
title = "PSA: Your Steam Deck OLED May Have Audio Crackling Issues on the Headphone Jack"
date = 2023-12-05T22:11:54Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/headphone_jack/cover.jpg"
tags = ["psa", "steam deck", "steam deck oled", "troubleshooting", "headphone jack"]
keywords = ["steam deck oled", "steam deck", "steam deck oled audio crackling", "steam deck oled headphone jack"]
description = "Insulating the screws on the audio PCB may provide a workaround."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Some users have reported that using wired headphones on the Steam Deck OLED can result in [audio crackling](https://github.com/ValveSoftware/SteamOS/issues/1235). I have not personally encountered this issue on my own unit (maybe the audio PCB is designed a little differently on the Limited Edition).

There's one of two things that you can do if this is happening on your end. One is by simply getting in touch with Steam Support so you can RMA the device. Another is by applying some DIY tricks if you'd rather not wait for United Radio to fix it. Note that the latter is only a workaround and *not* a solution -- **you may experience Wi-Fi and Bluetooth issues after doing this.**

If you want to fix it yourself, you'll have to take the back plate off. Towards the top-right is the audio PCB. There are two screws holding the PCB in. Disconnect the battery cable. Unscrew the screws. Use insulated/shrink tape on the PCB where the screw holes are. Put the screws back in. The tape will keep the screws from touching the ground of the PCB.

![Steam Deck OLED audio PCB with taped screws](/images/steam_deck_oled/headphone_jack/audio_pcb_with_tape.webp)
*Image credit: u/Chiny_1990*

See the post from L0rdEnki on [GitHub](https://github.com/ValveSoftware/SteamOS/issues/1235#issuecomment-1840599310) or one of the threads on [r/SteamDeck](https://www.reddit.com/r/SteamDeck/comments/188fxu1/fix_audio_cracklingstatic_on_35mm_headphone_jack/) for more info.

Thanks to **sonic2kk** for bringing this to my attention!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
