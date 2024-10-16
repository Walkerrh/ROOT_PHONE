
# Google Pixel and Nexus Phones
* archive does not contain 'system.sig' / archive does not contain'vendor.img' ERROR
* Stuck at Google logo (BOOTLOOP) ERROR
## Quick Fix
* Download latest platform-tools then try the flash-all.bat. If this still fails then try individually flashing each image FIX
* Could be a hardware or software issue, If software issue then try installing a custom rom from twrp then try flashing stock firmware FIX

# Samsung devcies
* ODIN: custom binary blocked by FRP lock ERROR
* SAMSUNG screen flashing Bootloop ERROR
## Quick Fix
* Remove Goofle and SAMSUNG account, also disable reactivation lock in settings FIX
* Flash boot + recovery image. If still not fixed flash latest firmware FIX

# HTC
* No download mode, No recovery mode, HTC white logo stuck ERROR
## Quick Fix
* Downlaod a file called hosd_signed.img for your phone, flash it in the bootloader mode FIX
* Fastboot flash hosd hosd_signed.img

# HUAWEI DEVICES
* Has only fastboot mode and nothing else, I accidentally messed up the firmware while rooting ERROR
## Quick Fix
* Download Huawei Firmware extractor from xda and download firmware
* flash each partition separately from fastboot mode
* If device has sdcard slot then only flash EMUI recovery partition and place firmware in sdcard then boot to EMUI recovery mode FIX

# MOTOROLA DEVICES
* How to flash firmware? QUERY
* Phone bootlaoder not unlocking ERROR
## Quick Fix
* Search on google for proper guide, Motorola devices are different and require to follow a guide FIX
* Try fastboot OEM unlock or fastboot flashing unlock / fastboot flashing unlock_critizal FIX

# LG DEVICES
* KDZ / TOT fails to flash ERROR
* Phone not supported by LGUP ERROR
## QUICK FIX
* Rename the kdz file to all capital letter then try again FIX
* Try uppercut FIX

