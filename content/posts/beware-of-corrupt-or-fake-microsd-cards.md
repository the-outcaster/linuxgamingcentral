+++
title = "Corrupt MicroSD Card? Your Steam Deck (Or Amazon) May Be to Blame"
date = 2022-12-28T19:02:30Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/microsd_card/format_error.jpg"
tags = ["psa", "microsd card", "steam deck", "amazon"]
keywords = ["microsd card", "fake microsd card", "amazon", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
You might have bought a MicroSD card for your Deck. Over time, however, you might notice the speeds start to slow down. In fact, they might slow down so much that they are practically useless. I'm not talking about opening up your Deck with the card still inside (*cough* [Liam from GOL](https://linuxgamingcentral.com/posts/interview-with-liam-from-gol/#anything-else-youd-like-to-share-with-us) *cough*). Bad MicroSD cards are usually caused by one of two things:

1. If you bought the card on Amazon, [it might be a fake](https://www.reddit.com/r/NintendoSwitch/comments/dz3h6z/amazon_still_selling_fake_microsd_cards_even_if/)
2. If you formatted the card on the Deck earlier this year (before the end of May), the Deck did a full format as opposed to a quick format, causing your card to be overwritten too much

As reported on the Reddit thread, the OP bought a SanDisk 200GB Ultra MicroSDXC UHS-I on Amazon. Turns out it was actually only 32 GB. Here's what they had to say:
> Due to sheer laziness on Amazon's part, the counterfeit cards get mixed right in with the real ones. The negative side of this is that you are getting at most 1/6 of what you paid for, the card will likely be slower than typical, your game data will 100% be corrupted if you use these cards due to their overwriting nature, and it takes three hours or so to test these large cards.

![Steam Deck attempting to rescue a MicroSD card](/images/steam_deck/microsd_card/rescuing.jpg)

Keep in mind that thread was posted three years ago. But there's still a risk of buying a fake card from Amazon -- as indicated by a [more recent report](https://steamcommunity.com/app/1675200/discussions/0/3269060419624832750/) -- even if it's from a legit retailer like SanDisk, Lexar, Samsung, etc. Your best bet would be to [test](https://github.com/JonMagon/KDiskMark) the card once you get it to confirm if it's the actual size and speed as advertised, and if it's not, simply return it.

But let's say your card *is* legit. There is still a limit in regards to how often the MicroSD card can be written into. And once the card has reached that limit, it will slow down; eventually to the point where it will become unusable. So if you plugged it into your Steam Deck and formatted it in Game Mode, there's a chance that the Deck did a *full* format as opposed to a quick format. Full formats write much more data to the card as opposed to quick format -- the card will therefore reach this "unwritable" state more quickly.

Valve changed the formatting behavior of the MicroSD card from full to quick with the [SteamOS 3.2 update](https://steamcommunity.com/games/1675200/announcements/detail/3297210455204145217) that shipped in late May. According to the interview from [The Verge](https://www.theverge.com/23499215/valve-steam-deck-interview-late-2022), this simple change fixed a lot of cards from reaching end-of-life. But if you formatted your card prior to this update, this may explain why your card is behaving erratically.

![KDE Partition Manager formatting a MicroSD card](/images/steam_deck/microsd_card/kde_partition_manager.jpg)

So here's some tips:
- you may want to buy a MicroSD card from somewhere *other* than Amazon to avoid getting a counterfeit card. I also have a [guide](https://linuxgamingcentral.com/posts/microsd-card-buying-tips/) for getting the right type of card
- test the speed and size of the card with something like [KDiskMark](https://github.com/JonMagon/KDiskMark) to make sure you got what you paid for. Send the card back otherwise
- the Deck should use a quick format in Game Mode nowadays, but if you're feeling paranoid about using it you may want to format the card in Desktop Mode with KDE Partition Manager instead (you may want to opt for [btrfs](https://linuxgamingcentral.com/posts/save-disk-space-on-deck-with-steamos-btrfs/) as the file system for it as well, to preserve disk space)
- it's safer to shut the Deck down prior to changing the MicroSD card as opposed to when it's on; the Deck may be in the middle of writing to the card if you're running games on it or downloading game updates (cards are hot-swappable, but better safe than sorry)

If you have a bad card, whether it be fake or it got corrupted somehow, don't lose hope. You can actually send your card to Valve and see what they can do about it. In regards to how that works, I'm not sure; I'd imagine it's similar to [how the Deck RMA process works](https://linuxgamingcentral.com/posts/how-the-steam-deck-rma-process-works/). I have a friend who may actually do that; I will document the process if he does.

*All images are credit of [Ruineka](https://linuxgamingcentral.com/posts/hp-dev-one-review-by-chimeraos-dev/).*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
