+++
title = "NVIDIA Driver 525.60.11 Adds a Fix for GNOME, Supports Dynamic Boost on AMD Laptops"
date = 2022-11-28T13:39:13-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/nvidia/cover.jpg"
tags = ["news", "software update", "graphics driver update", "nvidia"]
keywords = ["nvidia", "nvidia 525.x"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
New driver update for NVIDIA GPUs went out today. Included in this update are the support of Dynamic Boost for notebooks with AMD CPUs, improved performance of PRIME render-offloaded apps, the removal of stutter when moving windows in GNOME, a fix for *Marvel's Spider-Man Remastered*, and tons of other changes.

**Features** include:
- Added support for Dynamic Boost on notebooks with AMD CPUs.
- Added support for the EGL_MESA_platform_surfaceless extension.
- Implemented support for over-the-air updates in the Proton and Wine NVIDIANGX build. This feature is disabled by default and can be enabled by setting the "PROTON_ENABLE_NGX_UPDATER" environment variable to a value of "1".
- Added a new CUDA Debugger implementation for Pascal and newerarchitectures as a part of the driver package: libcudadebugger.so (previously released separately as "CUDA GDB Developer Preview").

**Updates:**
- Improved the performance of PRIME render-offloaded applications.
- Updated the nvidia-settings control panel to prevent the creationof display layouts that exceed hardware size limitations when using the SLI Mosaic configuration page, and to display a warning if such a layout is created manually in the Display Configuration page.
- Removed the hard dependency on GTK 2 when building nvidia-settingsfrom source. nvidia-settings may now be built with support for GTK 2 only, GTK 3 only, or both GTK 2 and GTK 3.
- Updated the open kernel modules to support Quadro Sync, Stereo,rotation in X11, and YUV 4:2:0 on Turing.
- Updated an error message that nvidia-installer displays when kernelheader files cannot be found to print full paths for the missing files.
- Updated nvidia-installer to use "command -v" in place of depending on"which" to determine the availability and location of certain tools.
- Updated the Vulkan driver so that the following extensions no longerdepend on nvidia-uvm.ko being loaded at runtime:
  * VK_KHR_acceleration_structure
  * VK_KHR_deferred_host_operations
  * VK_KHR_ray_query
  * VK_KHR_ray_tracing_pipeline
  * VK_NV_cuda_kernel_launch
  * VK_NV_ray_tracing
  * VK_NV_ray_tracing_motion_blur
  * VK_NVX_binary_import
  * VK_NVX_image_view_handle
- Updated nvidia-installer to allow use of the "--add-this-kernel"feature by non-root users.
- Updated nvidia-installer to display a more accurate progress bar whenbuilding the kernel modules.
- Updated nvidia-installer to display a warning message if a VulkanICD loader is not detected.
- Reworked nvidia-installer's support for DKMS: the kernel modules willnow be optionally registered with DKMS after the installer has already built and installed them on its own. nvidia-installer will now register the kernel modules with DKMS by default when the dkms(8) utility is detected on the system.

**Bug fixes** are as follows:
- Fixed a bug which caused Dynamic Boost to not engage on certain AmpereGPU based notebooks.
- Fixed a regression that prevented Warp & Blend from working correctly.
- Fixed a bug that resulted in stutter when moving windows in GNOME.
- Fixed a bug which caused suspend to fail on systems running GNOME 3as a Wayland compositor with NVreg_PreserveVideoMemoryAllocations enabled.
- Fixed a bug in the Vulkan driver which could lead to corruption ingeometry and tessellation control shaders.
- Fixed a bug that caused nvidia-settings to find incorrect fan speedranges on some GPUs.  Lower-level layers of the driver protected the hardware from programming incorrect fan speeds, so the symptom was only incorrect reporting.  Now, reporting in nvidia-settings matches what actually gets programmed in hardware.
- Fixed a regression in 515.76 that caused blank screens and hangs whenstarting an X server on RTX 30 series GPUs in some configurations where the boot display is connected via HDMI.
- Fixed a bug where Marvel's Spider-Man Remastered would sometimes crashwith Xid 13 errors on Turing and later.

Patch notes can also be seen on [NVIDIA's website](https://www.nvidia.com/download/driverResults.aspx/196733/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
