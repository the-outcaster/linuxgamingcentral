+++
title = "Increase Power on AMD GPUs (and Fix Random Game Crashing)"
date = 2023-01-18T18:18:33Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/guides/amd_gpus/corectrl.png"
tags = ["guide", "amd"]
keywords = ["amd", "amd 6700 xt", "corectrl", "linux", "gpu overclocking"]
description = "Here's how you can unlock more advanced power settings for your AMD GPU."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**UPDATE (1/19/2023): this guide has been updated towards step 3 when it comes to regenerating the bootloader config. (Regenerating config is dependent on distro used, not the GRUB version.)**

A few days ago I talked about the [6700 XT](https://linuxgamingcentral.com/posts/moving-from-nvidia-to-amd/) and how much more bliss it has given my everyday Linux life in contrast to using a NVIDIA GPU. Thanks to some of the comments I got on the article, I've discovered it's possible to increase the number of watts supplied to the GPU. This should increase game performance. Another commenter also brought out that it's also possible to fix the random game crashing that can occur due to the fan not running properly. So I will document both of these steps!

By default, the 6700 XT can only get up to 186 W:

![6700 XT default max power limit](/images/6700xt/corectrl.png)

However, we can increase this to **213 W**. The fix is very simple: we just need to [append `amdgpu.ppfeaturemask=0xffffffff` to our GRUB configuration file](https://gitlab.com/corectrl/corectrl/-/wikis/Setup#full-amd-gpu-controls). Appending this parameter will also allow us to have "full control" of the GPU; we'll have more advanced options to choose from in CoreCtrl as far as voltage, GPU min/max frequency, and memory speed.

*Disclaimer: this will effectively overclock your GPU. If you experience erratic behavior with your system (i.e. frequent game crashing), restore the GRUB file back to what it was before!*

# 1. Make a Backup of GRUB
If your system is using GRUB, you should have a config file named `grub` in `/etc/default/`. Make a backup of this file before proceeding:

`sudo cp /etc/default/grub /etc/default/grub.bak`

This way in the event your system somehow breaks on the next restart (which it shouldn't), or are experiencing issues getting games to run without crashing, you'll be able to restore the backup file.

# 2. Edit GRUB Configuration
Open up your preferred text editor as root and open up the GRUB config file. I like to use gedit:

`sudo gedit /etc/default/grub`

Somewhere in that file should be a `GRUB_CMDLINE_LINUX_DEFAULT=` line, followed by a pair of quotation marks. In my case it looks like this:

`GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`

Literally all we have to do is append `amdgpu.ppfeaturemask=0xffffffff` before the closing quotation mark. So my line would look like:

`GRUB_CMDLINE_LINUX_DEFAULT="quiet splash amdgpu.ppfeaturemask=0xffffffff"`

Save the file and close the text editor.

# 3. Regenerate Bootloader Configuration
On Debian-, Ubuntu-, and Arch-based systems, regenerate the bootloader config file with:

`sudo grub-mkconfig -o /boot/grub/grub.cfg`

If you're using a Fedora-based distro or openSUSE, use:

`sudo grub2-mkconfig -o /boot/grub2/grub.cfg`

# 4. Restart and See the Changes
Restart the computer and you should be good to go. If you haven't already, install [CoreCtrl](https://gitlab.com/corectrl/corectrl).

Under your GPU, select "Advanced" from the dropdown menu next to Performance mode. Not only can I increase the GPU power to 213 W, I also have some other options available to me.

![CoreCtrl with more advanced GPU options](/images/guides/amd_gpus/advanced.png)

Click "Apply" and "Save" on the top-right corner of the window to save your changes. Note that you *may* need to restart the computer again if you notice some odd behavior with games (some games crashed on me the first couple of runs).

Observe the difference in framerates between 186 W (what the card could max out at previously) and 213 W:

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/6700xt/186w_vs_213w.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Okay, so the numbers may be a little hard to see (I keep my video file sizes small). But clearly at 213 W the GPU is squeezing in more power for a higher framerate. There are some moments where the game can only get 60 FPS at 186 W, but *90* at 213 W!

# 5. (Optional) Fix Random Game Crashing
Your GPU's fan may not run at all on the default profile with CoreCtrl...which can cause the game to crash from overheating. In CoreCtrl, select "Curve" from the dropdown menu next to Ventilation. Check off "Fan start" as well. Hopefully your fan should be running now.

![Curve ventilation in CoreCtrl](/images/guides/amd_gpus/curve.png)

The fan might appear to be 0 RPM in the screenshot, but believe me, the fan runs when running a game now. I played *Crisis Core* remake for several hours after making this change and haven't experienced a random crash since then.

Special thanks to Anonymous and Lancaban for their comments!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
