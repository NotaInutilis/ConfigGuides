# Asus Armoury Crate (AC) [Windows]

This guide might be either outdated quickly, or be useful for another iteration of this crapware as it tends to get a rebrand every couple of years.

not specific as name and packaged sofware can change. asus whatever
https://github.com/sammilucia/ASUS-G14-Debloating/tree/main

## 1. Turn off auto-installation in the BIOS 

Turn it off before booting on Windows so it does not auto-install and you don't have to go through the hassle of removing it.
Only possible on desktop motherboards.
This option is not present on laptops (that I know of).

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

If at this point, you have already used ACUT, you might want to reinstall AC in order to use an uninstaller (this advice is stupid, but AC is even worse).

## 2.2 Ac uninstaller

https://www.asus.com/supportonly/armoury%20crate/helpdesk_download/

## 3. Manual labor

driverstore, force delete if needed. only delete driver that is referenced by a service so as to not delete an actual useful driver.

delete all 'asus' and armoury crate services

terminal as admin:
sc.exe delete servicename
(bc driver or manual doesn't remove the service, it's inactive but le'ts clean)

scheduled tasks

### Folders

### Services
services asus + gamesdk https://rdr-it.com/troubleshooting/supprimer-un-service-sous-windows/
fichiers asus dans system32 + asus folder  qui restent après services

https://www.reddit.com/r/ASUS/comments/kddyw5/ai_suite_iii_complete_removal/
Del asus folder in program files x86 and data (might need to end task of some exe)

Deletr services, track the executable from here. if in drivers, use driver removal thingie.
C:\Windows\System32\ASUSACCI
https://github.com/lostindark/DriverStoreExplorer

### Game library

When right click on desktop
game library in registry https://www.reddit.com/r/ASUS/comments/scsc70/comment/ihwvhyq/?context=3 Computer\HKEY_CLASSES_ROOT\Directory\Background\shell\GameLibrary

## Replace
https://github.com/seerge/g-helper
some services reappear after installing driver.

https://github.com/sammilucia/ASUS-G14-Debloating/tree/main
