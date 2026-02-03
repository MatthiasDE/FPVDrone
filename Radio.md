# Radio

## EdgeTX
Nowadays the standard operating system for radios.

## Jumper Bumblebee Firmware Update Procedure
> Before Starting connect your device via USB and make a backup of your SD Card!

1. Press Boot Button at the back
2. While pressed insert USB A to USB C Cable connected to your computer
3. Check on Windows Device Manager if you have "STM32 Bootloader"
  * with "Other Devices" and with exclamation mark because of no installed driver, or => continue with step 4
  * if you have "STM32 Bootloader" with "USB Devices" => skip step 4
4. Download [Zadig](https://zadig.akeo.ie/) what is recommended as per [community.st.com](https://community.st.com/t5/stm32-mcus-products/firmware-flash-with-custom-desktop-application-using-stm32-s/m-p/718963)
5. Open Link `[https://buddy.edgetx.org/](https://buddy.edgetx.org/) in Chrome Browser (Chrome!!!)
6. In `Firmware version` select the latest version, e.g. `EdgeTX "Jolly Mon" v 2.11.4
7. In `Radio model` select `Jumper Bumblebee`
8. Click `Flash via USB`
9. Click `Add new device`
10. Select `STM32 Bootloader"
11. Flash the device and stay patient
11. Turn on your device go into sys-menu (press burger menu key long) and go to page 7/7 to assure you installed `edgetx-bumblebee` with your selected version


## ExpressLRS Configuration
[https://www.expresslrs.org/software/updating/wifi-updating/](https://www.expresslrs.org/software/updating/wifi-updating/)
Password: expresslrs
Interface: http://10.0.0.1/

## ExpressLRS LUA Script Update
1. Download/Install [ExpressLRS Configurator](https://github.com/ExpressLRS/ExpressLRS-Configurator/releases)
3. Choose Device: Category `Jumper 2.4 GHz` and device target `Jumper AION Bumblebee 2.4 GHz TX`
4. Choose Regulatory Region 2,4 Ghz Band: `2.4 GHz LBT (EU)`
4. Bindphrase selected: `<YourBindingPassphrase>`
5. Flash Choosing WLAN; then create firmware file and connect via WLAN to update the Firmware
6. Download LUA File (e.g. `elrsV3.lua`) and transfer to folder `<drive>\SCRIPTS\TOOLS` after connecting via WLAN

> 3.6.3 was installed on the radio

## Errors
### Entering `ExpressLRS` in sys-menu results in looping `Loading`
This is caused because Express LRS module can't be found. Check in Module Setting on page 2/11 and see if Internal RF Mode is `Off` or External RF Mode is `Off`. If both are off then switch on the corresponding one needed e.g. Internal RF - Mode `On`. This should fix the problem. Credits to [Whirly Bloke - How to fix a RadioMaster/EdgeTX ExpressLRS LUA script that gets stuck saying Loading...](https://odysee.com/@whirlybloke:e/how-to-fix-a-radiomaster-edgetx:9)
