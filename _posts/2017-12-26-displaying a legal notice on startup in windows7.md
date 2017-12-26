---
layout: post
title: Displaying a Legal Notice on startup in Windows 7
tags: [hacks]
categories:
- blog
---
If your PC has multiple users then you can display legal notice to every user before they
login to your PC. *This legal notice will be displayed at every startup just before the*
*Desktop is loaded*. Using this you can tell your friends about the do’s and don’ts in your
computer when they login in your absence.

By tweaking the [Windows Registry](#), you can *display a legal notice.*

*To Open Registry:* Press `windows +r` & type `regedit` & press `enter`.

---

### THE STEPS

1. Open the Registry Editor.

2. In left pane of Registry Editor, go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion`.

3. On the right side pane look for `legalnoticecaption`, double click on it and enter the
   desired *Legal Notice Caption*.
   
4. Next below this look for `legalnoticetext` and enter the desired *Legal Notice Text*. The
   legal notice text can be up to a page in its size so that it can include a *set of do’s and
   don’ts for your computer*.
   
5. After you does this just restart your computer and upon the next startup you can see
   the legal notice information for your computer.

---

**Note:** Modifying the registry can cause serious problems that may require you to
reinstall your operating system. I cannot guarantee that problems resulting from
modifications to the registry can be solved. 

---

