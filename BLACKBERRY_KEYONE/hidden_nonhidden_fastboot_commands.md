* [source link](https://forums.crackberry.com/blackberry-keyone-f445/hidden-non-hidden-fastboot-commands-list-few-other-tidbits-rambling-1114897/)

# the typical ones if you type fastboot --help I won't list all of those
* `fastboot oem unlock-go`
* `fastboot oem unlock`
* `fastboot oem lock`
* `fastboot oem device-info preflash`
* `fastboot oem enable-charger-screen`
* `fastboot oem disable-charger-screen`
* `fastboot oem off-mode-charge`
* `fastboot oem select-display-panel`
* `fastboot oem bootlog`
* `fastboot oem getvar`
* `fastboot oem mmcinfo`
* `fastboot oem info`
* `fastboot oem securewipe` - (this tries to run if you run the autoloader but gives feedback that device is in user-wipe mode so it doesn't do a full wipe. It is looking for GRS wipe mode to do the full wipe. Don't know if we can ever get to GRS wipe)
* `fastboot oem blocklist-wipe`
* `fastboot oem grswipe`
* `fastboot oem enable-usb-reset` - working
* `fastboot oem enable-usb-shutdown` - working
* `fastboot oem led`
* `fastboot oem setled`
* `fastboot oem setprd`
* `fastboot oem clear-anti-theft`
* `fastboot oem format`
* `fastboot oem gptinfo`
* `fastboot oem set-factory-mode` - (this would enable a lot but authboot permissions deny it. You can notice in bootloader screen that you are always in product mode. in /system/bin there is something called mfgUtil that won't run unless you are in factory mode.)
* `fastboot oem set-product-mode`
* `fastboot oem erase-ddr-training-primary` - working but I don't know what it does
* `fastboot oem erase-ddr-training-backup`
* `fastboot oem getvarp`
* `fastboot oem read`
* `fastboot oem mmchealth`
* `fastboot oem console`
* `fastboot oem clear-lal`
* `fastboot oem bide-storage-wipe`
