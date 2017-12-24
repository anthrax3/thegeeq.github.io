---
layout: post
title: Changing the Logon Screen of Windows 7.
tags: [hacks]
categories:
- blog
---
By tweaking the [Windows Registry](#), you can *change the logon screen.*

*To Open Registry:* Press `windows +r` & type `regedit` & press `enter`.

---

### THE STEPS

1. Open the Registry Editor.

2. In left pane of Registry Editor, go to `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\Authentication\LogonUI\Background`

3. Double-click the `OEMBackground DWORD key` and Set value of the key to 1.

4. Select a background image for logon screen with size less than 256 KB and rename that
   image as `BackgroundDefault`.
   
5. Copy that image, Open `My Computer` and go to `C:\Windows\system32\oobe\info\backgrounds` folder

6. Paste it and select `Copy and Replace`.
*Tips: Cut and paste the original log-on Screen image in a folder for further use.*

7. Reboot, and now your logon image would have changed.

---

**Note:** Modifying the registry can cause serious problems that may require you to
reinstall your operating system. I cannot guarantee that problems resulting from
modifications to the registry can be solved. 

---

