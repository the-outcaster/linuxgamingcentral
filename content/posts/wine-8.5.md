+++
title = "Wine 8.5 Upgrades VKD3D to 1.7, Adds Dark Theme"
date = 2023-04-01T02:48:34Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.5.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator"]
description = "Along with bug fixes for Deus Ex, Ultimate Race Pro, Fair Strike, and other games."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.5 is now available. Included in this release is the upgrade to [VKD3D 1.7](https://www.phoronix.com/news/Wine-VKD3D-1.7). A WinRT dark theme can be configured, there's better error handling in the IDL compiler, cleanups in IME support, and 21 bug fixes.

Bug fixes are as follows (gaming fixes are in bold):
 - **#44547  Deus Ex: invisible War v1.2 crashes when using the hotkey to quickload a saved game**
 - **#54701  Ultimate Race Pro crashes after intro movies**
 - **#47326  Fair Strike fails to map joystick due to IDirectInputDevice8 SetActionMap being a semi-stub.**
 - **#53704  Bible Black ~La Noche de Walpurgis~ won't start**
 - **#53794  Sins of the Solar Empire Rebellion (Gog 1.975.1) crashes on unimplemented function concrt140.dll.?_CheckTaskCollection@_UnrealizedChore@details@Concurrency@@IAEXXZ**
 - **#54679  Conspiracy's Clean Slate 64K demo crashes due to HLSL shader compilation failure**
 - #46562  Notepad++ 7.6.3 crashes when searching twice and first time found results
 - #53981  Chromium broken sandbox due to GetSecurityInfo giving access denied
 - #54560  mscoree:mscoree - test_loadpaths_execute() sometimes gets directory creation errors
 - #54618  VARA FM crashes on unimplemented function pdh.dll.PdhVbGetDoubleCounterValue
 - #54640  Treecomp listviews and possibly other widgets are not drawn
 - #54675  Chocolatey OpenSSH installer fails
 - #54687  LibreVR Revive fails to run (CertGetNameStringW with dwType=CERT_NAME_ATTR_TYPE and pvTypePara missing additional fallbacks)
 - #54691  reg.exe:copy, reg.exe:delete, reg.exe:export, reg.exe:import & reg.exe:query (+32-bit reg.exe:add) - The 64-bit tests fail due to ERROR_ACCESS_DENIED errors in Wine
 - #54702  ldp.exe crashes when attempting to add, delete, modify, or compare an entry without a name
 - #54707  adsldp:ldap - test_DirectorySearch() fails on Windows and Linux
 - #54710  imm32:imm32 - test_ImmEscape() fails in the Korean locale on Windows
 - #54711  imm32:imm32 - test_ImmGetProperty() fails in the Korean locale on Windows
 - #54724  LDAP bind over SSL to a server and port that do not support SSL hangs forever
 - #54727  LDAP Explorer (LEX) throws an exception when attempting to connect over SSL
 - #54729  wine build fails with bison 3.0.5

See the patch notes on [WineHQ](https://www.winehq.org/announce/8.5).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
