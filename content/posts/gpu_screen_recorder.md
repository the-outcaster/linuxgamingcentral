+++
title = "App Spotlight: Easily Record Videos on NVIDIA with GPU Screen Recorder"
date = 2022-04-14T22:01:08-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/gpu_screen_recorder/cover.jpg"
tags = ["app spotlight", "screen recorder"]
keywords = ["gpu screen recorder", "nvidia"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Don't get me wrong; OBS is a great tool to record your screen, regardless of what operating system your using. But you might have noticed something while trying to record gameplay on Linux: the CPU gets taxed quite a bit, even when using the NVENC encoder on NVIDIA GPUs. As a result, the framerate drops.

Introducing a new, open-source screen recorder: [gpu screen recorder](https://git.dec05eba.com/gpu-screen-recorder/about/). The developer of this project claims this significantly reduces CPU usage, "at around 0%" due to keeping the window image on the GPU and sending it directly to the video encoding unit with CUDA. [GamingOnLinux](https://www.gamingonlinux.com/2022/04/a-developer-made-a-shadowplay-like-high-performance-recording-tool-for-linux/) had also recently touched on this.

I recorded some footage of the [*Metroid Prime* remastered mod](https://youtu.be/2EVy0yo0-Wc) with this. The result came out pretty good! File size was fairly large at 1.5 GB (about 16 minutes of footage, so roughly 1 GB for every 10 minutes) at High quality, but I didn't notice any slowdowns playing the game while recording.

![gpu screen recorder gtk stream](/images/gpu_screen_recorder/stream.jpg)

What I appreciate about this screen recorder besides the reduced CPU usage is how dead simple it is to use. On the [GTK frontend](https://git.dec05eba.com/gpu-screen-recorder-gtk/about/), all you have to do is select a window (or record the entire desktop), adjust the resolution, framerate, and quality, and if you want to include audio as well just select your audio playback device from the dropdown menu. From here you can stream to YouTube or Twitch, record, or save a "replay" at a default duration of 30 seconds.

If you prefer a [CLI-based version](https://git.dec05eba.com/gpu-screen-recorder/about/) instead, you can do that. You could run this, for example: `gpu-screen-recorder -w $(xdotool selectwindow) -c mp4 -f 60 -a "$(pactl get-default-sink).monitor" -o test_video.mp4`

Keep in mind the following caveats, at least for the time being:
- this only works on NVIDIA GPUs (Intel and AMD support are planned later down the road)
- recording the entire desktop requires a GPU with NvFBC support (Tesla and Quadro GPUs support this, others can be patched with [nvidia-patch](https://github.com/keylase/nvidia-patch) or [nvlax](https://github.com/illnyang/nvlax))
- mouse cursor is currently invisible

![gpu screen recorder gtk record](/images/gpu_screen_recorder/record.jpg)

Interested in trying it out? On Arch you can get it from the [AUR](https://aur.archlinux.org/packages/gpu-screen-recorder-gtk-git) (this is for the GUI version). Otherwise you'll have to clone the repo and run the `build.sh` script. Dependencies needed include `gtk3`, `libx11`, `libxrandr`, and `libpulse` (which, I believe, is in addition to the dependencies needed for the CLI version: `glew`, `glfw3`, `cuda`, `ffmpeg`, `libxcomposite`, `libpulse-simple`).

I definitely recommend giving gpu screen recorder a spin if you want an easy-to-use interface while also keeping your game's framerate intact while recording.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
