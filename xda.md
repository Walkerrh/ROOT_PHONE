If your device is rooted, you need to unroot it first.

If you have stock recovery only, you can use ADB (Android Debug Bridge).
*------------------------------------------------------*
adb devices (check connection)
adb reboot-bootloader
fastboot devices
fastboot format userdata (Attention! All your data will be lost!)
fastboot update /path_to_zip/Disable_Dm-Verity_ForceEncrypt_09.02.2018.zip
*------------------------------------------------------*
If you need Magisk systemless root:
fastboot update /path_to_magisk/Magisk-v17.1.zip
*------------------------------------------------------*
fastboot reboot
 
