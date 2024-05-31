+++
title = "Steam to Ditch Google Analytics in Favor of Their Own Solution"
date = 2023-05-16T13:10:50Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam/traffic_update.webp"
tags = ["news", "steam"]
keywords = ["steam leaving google analytics", "steam traffic reporting", "google analytics", "google analytics 4"]
description = "\"We’ve come to realize that Google’s tracking solutions don't align well with our approach to customer privacy.\""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday a new [blog post](https://store.steampowered.com/news/group/4145017/view/3719453992486109638?l=english) from the Steamworks Development team was published, going over "the future of traffic reporting on Steam."

They emphasize "player privacy first":
> Steam will continue to not share personally identifiable information. This approach to privacy means that some trade-offs have been made along the way that limits how specific some reporting can be. In most cases, it simply means that any traffic sources that are below a threshold of volume will get reported as "other". We intentionally don't collect or store demographic information about users such as age, gender, or race.

Developers will now be able to get a geographic breakdown and "better identification of external sources" when they observe traffic coming to their game on Steam. Additionally, Steam's UTM system has been updated with increased tracking percentage, one-day conversion tracking, and a few other areas.

But what's probably the best news out of this post is **Steam is no longer using Google Analytics.** They will be using their own solution in the summer, rather than using the new replacement Google is using -- Google Analytics 4:
> As time has gone on we’ve come to realize that Google’s tracking solutions don't align well with our approach to customer privacy, and so with the migration to GA4 we’ve made the decision to end our support of Google's analytics systems on Steam. Instead, we're focused on building the most useful parts of aggregated reporting into Steam itself.

So, if a company as prolific as Valve won't use Google Analytics, it's all the more reason [why you should look into alternatives](https://linuxgamingcentral.com/posts/plausible-analytics-and-why-you-should-use-it/) if you host your own website.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
