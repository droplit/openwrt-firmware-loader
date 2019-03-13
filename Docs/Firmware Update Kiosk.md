# Firmware Update Kiosk

This tool will help you semi-automate your process of updating the firmware of an OpenWRT device. The requirements for this process are:

1. OpenWRT device you wish to provision.
2. Kiosk device running this app.
3. New compatible firmware image to update to.
4. A `FAT` or `NTFS` external storage device containing the firmware.
5. A working internet connection.

### Home screen

To begin the firmware upgrade process please insert the removable storage with the new firmware image into the kiosk device.

Follow the on-screen instructions and press continue.

Optionally you can also press the settings button in top right corner to navigate to the settings screen and configure an optional code scanner device.

### Settings Screen

On this screen you will be able to select which port the code scanner is connected to. Once the device is selected the app will automatically try to connect and will display a success or error message in the middle of the screen depending on the status of the connection to the device. Once you have made your selection, press back in the top left corner to return to the previous screen.

### Select Device Screen

On the next screen you should see a list of possible devices you can connect to and upgrade. There are also two filtering options to help you narrow down your search results. You can filter by `MAC address` and/or a prefix. Next to the `MAC address` filter you will also see a barcode icon. Clicking on this icon will let you configure a code scanner that can scan the appropriate QR code on your tonly hub and enter it into the `MAC address` filter field automatically. You can also do this by typing into either field using the onscreen or a physical keyboard.

At the bottom of the screen there are two checkboxes. The "auto-select exact match" checkbox will automatically select the item in the list if it matches exactly to either of the filters. The second checkbox will be grayed out on your first use of the app and only becomes available as an option after you will have picked a firmware image to use. Checking this box will let you skip picking the firmware screen every time. Once you are satisfied with your device choice, select it and press next.

### Select Firmware Screen

On this screen you will be able to select which firmware image you want upload to your device. The app will attempt to connect to your device and retrieve the current version of the device, as well as the list of all binary files on your removable storage. The app should be able to automatically recognize a removable storage device plugged in as long as it's in the supported format.

At the bottom of the screen you will see a checkbox to `auto-start upgrade`. Checking this box will let you bypass the current screen next time you use the app so you won't have to pick the same firmware version every time. To get back to this screen, simply uncheck the `auto-start upgrade` checkbox on the previous `Select Device Screen`.

After you have decided on your desired firmware image, select it and press next.

If you have accidentally selected the wrong device, you can press back instead.

*N.B: Be careful in providing the right format of firmware image. Providing an incompatible file can result in bricking your device for good.*

### Upgrade Screen

At this point the app will attempt to complete the firmware upgrade process for you. The app will establish a connection with the device and start uploading the file. You should be able to track this on the progress bar at the bottom of the screen.

Once the file is uploaded, the app will perform an `MD5` hash calculation to check that the file has been transferred in it's entirety before beginning the upgrade. Since the upgrade requires the device to reboot, you will be disconnected from the device and redirected to either a success or failure screen.

### Success Screen

Yay! Your device should now be upgraded to the new firmware image :)
You can confirm the new firmware image by using the app or navigating to the device directly at its IP address in a web-browser.

### Failure Screen

Something went wrong and the upgrade process failed :(
You can try it once more by clicking the `RESET` button and going through these steps again.

### Network Unavailable

This usually happens when the app tries to retrieve the default gateway address of the device, but fails to connect. This can happen several times in a row until it is finally able to connect. You can click on the `RESET` button to try again.

### Firmware Integrity Failure

If you see this screen that means the file wasn't successfully transmitted to the device in it's entirety and/or ended up being corrupt upon receipt. You can click the `RESET` button to try again.

### Firmware Retrieval Failure

This error occurs when the app is unable to retrieve the selected firmware from the removable storage device. You can click the `RESET` button to try again.



## Troubleshooting

Make sure there is enough space on device before uploading the firmware image. Don't worry if there's a copy of the old image, the app will overwrite that image as long as it is the same name. Rebooting the device should clear the RAM from any additional files.

Power cycling the device can sometimes help resolve network connection and availability issues between the app and device.