+++
title = "How to Set Up Xbox Game Pass on Steam Deck"
date = 2023-04-25T19:11:55Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/xbox_game_pass/cover.jpg"
tags = ["guide", "steam deck", "xbox game pass"]
keywords = ["xbox game pass", "xbox game pass ultimate", "xbox game pass on steam deck", "xbox cloud gaming on steam deck"]
description = "Cloud streaming available right in your fingertips."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Please note this is for the **cloud** version of Xbox Game Pass. To my knowledge, it is not possible to run the native Xbox Game Pass app on Deck. Also, you will need an active **Xbox Game Pass Ultimate** subscription in order to use this.

# 1. Get a Chromium-Based Web Browser
Go to Desktop Mode. I'm assuming you have some sort of Chromium-based browser installed, but if not, install one via the Discover App. While of course Microsoft is going to suggest Microsoft Edge, we don't need to use that. Any browser that uses Google's Blink engine will work:
- Brave
- Chrome/Chromium
- Vivaldi
- Opera
- among many, *many* other browsers

In this guide, I will be using Brave.

# 2. Give the Browser Gamepad Permissions
Open up a terminal and run this:

`flatpak --user override --filesystem=/run/udev:ro com.brave.Browser`

Change `com.brave.Browser` to whatever web browser you're planning on using. So, if you wanted to add the udev permissions to Chromium, you would use `org.chromium.Chromium`.

# 3. Go to Xbox Game Pass in Your Browser and Install it as an App
Open the web browser up and direct it to the [Xbox Cloud Gaming webpage](https://xbox.com/play). Sign in to your Microsoft account if you haven't already. Inside the URL box, there should be an "Install" icon to the far right. Click on it, and select "Install".

![Install Xbox Game Pass as an app](/images/steam_deck/guides/xbox_game_pass/install_as_app.webp)

Xbox Game Pass will open in a new window. Close it for now.

# 4. Add Xbox Cloud Gaming as a Non-Steam App
Now that Xbox Cloud Gaming is installed as an app, it should be listed under "Lost & Found" within the Application Launcher. If not, scroll all the way down under the "All Applications" category. Right-click the app and select "Add to Steam".

![Add Xbox Game Pass to Steam](/images/steam_deck/guides/xbox_game_pass/add_xcg_to_steam.webp)

Xbox Cloud Gaming should now be in your Steam library.

![Xbox Cloud Gaming in Steam](/images/steam_deck/guides/xbox_game_pass/xcg_in_steam.webp)

# 5. Run the App in Fullscreen
By default, when the app is launched, it opens up in a window. We want this to be in fullscreen, so add this to the game properties:

`--start-fullscreen`

Right-click the non-Steam app -> Properties -> And append this to end of the Launch Options box. So it might look something like this:

`"run" "--command=brave" "com.brave.Browser" "--profile-directory=Default" "--app-id=some gibberish" --start-fullscreen`

![Xbox Cloud Gaming launch options](/images/steam_deck/guides/xbox_game_pass/launch_options.webp)

# 6. Get Gaming
Should be good to go! You can go back to Game Mode and launch Xbox Cloud Gaming directly from Steam. It might be worth changing the gamepad template to "Gamepad with Mouse Trackpad".

I haven't found a way to use the in-game Guide button with the gamepad, but you can still make use of it by tapping the top-left corner of the screen and then tapping the Xbox icon.

While you're at it, you may want to bring the TDP and GPU clock speeds all the way down. We're only streaming, after all.

![Hi-Fi Rush](/images/steam_deck/guides/xbox_game_pass/hifi.jpg)

# 7. (Optional) Get Artwork
While Microsoft might have you download [their artwork](https://support.microsoft.com/en-us/topic/xbox-cloud-gaming-in-microsoft-edge-with-steam-deck-43dd011b-0ce8-4810-8302-965be6d53296) and have Steam use it, there's something a bit easier: [SteamGridDB](https://linuxgamingcentral.com/posts/steamgriddb/). You can use SteamGridDB to get artwork all through Game Mode, without having to use a keyboard and mouse.

So your library might go from this:

![Xbox Cloud Gaming without artwork](/images/steam_deck/guides/xbox_game_pass/without_artwork.jpg)

To this:

![Xbox Cloud Gaming with artwork](/images/steam_deck/guides/xbox_game_pass/with_artwork.jpg)

A few weeks down the line I may have an overview of how well Xbox Cloud Gaming on Deck and desktop, so stay tuned.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
