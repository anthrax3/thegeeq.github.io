---
layout: post
title: The Windows Registry in Windows 7
tags: [hacks]
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

###Back up the registry

Before you make changes to a registry key or subkey, I recommend that you export, or
make a backup copy, of the key or sub key. You can save the backup copy to a location
you specify, such as a folder on your hard disk or a removable storage device. If you make
changes that you want to undo, you can import the backupcopy.

1. Open the Registry Editor.

2. Locate and click the key or subkey that you want to back up.

3. Click the `File` menu, and then click `Export`.

4. In the Save in box, select the location where you want to save the backup copy to,
and then type a name for the backup file in the Filenamebox.

5. Click `Save`.

**Tips:** You must be logged on as an administrator to perform these steps. If you aren’t
logged in as an administrator, you can only change settings that apply to your user
account. Although you can back up more than just the registry key or subkey that you are
modifying, doing so adds to the size of the backup file.

---

