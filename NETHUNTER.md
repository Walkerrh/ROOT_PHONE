* [Installing NetHunter](https://www.kali.org/docs/nethunter/installing-nethunter/)
* [Installing Kali Nethunter on the OnePlus (and probably other phones too)](https://www.adamlabay.net/2022/09/17/installing-kali-nethunter-on-the-oneplus-and-probably-other-phones-too/)
* []()

# virtualbox
* [VirtualBox](https://www.virtualbox.org/)
* VirtualBox Extension Pack
  * `https://download.virtualbox.org/virtualbox/< VERSION >/Oracle_VirtualBox_Extension_Pack-< VERSION >.vbox-extpack`
* Guest Additions ISO
  * `https://download.virtualbox.org/virtualbox/< VERSION >/VBoxGuestAdditions_< VERSION >.iso`
  * `sudo gpasswd -a $USER vboxusers`

1. Update your phone to the latest stock OS
   * you will not be able to update Android after installing Nethunter
   * you must use the stock version of Android that ships with your device
    
2. Install ADB and Fastboot
   * Windows/Mac: install platform tools sdk from android developer site
   * Ubuntu:
     * `sudo apt install android-tools`
     * `sudo apt-get -y install android-sdk-platform-tools`
     * `sudo apt-get -y install android-tools-adb`
   * Arch: `sudo pacman -S android-tools`
  
3. Enable USB Debugging and other fancy developer tools
   * 1a) settings -> about phone -> build number (tap 7 times)
   * 1b) settings -> system -> developer options
     * enable usb debugging
     * (optionally) enable advanced reboot

4. Install Magisk
   * [Magisk Github Page](https://github.com/topjohnwu/Magisk)
   * `adb push Magisk-v25.2.apk /sdcard/Download`

5. Patch your Boot Image
   * 5a) Google “factory image [OS build] site:xda-developers.com”
   * 5b) extract all from the .zip
   * 5c) install [python](https://www.python.org/)
     * 5a1) `pip install protobuf`
     * 5a2) `pip install bsdiff4`
   * 5d) [payload_dumper github page](https://github.com/vm03/payload_dumper)
     * `python -m pip install -r requirements.txt`
     * `python update_metadata_pb2.py`
     * `python <path>/payload_dumper.py <path>/payload.bin`
   * 5e) `adb push <path>/boot.img /sdcard/Download`
   * 5f) open magisk app
     * 5f1) install -> select and patch a file -> boot.img
   * 5g) `adb pull /sdcard/Download/magisk_patched_[string of stuff].img`
  
6. Unlock the bootloader
   * `adb reboot bootloader`
   * `fastboot oem unlock`
  
7. Repeat Steps 3-4
  
8. Patch your boot image
    `fastboot flash boot magisk_patched_[string of stuff].img`

11. Disable encryption
    * option1) [Disable_Dm-Verity_ForceEncrypt](https://github.com/Zackptg5/Disable_Dm-Verity_ForceEncrypt)
    * option2) [DFE-NEO v2](https://xdaforums.com/t/a-b-a-only-script-read-only-erofs-android-10-disable-force-encryption-native-early-override-dfe-neo-v2-disable-encryption-data-userdata.4454017/)

13. Wipe the Data partition


15. Repeat Steps 3-4

16. Install Nethunter
    * download a [prebuilt nethunter](https://www.kali.org/get-kali/#kali-mobile) if phone and os are correct
    * else [Building NetHunter](https://www.kali.org/docs/nethunter/building-nethunter/)
      * `git clone https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-installer.git`
      * `cd kali-nethunter-installer/`
      * `./bootstrap.sh`
        * blank & N
      * `python3 build.py -h`
      * `python3 build.py -k oneplus6-oos --eleven -fs full`



# super partition stuff
* [Implement dynamic partitions](https://source.android.com/docs/core/ota/dynamic_partitions/implement)
`adb reboot bootloader`
`fastboot getvar current-slot`
`fastboot flash super super_patched.img` to flash super partition 
* to switch boot slots (two different ways)
  * `fastboot --set-active=b`
  * `fastboot set_active a`

https://xdaforums.com/t/tool-oneplusrecovery-tool-v1-0-restore-stock-cm11s-fix-bricks-etc.2991851/
https://xdaforums.com/t/index-oneplus-one.2843675/


# ah
* `bcdedit.exe -set testsigning on`
* `bcdedit.exe -set testsigning off`

# disable unsigned drivers
* restart windows
* boot into windows troubleshoot
* startup settings -> choose 7
