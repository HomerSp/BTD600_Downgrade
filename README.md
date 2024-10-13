# BTD600_Downgrade
Instructions for downgrading the Sennheiser BTD600 adapter.<br>Note that I will not take any responsibility in case anything should go wrong - do this at your own risk! I have switched to all the available versions myself, but I cannot guarantee anything.  

# Steps:
* Download the official Sennheiser updater for Windows from: https://www.sennheiser-hearing.com/btd600-license-agreement and extract. Open it and make sure the version number in the title bar says 1.0.9. Close when done.
* Use your choice of hex editor (https://hexed.it/ if you don't have one) and open it. Once it's loaded, open up SDUpdater.exe from the SennheiserTransmitterUpdater directory inside the hex editor.
* Once it's loaded, go to byte 0x6e74 (CTRL+G and type that in the Go to box if using hexed). The highlighted byte should say 16. Change it to say 17 (simply higlight the byte, and type in 17). The surrounding bytes should now say 17 16 *17* 17 17.
* Save the modified file as SDUpdater.exe, replacing the old file.
* Open up the updater program again, and once you've accepted the license agreement, there should be a new button in the bottom left corner. Pressing this button allows you to select a file from your computer to update - this will allow us to "upgrade" to any version we want.
* Download the firmware you want from the list below, and save it in the same folder as the SDUpdater.exe file.
* Select the file from updater program and start the Update.
* Good luck!

# Firmware version downloads:
v1.13.0: https://firmware.s-consumer-cloud.com/files/btd600/1.13.0/MX168_BT_DFU_V1.13.00.bin<br>
v1.14.0: https://firmware.s-consumer-cloud.com/files/btd600/1.14.0/MX168_BT_DFU_T1.14.00.bin<br>
v1.20.0: https://firmware.s-consumer-cloud.com/files/btd600/1.20.0/MX168_BT_DFU_V1.20.00.bin<br>
v1.22.0: https://firmware.s-consumer-cloud.com/files/btd600/1.22.0/MX168_BT_DFU_V1.22.00.bin<br>

# API endpoints:
Available firmware versions: https://api.s-consumer-cloud.com/firmware/api/v2/availableSystemReleases/700248?os_type=android<br>
Firmware manifest: https://api.s-consumer-cloud.com/firmware/api/v2/systemRelease/700248/{version}?os_type=android<br>
