---
layout: post
title: Enabling Superfast Shutdown in Windows 7
tags: [hacks]
categories:
- blog
---
By tweaking the [Windows Registry](#), you can *achieve a superfast speed*
*for shutting down your system.*

*To Open Registry:* Press `windows +r` & type `regedit` & press `enter`.

---

### THE STEPS

1. Open the Registry Editor.

2. In left pane of Registry Editor, go to `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control`

3. In the right pane, right click on `WaitToKillServiceTimeout` and click on `Modify`.

4. Type in a number between 2000-20000 (2-20 seconds) and click on OK.
   *NOTE: The default time is 12000 (12 seconds).*

5. Close regedit.

6. *After rebooting* (restart) Windows the new settings will take effect. The time to wait
   for terminating services will be faster and shutdown won’t drag on forever.
   
7. If you have problems with programs from your computer shutting down too
   quickly, then repeat the above steps and increase the time (Step 4) a bit.
   .
---

**Note:** Modifying the registry can cause serious problems that may require you to
reinstall your operating system. I cannot guarantee that problems resulting from
modifications to the registry can be solved. 

---

