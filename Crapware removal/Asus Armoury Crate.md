# Asus Armoury Crate (AC) [Windows]

This guide might be either outdated quickly, or be useful for another iteration of this crapware as it tends to get a rebrand every couple of years. The content of the bundle as well as the names of programs, packages or drivers change even from desktop to laptop, so this guide is not very specific regarding that.

## 1. Turn off auto-installation in the BIOS 

Turn it off before booting on Windows so it does not auto-install and you don't have to go through the hassle of removing it.
Only possible on desktop motherboards: this option is not present on laptops (that I know of).

- Enter BIOS (Del or F2 at boot).
- Enter "Advance Mode" (F7).
- Navigate to "Tool" > "ASUS Armoury Crate".
- Change option "Download & Install ARMOURY CRATE app" to "Disabled".
[Official FAQ](https://rog.asus.com/support/FAQ/1043788)

## 2.1 Specialized uninstaller

Uninstall all ASUS crapware you can find (except useful drivers) using an uninstaller program.
I use [Geek Uninstaller](https://geekuninstaller.com/), you can use another like [Revo Uninstaller](https://www.revouninstaller.com/), [Bulk Crap Uninstaller](https://www.bcuninstaller.com/) or something else.

The rationale for using a specialized uninstaller program before the official Armoury Crate Uninstall Tool (ACUT) is that the uninstaller needs a program to be installed so it can remove and clean it, while the ACUT runs whether AC is installed or not.
Plus ACUT does a piss poor job at cleaning up, so running a proper uninstaller saves some of manual labor down the road.

If at this point, you have already used ACUT, you might want to reinstall AC in order to use an uninstaller (this is definitely stupid advice but you can't stop me, I'm a professionnal idiot).

## 2.2 Armoury Crate Uninstall Tool (ACUT)

[Asus Download page](https://www.asus.com/supportonly/armoury%20crate/helpdesk_download/)
Click "Show all" at the bottom on the list to actually show the whole list and the link to download the latest version of ACUT.

[Direct link to (hopefully) download the latest version of ACUT](https://dlcdnets.asus.com/pub/ASUS/mb/14Utilities/Armoury_Crate_Uninstall_Tool.zip?model=Armoury%20Crate).

ACUT runs whether AC is installed or not and clears out *some* stuff. A lot is left to do.

## 3. Manual labor

ACUT left a lot of folders, which are locked by services, which are in turn launched by scheduled tasks. And then there's drivers which might or might not be useful: on a desktop you can generally remove everything, but a laptop might need those to use some of its features (keyboard lights, fan control, keyboard shortcuts, etc.).

[Another guide with a lot of helpful information regfarding the following steps](https://github.com/sammilucia/ASUS-G14-Debloating/)

### Services

On a laptop, some stuff might break starting here. It'll be fixed later.

run debloat: it deactivates services that are with the basic driver (for laptop)

anything that has Asus, ROG, Armoury Crate and that is not deactivated should go.

delete all 'asus' and armoury crate services

track where they are so you can delete their folders

terminal as admin:
> sc.exe delete Service name

on laptop: deactivate services only, with ghelper (more options, down) or its bat script. need to keep the shitty driver (asussci2) installed with the control interface

https://github.com/seerge/g-helper/blob/main/debloat.bat
services asus + gamesdk https://rdr-it.com/troubleshooting/supprimer-un-service-sous-windows/
fichiers asus dans system32 + asus folder  qui restent après services
https://www.reddit.com/r/ASUS/comments/kddyw5/ai_suite_iii_complete_removal/
Del asus folder in program files x86 and data (might need to end task of some exe)

Deletr services, track the executable from here. if in drivers, use driver removal thingie.
C:\Windows\System32\ASUSACCI
https://github.com/lostindark/DriverStoreExplorer

### Scheduled tasks

### Folders

services are not locking them

`C:\Program Files (x86)\` `C:\Program Files\` `C:\ProgramData` `C:\Users\your name here\AppData`

Asus, ROG, Armoury Crate

### Drivers and AC replacement for laptop

be careful not to delete useful stuff. use a search engine if unsure

driverstore, force delete if needed. only delete driver that is referenced by a service so as to not delete an actual useful driver.
Armoury Crate Control Interface
Remove the AC driver and replace it with whatever Asus System Control Interface v3+. 

Once everything has been cleared out, 
https://github.com/seerge/g-helper
some services reappear after installing driver. 

### Game library

AC adds a "Game library" entry in the desktop right click menu which isn't removed by any uninstaller. It is removed by deleting the following key in the registry:
> Computer\HKEY_CLASSES_ROOT\Directory\Background\shell\GameLibrary
[Source](https://www.reddit.com/r/ASUS/comments/scsc70/comment/ihwvhyq/)