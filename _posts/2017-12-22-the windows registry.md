---
layout: post
title: The Windows Registry
tags: [hacks, window-7 hacks, registry hacks]
categories:
- blog
---
[Windows Registry](#) *is a database* used to store information that is necessary to configure
the system for one or more users, applications and hardware devices and it keeps record of
the settings of all the Software installed in Computer including Operating System

*To Open Registry:* Press `windows +r` & type `regedit` & press `enter`.

Windows Registry contains **Five Hives** and *hives contain Keys and Sub keys and their respective Values.* 

---

### THE HIVES 
 
1. **HKEY_CLASSES_ROOT:** The information that is stored here makes sure that the
   correct program opens when you open a file by using Windows Explorer.

2. **HKEY_CURRENT_USER:** Contains the configuration information for the user who is
   currently logged on. The user’s folders, screen colors, and Control Panel settings
   are stored here.

3. **HKEY_LOCAL_MACHINE:** Contains configuration information particular to the
   computer (for any user).
   
4. **HKEY_USERS:** Contains all the actively loaded user profiles on the computer.
   *HKEY_CURRENT_USER* is a subkey of HKEY_USERS.

5. **HKEY_CURRENT_CONFIG:** Contains information about the hardware profile that is
   used by the local computer at system startup.
   
---

### THE KEYS

1. **Binary Value (REG_BINARY):** Raw binary data. Most hardware component
   information is stored as binary data and is displayed in Registry Editor in hexadecimal
   format.

2. **DWORD Value (REG_DWORD):** Data represented by a number that is 4 bytes long (a 32-bit integer).
   Can also contain binary, hexadecimal, or decimal format.
   
3. **Expandable String Value (REG_EXPAND_SZ):** A variable-length data string. This data
   type includes variables that are resolved when a program or service uses the data.

4. **String Value (REG_SZ):** A fixed-length text string.

5. **Multi-String Value (REG_MULTI_SZ):** Values that contain lists or multiple values in a
   form that people can read are generally this type.
   
---

**Note:** Modifying the registry can cause serious problems that may require you to
reinstall your operating system. I cannot guarantee that problems resulting from
modifications to the registry can be solved. In future posts, I will be tweaking 
the registry. Use the information provided at your own risk.

---

