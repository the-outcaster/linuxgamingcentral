+++
title = "How to Add Your Own Background Music and Sound Effects to your Steam Deck"
date = 2023-02-15T15:53:42Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/adding_custom_bgm_and_sfx/cover.jpeg"
tags = ["guide", "steam deck", "audio loader"]
keywords = ["steam deck custom audio", "steam deck sound effects", "steam deck background music"]
description = "Want to add your own sound effects or background music to your Deck? Here's how."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Keyboard and mouse highly recommended!

# 1. Get Decky Loader and Audio Loader
Get Decky Loader [here](https://github.com/SteamDeckHomebrew/decky-loader). After that's installed you can get Audio Loader through the shopping icon on the top-right from the Quick Access Menu.

![Audio Loader in Decky store](/images/steam_deck/guides/adding_custom_bgm_and_sfx/audio_loader_in_store.jpeg)

# 2. (Optional) Enable SSH to your Deck
I recommend setting up SSH on your Deck to allow remote access from your desktop. This will make your life a lot easier -- you can work on the BGM/SFX on your desktop, then wirelessly transfer the files to your Deck whenever you're ready to test.

You can read [this post](https://shendrick.net/Gaming/2022/05/30/sshonsteamdeck.html) for more info, but in a nutshell, to start the SSH daemon on your Deck, first make sure you have a sudo password set up, then run:

`sudo systemctl start sshd`

The service can be stopped at any time with:

`sudo systemctl stop sshd`

Beware that enabling SSH on your Deck can potentially expose the device to attackers if they have remote access to it, so it's best to shut it off when you're done.

# 3. Add BGM
We'll start with custom BGM, since it's easier to work with than SFX. A couple of guidelines as to what you should select for the BGM:
- should be lyricless
- it's *background* music; not a general music player
- try to refrain from anything that's heavy-hitting; ideally it should be ambiance and/or instrumental
- BGM should loop well, without sounding too abrupt whenever it repeats
- BGM needs to be in **MP3** format

You will also likely need to have an audio editor available on hand, such as Audacity, to trim the audio as needed, or ensure it loops properly.

On your Deck, navigate to `~/homebrew/sounds/`. Create a new folder. Name it to whatever you like; preferably something along the same lines as the title of the music you want to add. For this tutorial, I'm going to go with something retro: [Lower Brinstar from *Super Metroid*](https://www.youtube.com/watch?v=Q9ieYLHc1fQ). So I'm going to name my folder "Lower Brinstar".

![Lower Brinstar folder in ~/homebrew/sounds/](/images/steam_deck/guides/adding_custom_bgm_and_sfx/lower_brinstar_folder.png)

Go inside the folder you just made. Create a new file and name it `pack.json`. Add the following lines to it:

```
{
  "name": "Pack Name",
  "description": "Use this field to describe the pack.",
  "author": "GitHubUsername",
  "version": "v1.0",
  "manifest_version": 2,
  "music": true,
  "ignore": [],
  "mappings": {}
}
```

Now modify the values. In my case, I would name "name" to "Lower Brinstar (Super Metroid)", the "description" to "Lower Brinstar from Super Metroid. ©1994-2019 Intelligent Systems Co., Ltd., Nintendo Co., Ltd. & Nintendo R&D1. All Rights Reserved.", and "author" to "Linux Gaming Central". My JSON file would look like this:

```
{
  "name": "Lower Brinstar (Super Metroid)",
  "description": "Lower Brinstar from Super Metroid. ©1994-2019 Intelligent Systems Co., Ltd., Nintendo Co., Ltd. & Nintendo R&D1. All Rights Reserved.",
  "author": "Linux Gaming Central",
  "version": "v1.0",
  "manifest_version": 2,
  "music": true,
  "ignore": [],
  "mappings": {}
}
```

Now here's the fun part. Get your MP3 and put it in the same folder as the JSON file. Name it to `menu_music.mp3`. An easy way of ripping sound tracks from YouTube, if there isn't a download available, is by using [yt-dlp](https://github.com/yt-dlp/yt-dlp). So, if I were to download the Lower Brinstar theme, I would run this:

`yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=Q9ieYLHc1fQ`

Obviously, if the music isn't yours, make sure you give proper credit to whoever made it in the "description" field.

![Lower Brinstar thumbnail](/images/steam_deck/guides/adding_custom_bgm_and_sfx/lower_brinstar.webp)

Now open the MP3 file with an audio editor (Audacity is a great example). The first thing we need to do is **lower the amplification by 10 decibels.** Select the entire track -> Effect -> Amplify -> Amplification: **-10** -> OK.

![Lowering amplification via Audacity](/images/steam_deck/guides/adding_custom_bgm_and_sfx/lowering_amplification.png)

In the case of the Lower Brinstar theme I just downloaded, it doesn't need to be seven minutes long. We can actually trim this down to around one minute and 52 seconds. **Trim the length of the theme so that it's just long enough to go around once. Make sure there are no fade ins or outs.** Copy this track, paste it right next to it, and play it back to test how well the loop effect sounds. If the loop effect sounds natural, you know you edited the track right. 

![Trimming BGM in Audacity](/images/steam_deck/guides/adding_custom_bgm_and_sfx/trimmed_audio.png)

Delete the copy of the track, and export the project as an MP3 file. Again, make sure the file name is `menu_music.mp3` and put inside the folder we created earlier.

![Properly named BGM file](/images/steam_deck/guides/adding_custom_bgm_and_sfx/properly_named_bgm_file.png)

If everything went well your newly created theme should be available in the dropdown menu for Audio Loader in the QAM. Select it, test to make sure the volume is okay, that it's not too loud or too quiet, and that it loops nicely. Make changes as needed.

# 4. Add SFX
SFX will be a little more tricky, as a lot of memorization is needed to keep track of which sound file does what. And hopefully the sound effects that you want will be available as a nice .zip file, labeled with the names of each sound effect. **Sound effects need to be in WAV format.**

Add a new folder in `~/homebrew/sounds/`. Name it to whatever you want. I'll go with "Super Metroid SFX". Inside the folder, create a `pack.json` file, just like with custom BGM. Add the following contents to it:

```
{
  "name": "Pack Name",
  "description": "Use this field to describe the pack.",
  "author": "GitHubUsername",
  "version": "v1.0",
  "manifest_version": 2,
  "music": false,
  "ignore": [
    "bumper_end.wav",
    "confirmation_negative.wav",
    "confirmation_positive.wav",
    "deck_ui_achievement_toast.wav",
    "deck_ui_bumper_end_02.wav",
    "deck_ui_default_activation.wav",
    "deck_ui_hide_modal.wav",
    "deck_ui_into_game_detail.wav",
    "deck_ui_launch_game.wav",
    "deck_ui_message_toast.wav",
    "deck_ui_misc_01.wav",
    "deck_ui_misc_08.wav",
    "deck_ui_misc_10.wav",
    "deck_ui_navigation.wav",
    "deck_ui_out_of_game_detail.wav",
    "deck_ui_show_modal.wav",
    "deck_ui_side_menu_fly_in.wav",
    "deck_ui_side_menu_fly_out.wav",
    "deck_ui_slider_down.wav",
    "deck_ui_slider_up.wav",
    "deck_ui_switch_toggle_off.wav",
    "deck_ui_switch_toggle_on.wav",
    "deck_ui_tab_transition_01.wav",
    "deck_ui_tile_scroll.wav",
    "deck_ui_toast.wav",
    "deck_ui_typing.wav",
    "deck_ui_volume.wav",
    "pop_sound.wav",
    "steam_at_mention.m4a",
    "steam_chatroom_notification.m4a",
    "ui_steam_message_old_smooth.m4a",
    "ui_steam_smoother_friend_join.m4a",
    "ui_steam_smoother_friend_online.m4a"
  ],
  "mappings": {}
}
```

Modify the values accordingly.

[The Sounds Resource](https://www.sounds-resource.com/) is a great place to find sound effects from various games. And guess what? There's a sound pack available for [*Super Metroid*](https://www.sounds-resource.com/snes/supermetroid/sound/46395/), so I'll be using this in congruence with the Lower Brinstar theme.

![Sounds resource for Super Metroid](/images/steam_deck/guides/adding_custom_bgm_and_sfx/sounds_resource.png)

Download the archive and extract it. This is where things get a bit convoluted. You'll need to rename each sound file to the name of the sound file found in `~/.local/share/Steam/steamui/sounds/`. So, for instance, if you wanted to replace the sound file when navigating across most UI options, you would rename your sound file to `deck_ui_misc_10.wav`, then place this file in the new folder you created.

You can use this as a guideline for the SFX you want to replace:
- `deck_ui_achievement_toast.wav` - Played when a user unlocks an achievement in a Steam game.
- `deck_ui_bumper_end_02.wav` - Played when attempting to navigate and being unable to move further.
- `deck_ui_default_activation.wav` - Played when selecting most interactable objects.
- `deck_ui_hide_modal.wav` - Played when exiting most pop-ups.
- `deck_ui_into_game_detail.wav` - Played when opening a game's details page.
- `deck_ui_launch_game.wav` - Played when launching a game.
- `deck_ui_misc_10.wav` - Played when navigating through most areas.
- `deck_ui_navigation.wav` - Played when navigating through specific areas (ex. Settings).
- `deck_ui_out_of_game_detail.wav` - Played when exiting a game's details page.
- `deck_ui_show_modal.wav` - Played when a pop-up appears.
- `deck_ui_side_menu_fly_in.wav` - Played when opening the Steam or Quick Access menus.
- `deck_ui_side_menu_fly_out.wav` - Played when exiting the Steam or Quick Access menus.
- `deck_ui_slider_down.wav` - Played when decreasing a slider.
- `deck_ui_slider_up.wav` - Played when increasing a slider.
- `deck_ui_switch_toggle_off.wav` - Played when toggling off a toggle.
- `deck_ui_switch_toggle_on.wav` - Played when toggling on a toggle.
- `deck_ui_tab_transition_01.wav` - Played when switching between tabs (ex. Library views).
- `deck_ui_toast.wav` - Played when a toast appears at the bottom-right corner of the UI.
- `deck_ui_typing.wav` - Played when typing on the keyboard.
- `deck_ui_volume.wav` - Played when confirming the volume setting in Settings.
- `steam_at_mention.m4a` - Played when mentioned in a group chat.
- `steam_chatroom_notification.m4a` - Played when receiving a group chat message.
- `ui_steam_message_old_smooth.m4a` - Played when receiving a private chat message.
- `ui_steam_smoother_friend_join.m4a` - Played when a friend runs a game or software.
- `ui_steam_smoother_friend_online.m4a` - Played when a friend goes online on Steam.

Once you've renamed a sound file and put it in the SFX folder you made earlier, you can then cross the filename in the "ignore" list in the `pack.json` file. So if you added a custom sound effect for `deck_ui_achievement_toast.wav`, you can remove this line in the "ignore" list. Keep doing this for each sound effect that you replace. Lines that remain inside the "ignore" list will be ignored and will use the vanilla sound effect.

When you're done, test the sound effects on your Deck by selecting it from Audio Loader. Make sure the volume isn't so loud that the speakers "pop"; you may need to decrease the amplification on the sound effect so it doesn't create this effect.

At the end of the day my `pack.json` file would look like this:

```
{
  "name": "Super Metroid SFX",
  "description": "Sound effects from Super Metroid. ©1994-2019 Intelligent Systems Co., Ltd., Nintendo Co., Ltd. & Nintendo R&D1. All Rights Reserved.",
  "author": "Linux Gaming Central",
  "version": "v1.0",
  "manifest_version": 2,
  "music": false,
  "ignore": [
    "bumper_end.wav",
    "confirmation_negative.wav",
    "confirmation_positive.wav",
    "deck_ui_message_toast.wav",
    "deck_ui_misc_01.wav",
    "deck_ui_misc_08.wav",
    "deck_ui_tile_scroll.wav",
    "pop_sound.wav",
    "steam_at_mention.m4a",
    "steam_chatroom_notification.m4a",
    "ui_steam_message_old_smooth.m4a",
    "ui_steam_smoother_friend_join.m4a",
    "ui_steam_smoother_friend_online.m4a"
  ],
  "mappings": {}
}
```

# 5. Upload for Others to Enjoy
Check the [submission criteria](https://docs.deckthemes.com/#/Submission) page before submitting your work. If the developers approve, it will be available on the Audio Loader store.

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/steam_deck_custom_sfx/super_metroid_sfx.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

If you want to use *Super Metroid* BGM/SFX, you can go to my [GitHub repo](https://github.com/linuxgamingcentral/super-metroid-bgm-and-sfx-for-deck) and follow the instructions there. I also have [*Metroid Prime* SFX/BGM](https://github.com/linuxgamingcentral/metroid-prime-sfx-and-bgm-for-deck) as well. I will likely submit these packs soon so it will be easier to install them.

I'll have a video to accompany this article soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
