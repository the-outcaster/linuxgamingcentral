+++
title = "Wine May Soon Work Natively With Wayland"
date = 2023-03-02T13:44:19Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/wine_wayland.webp"
tags = ["news", "wine", "wayland"]
keywords = ["wine wayland", "collabora"]
description = "Keyword is *may*, though."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Back in December, Alexandros Frantzis from the Collabora team [detailed](https://www.collabora.com/news-and-blog/news-and-events/wine-on-wayland-2022-updatye-more-games-more-apps-more-fun.html) the progress with Wine working natively on Wayland, rather than using XWayland as a workaround. Improvements made to Wine Wayland include:
- support for cross-process rendering -- allows Chromium/CEF applications to run
- Chrome works without using any flags, and is fully GPU-accelerated on both OpenGL and Vulkan
- enhanced support for the linux-dmabuf v4 Wayland protocol -- allows compositors to dynamically send info about optimal formats/modifiers

Collabora also posted a [video](https://www.youtube.com/watch?v=lZ-MK72Kyp8) showcasing Wine Wayland's progress. In it are several games -- some of which are 3D -- running fairly well, including *Call of Duty 2*, *Phoning Home*, *Factorio*, and more. They also demonstrate LibreOffice and Chrome with accelerated cross-process rendering.

Now this work is finally being [upstreamed](https://gitlab.winehq.org/wine/wine/-/merge_requests/2275), and is in the process of being reviewed. If the merge is approved, Wine will get native Wayland support. Brodie Robertson [noted](https://www.youtube.com/watch?v=K9IRHD6gVhA) that some games have issues running with XWayland, and these issues will supposedly no longer exist once the game is run with Wine Wayland.

While we're waiting for this to get merged (if it ever does; seems like there are some [concerns](https://www.winehq.org/pipermail/wine-devel/2021-February/181338.html) from other Wine developers about the driver being feature-incomplete), if you're feeling adventurous you can [compile](https://www.winehq.org/pipermail/wine-devel/2020-December/178575.html) the Wayland driver yourself. But be aware, this seems very experimental; out there be dragons.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
