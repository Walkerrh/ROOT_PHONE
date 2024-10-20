
* [firmware.mobi](https://firmware.mobi/)
* [Oneplus](https://oneplus.com/)
* [oneplus community offical firmware](https://community.oneplus.com/thread/836441)
* [OnePlus 6: Unlock Bootloader](https://community.oneplus.com/thread/836005)
* [RECOVERY 11 12 13 UNOFFICIAL TWRP for OnePlus 6 & 6T](https://xdaforums.com/t/recovery-11-12-13-unofficial-twrp-for-oneplus-6-6t.4382121/)
* [TWRP for OnePlus 6 (enchilada)](https://twrp.me/oneplus/oneplus6.html)
* [(OnePlus 6)(ROM)(OTA)(Oxygen OS) Mirrors for official Oxygen OS ROMs and OTA updates](https://xdaforums.com/t/oneplus-6-rom-ota-oxygen-os-mirrors-for-official-oxygen-os-roms-and-ota-updates.3792244/)
* [TWRP for OnePlus 6 (enchilada)](https://twrp.me/oneplus/oneplus6.html)
* [How To Flash Twrp Recovery & Root Oneplus 6, Oneplus 6T, Oneplus 7 & Oneplus 7T](https://www.youtube.com/watch?v=cAUAYQoMOto&ab_channel=BitTech)
  
* [Root Oneplus 6 & 6T OxygenOS 11.1.2.2 - Step by Step Guide](https://www.youtube.com/watch?v=FSStkSVcBRk&ab_channel=TechiBee)
  * [](https://techibee.in/root-oneplus-6-6t-running-oxygenos-11-1-2-2-step-by-step-guide/)
  * [TWRP OnePlus 6 Series Files](https://sourceforge.net/projects/oneplus-6-series/files/TWRP/)
  * [Magisk](https://github.com/topjohnwu/Magisk)
  * [SDK Platform Tools release notes](https://developer.android.com/tools/releases/platform-tools)

use dot image to boot the erb then install the installer



Prerequisite :
* A Windows PC.
* Properly Installed Adb/fastboot drivers: Follow this guide
* TWRP Recovery zip & Image File for Oneplus 6 & 6T: Download  
* Oneplus 6 or 6T Device Running Android 11.
* Magisk XDA : Download/ Direct link of Magisk 24.1 (always use latest version)

# Steps to Root Oneplus 6 & 6T running OxygenOS 11.1.2.2
1. SETTINGS – ABOUT PHONE – TAP BUILD NUMBER 7 TIMES UNTIL YOU SEE A POP OF DEVELOPER OPTION
2. SETTINGS – SYSTEM – DEVELOPER OPTIONS
3. ENABLE OEM UNLOCK
4. ENABLE ADVANCE REBOOT
5. ENABLE USB DEBUGGING
6. Install ADB DRIVERS
7. a new folder will be created in C: Drive
8. place the downloaded files (TWRP image) file in ADB folder
9. connect device to the PC
10. open the command prompt in ADB folder
11. Unlock Bootloader by using the power button
12. check if the device is properly connected `fastboot devices`
13. serial number should show
14. unlock the Bootloader by using the command `Fastboot OEM Unlock`
15. the command will get a Warning message
16. select unlock bootloader
17. repeat steps 1 -> 5
18. boot device in fastboot mode
19. `fastboot boot <Recovery-Name>.img` Eg: "fastboot boot twrpxx.img"
20. if no Error then the device will boot into TWRP
21. Now transfer all the Downloaded Files inside internal Storage (Twrp zip & Magisk)
22. flash Twrp Zip for Once reboot recovery
23. After booting recovery flash magisk & reboot device
24. enjoy



## Fix Fastboot/Adb & Qualcomm drivers not detecting on Windows 10/11
1. download the latest Fastboot driver
2. extract the ZIP file
3. connect your device to the PC while the phone is in Fastboot / Bootloader screen
4. run `adb reboot bootloader`
5. Windows + X
6. Device Manager
7. expand the “Portable” or “Other devices” menu
8. find your Android device mentioned
9. yellow sign next to it which means Fastboot is not working
10. right-click on it and click on “Update Driver”
11. click on “Browser my computer for drivers“
12. click on “Browse”
13. select the fastboot driver folder
14. Device Manager will automatically find the android_winusb.inf file and apply the update
15. it will install the Fastboot drivers
16. name will change to “Android Phone -> Android Bootloader Interface“
17.  open the command prompt window and run the `fastboot devices`

## Fastboot Drivers Not Installing on Windows 10
1. Open the Start Menu and click on “Restart” while holding the “Shift” key. Release the Shift key when you see the “Please Wait” screen.
2. boot into the Advanced Recovery screen
3. Troubleshoot -> Advanced Options -> Startup Settings -> Restart.
4. “Startup Settings” window will open up
5. press “7” or “F7” to open Windows 10 without Driver Signature Enforcement.
6. Disable driver signature enforcement

## Let me pick from a list of available drivers
1. double-click on “Android Phone“
2. choose “Android Bootloader Interface”
3. Fastboot drivers will be successfully installed
4. move the “Platform Tools” folder or “Minimal ADB” folder inside the “C” drive. Fastboot does not detect devices from other locations
