# Droplit OpenWRT Firmware Loader

## Hardware prerequisites

This app was designed with a specific set of hardware to meet the minimal requirements. The hardware is:
* Symbol Barcode Scanner DS9208
* Raspberry Pi3 7" Touchscreen Display (At least 800x480 resolution)
* At least a 16GB micro SD card
* Raspberry Pi3 B+

You can purchase all of these products on [amazon](https://amazon.com/ideas/amzn1.account.AHVDRPBVC2VKH6VEM5HFUTAZ24YQ/HFF7CPT9N3C1).

## How to install openwrt-firmware-loader

0. Make sure you have Windows 10 IoT installed and ready to go on your raspberry pi3 device. You can find instructions on how to do so [here](https://www.windowscentral.com/how-install-windows-10-iot-raspberry-pi-3).
1. Download the [latest release](https://github.com/droplit/openwrt-firmware-loader/releases/latest) and take note of its location.
2. Download and install the Microsoft IoT Dashboard from the Microsoft Store or [here](https://docs.microsoft.com/en-us/windows/iot-core/connect-your-device/iotdashboard).
3. After you open the dashboard, find your raspberry pi3 device in the `My Devices` list and right click on it. Press `Open in Device Portal`.
4. This will open a webpage in your default browser. Once you authenticate, navigate to `Apps->Apps Manager`.
5. Here you will be able to select a source for the app installation file with the `Browse...` button at the top of the screen. Once you find your file, press `Install`.
6. Once the app gets uploaded and installed, you should see it in your list of installed apps. Locate it and select the radio button in the `Startup` column to start the app.


## Documentation

You can find the documentation for this app in the `Docs` folder of this repository [here](https://github.com/droplit/openwrt-firmware-loader/tree/master/Docs).


[![licensebuttons by-nd](https://licensebuttons.net/l/by-nd/3.0/88x31.png)](https://creativecommons.org/licenses/by-nd/4.0)
