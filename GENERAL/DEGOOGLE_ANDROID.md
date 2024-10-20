# [(TUTORIAL) How to DeGoogle any Android phone WITHOUT root!](https://www.reddit.com/r/degoogle/comments/jqxe1u/tutorial_how_to_degoogle_any_android_phone/https://www.reddit.com/r/degoogle/comments/jqxe1u/tutorial_how_to_degoogle_any_android_phone/)

1. [Install App Manager](https://f-droid.org/en/packages/io.github.muntashirakon.AppManager/)
2. Enable Developer Options
3. Connect your Android phone to your PC via USB and select "File transfer" mode.
4. Download ADB Platform Tools
5. open the "platform-tools" folder
6. open a CMD/Terminal inside the platform-tools folder
7. `adb devices`
8. `adb shell`
9. uninstall Google Play Store -> `pm uninstall -k --user 0 com.android.vending`
10. show list of keyword name -> `pm list packages | grep <OEM/Carrier/App Name>`
11. Uninstalls the given app -> `pm uninstall -k --user 0 <package name>`
12. Disables the given app -> `pm disable-user --user 0 <package name>`
13. Reinstalls a system app if you accidently uninstalled it -> `cmd package install-existing <package name>`
14. Try if nothing else works -> `pm default-state <package name>`
15. Enables the given app -> `pm enable <package name>`
