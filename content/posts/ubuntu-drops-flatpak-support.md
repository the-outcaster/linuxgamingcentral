+++
title = "Ubuntu Drops Flatpak Support"
date = 2023-02-22T16:01:30Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ubuntu/cover.webp"
tags = ["news", "canonical", "ubuntu", "flatpak"]
keywords = ["canonical", "ubuntu", "ubuntu drops flatpak", "ubuntu won't support flatpak", "ubuntu 23.04"]
description = "Starting with 23.04."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As the months and years go by, Canonical is making increasingly controversial decision after decision. Snaps, Amazon search results, Unity...the list goes on. And here they're pulling off yet another decision that will likely turn some users away: they won't have out-of-the-box Flatpak support with Ubuntu 23.04. This will include Ubuntu itself as well as the various "flavors," such as Kubuntu.

kewisch, community engineering manager at Canonical, explained in the [Ubuntu Discourse forum](https://discourse.ubuntu.com/t/ubuntu-flavor-packaging-defaults/34061):
> Going forward, the Flatpak package as well as the packages to integrate Flatpak into the respective software center will no longer be installed by default in the next release due in April 2023, Lunar Lobster. Users who have used Flatpak will not be affected on upgrade, as flavors are including a special migration that takes this into account. Those who haven’t interacted with Flatpak will be presented with software from the Ubuntu repositories and the Snap Store.

They go on to say "when a new packaging technology is provided by default, there is an expectation that the distribution provides community support and is invested in contributing to development to resolve issues. This creates fragmentation instead of focusing on improving the technologies chosen for the distribution."

While I appreciate the transparency, rather than just slipping it in without letting anyone know, I also feel this will actually *create* more fragmentation rather than closing the gap. Almost *no one* wants to use Snaps; even Ubuntu's own kernel developer, Ben Romer, [admits](https://linuxgamingcentral.com/posts/interview-with-canonical-dev/#you-had-alluded-to-snaps-as-being-unpopular-why-is-there-so-much-controversy-behind-snaps-from-your-viewpoint-what-are-the-advantages-of-this-packaging-system) that they're "quite divisive" and "a mixed bag." As a result, if you don't want to use Snaps, the only packaging solution that you'll be left with starting on Ubuntu 23.04 is the native .deb package. If you want Flatpak support, you're going to have to go out of your way to install it again.

You can read kewisch's [post](https://discourse.ubuntu.com/t/ubuntu-flavor-packaging-defaults/34061) for more details. Also, I recommend checking out the [interview](https://linuxgamingcentral.com/posts/interview-with-canonical-dev/) that I had with one of the Ubuntu kernel developers a few months ago; he's very honest about how he feels about the whole Snap situation.

What are your thoughts on this? Do you think this was a good decision on Canonical's part? Or do you think it will cause even *more* fragmentation?

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
