
* [developer.android](https://developer.android.com/)
* [android stuido](https://developer.android.com/studio)
* [SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools)
  * for windows
    * using winget
      * open terminal/powershell
      * `winget install Google.PlatformTools`
    * using android
      * open the platform tools folder
      * right click open PowerShell windows here
      * ./adb devices

# SCRCPY
* [GitHub link](https://github.com/Genymobile/scrcpy)
* [connect device](https://github.com/Genymobile/scrcpy/blob/master/doc/connection.md)
  * via serial
    * `scrcpy --serial=0123456789abcdef`
    * `scrcpy -s 0123456789abcdef   # short version`
    * `scrcpy --serial=192.168.1.1:5555 # the serial is the ip:port if connected over TCP/IP (same behavior as adb)`
  * via usb
    * `scrcpy --select-usb`
    * `scrcpy -d   # short version`
  * via TCP/IP
    * `scrcpy --select-tcpip`
    * `scrcpy -e   # short version`
    * `scrcpy --tcpip=192.168.1.1:5555`
    * `scrcpy --tcpip=192.168.1.1        # default port is 5555`

# Enable developer mode in android
* settings -> about -> tap build number 6 times

# Enable usb debugging
1. enable developer mode
2. system -> advanced -> developer options -> enable USB debugging

# Turn PowerShell into command promt
1. open PowerShell
2. `cmd`

# adb commands
* `./adb devices`
* `adb devices`
* `adb reboot`
* `adb reboot bootloader`
* `adb reboot download`
* `adb rebbot recovery`
* `adb push <filepath> /sdcard` push a file to the phone (/sdcard is phone storage)
* `adb pull /sdcard/<filepath>`
* `adb install <.apk filepath>`
* `adb shell`

# bootloader commands
* `fastboot devices`
* `getvar all`
* `fastboot getvar unlocked`
* `fastboot getvar secure`
* `fastboot boot <.img filepath(drop drop)>`
* `fastboot oem securewipe` # look into autoloader - bricked the keyone
* `fastboot flashing unlock`

# Check for connected android
* windows-key + r
* `devmgmt.msc`
* Other Devices -> Android

# Install drivers if android not detected
* motorola

# adb Drivers
* [link](https://adb.clockworkmod.com/)
