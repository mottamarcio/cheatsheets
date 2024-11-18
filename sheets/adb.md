## ADB (Android Debug Bridge)

**List of commands:**

| Command | Description |
|---|---|
| `adb devices` | List connected devices |
| `adb shell` | Open a shell on the device |
| `adb install <path/to/apk>` | Install an APK |
| `adb uninstall <package_name>` | Uninstall an app |
| `adb push <local_path> <remote_path>` | Push a file to the device |
| `adb pull <remote_path> <local_path>` | Pull a file from the device |
| `adb reboot` | Reboot the device |
| `adb reboot recovery` | Reboot into recovery mode |
| `adb reboot bootloader` | Reboot into bootloader mode |
| `adb logcat` | View device logs |
| `adb shell pm list packages` | List all installed packages |
| `adb shell pm clear <package_name>` | Clear app data |
| `adb shell dumpsys activity` | Get information about current activity |
| `adb shell screencap -p <path/to/screenshot.png>` | Take a screenshot |
| `adb shell screenrecord <path/to/video.mp4>` | Record the screen |
| `adb forward tcp:<local_port> tcp:<remote_port>` | Forward a port |
| `adb shell settings get global <setting_name>` | Get a global setting value |
| `adb shell settings put global <setting_name> <value>` | Set a global setting value |
| `adb shell am start -n <package_name>/<activity_name>` | Start an activity |
| `adb shell am broadcast -a <action_name>` | Send a broadcast intent |
| `adb shell input text "Hello World"` | Simulate text input |
| `adb shell input keyevent <keycode>` | Simulate key press |
| `adb shell monkey -p <package_name> -v 500` | Run Monkey stress test |
| `adb shell pm grant <package_name> <permission>` | Grant a permission to an app |
| `adb shell pm revoke <package_name> <permission>` | Revoke a permission from an app |
| `adb sideload <path/to/ota_update.zip>` | Sideload an OTA update |

**Tips and Tricks:**

* Use tab completion to quickly complete commands and file paths.
* Pipe `adb logcat` output to `grep` to filter logs.
* Use `adb shell getevent` to identify keycodes for specific keys.
* Create aliases for frequently used commands in your shell's configuration file.
