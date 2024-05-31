+++
title = "NVIDIA Open-Sources Their GPU Kernel Drivers, Plus a New Beta Driver with Gamescope Support"
date = 2022-05-12T08:32:34-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvidia/cover.jpg"
tags = ["news", "nvidia"]
keywords = ["gamescope", "nvidia", "open-source"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Well, chances are you've probably come across this already in the headlines yesterday, but if not, NVIDIA is gradually taking strides towards the FOSS philosophy, starting with their GPU kernel modules. They're now open-source and available on [GitHub](https://github.com/NVIDIA/open-gpu-kernel-modules), under a dual GPL/MIT license. All the documentation is there too, including how to compile it and what CPU architectures are supported. Linux kernels 3.10 and newer are supported.

Wow. About time. It's good news; ever try to downgrade your NVIDIA driver on Linux and end up borking your system? Hopefully contributions by the community will make removing or downgrading easier. It should also mean distros can now more easily include NVIDIA drivers by default with their distros. Their [blog post](https://developer.nvidia.com/blog/nvidia-releases-open-source-gpu-kernel-modules/) mentions that this is "a significant step toward improving the experience of using NVIDIA GPUs in Linux, for tighter integration with the OS and for developers to debug, integrate, and contribute back."

I'd really like to think what's going on in Torvald's mind right now. He's still probably taking this with a grain of salt. And in all honesty, I am too. I can't help but feel like there's some sort of catch here. Yes, it's great that NVIDIA is finally being a bit more friendly on the Linux side of things, but for being a walled-garden for so many years...I've got mixed feelings.

![nvidia open-source gpu kernel driver diagram](/images/nvidia/diagram.png)
*Image credit: NVIDIA blog post*

At the same time, a new driver came out: [515.43.04 beta](https://www.nvidia.com/download/driverResults.aspx/187834/en). Here's the changelog:
```
- Added support for the VK_EXT_external_memory_dma_buf and VK_EXT_image_drm_format_modifier Vulkan extensions. To use this functionality, the nvidia-drm kernel module must be loaded with DRM KMS mode setting enabled. See the DRM KMS section of the README for guidance on enabling mode setting.
- Changed nvidia-suspend.service, nvidia-resume.service, and nvidia-hibernate.service to use WantedBy= rather than RequiredBy=dependencies for systemd-suspend.service and systemd-hibernate.service.This avoids a problem where suspend or hibernate fails if the NVIDIA driver is uninstalled without disabling these services first.
See https://github.com/systemd/systemd/issues/21991
If these services were manually enabled, it may be necessary to update their dependencies by running sudo systemctl reenable nvidia-suspend.service nvidia-resume.service nvidia-hibernate.service
- Interlaced modes are now disabled when active stereo is enabled.
- NVIDIA X Server Settings will now display the quit confirmation dialog automatically if only there are pending changes that need to be manually saved. The corresponding configuration option to control the appearance of the quit dialog was thus also removed.
- Removed the warning message about mismatches between the compiler used to build the Linux kernel and the compiler used to build the NVIDIA kernel modules from nvidia-installer. Modern compilers are less likely to cause problems when this type of mismatch occurs, and it has become common in many distributions to build the Linux kernel with a different compiler than the default system compiler.
- Updated nvidia-installer to skip test-loading the kernel modules on systems where no supported NVIDIA GPUs are detected.
- Updated nvidia-installer to avoid a race condition which could cause the kernel module test load to fail due to udev automatically loading kernel modules left over from an existing NVIDIA driver installation. This failure resulted in an installation error message "Kernel module load error: File exists".
- Updated the RTD3 Video Memory Utilization Threshold (NVreg_DynamicPowerManagementVideoMemoryThreshold) maximum value from 200 MB to 1024 MB.
```
Supposedly this means this new driver supports Gamescope. You can use NVIDIA's image scaler via this [pull request](https://github.com/Plagman/gamescope/pull/488).

*Cover image credit: NVIDIA blog post*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
