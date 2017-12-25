---
layout: post
title: Disabling/Enabling USB Ports in Windows 7
tags: [hacks]
categories:
- blog
---
It’s really very easy to enable and disable a USB port of your Laptop and desktop
computer. Many companies disabled their employee’s laptop to prevent data threat. Also
many schools, colleges and universities block the USB ports of their computer. So, here is
the easy way to enable USB ports, access it and disable it back.

By tweaking the [Windows Registry](#), you can *disable the usb ports.*

*To Open Registry:* Press `windows +r` & type `regedit` & press `enter`.

---

### THE STEPS

1. Open the Registry Editor.

2. In left pane of Registry Editor, go to `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\USBSTOR`.

3. Right Click `Start` and Click `Modify` on right pane of Registry Editor.

4. Do one of the following:

	a) To *enable* USB ports: change the value from `4 to 3`
	
	b) To *disable* USB ports: change the Value from `3 to 4`
   
5. Copy that image, Open `My Computer` and go to `C:\Windows\system32\oobe\info\backgrounds` folder

6. Reboot, and that's it.

---

**Note:** Modifying the registry can cause serious problems that may require you to
reinstall your operating system. I cannot guarantee that problems resulting from
modifications to the registry can be solved. 

---

