---
description: 'Stage 2 D4K 21022-03 Owner: Amanda Janssen'
---

# 🚧 Programming

## Equipment Needed&#x20;

|                                      |   |   |
| ------------------------------------ | - | - |
| Ethernet to 8 pin connector          |   |   |
| Micro SATA cable                     |   |   |
| 6X 12v Powersupply with d4k adapter  |   |   |

## Prep&#x20;

1. Install on your computer&#x20;
   1. In windows features -> Install "WMIC"
   2. Online install -> ".NET framework 3.5" (complete before ADB installer)
   3. Open prereqs folder -> Factory\_Flash\_usb folder
      1. install the ADB Installer and Install Keys

## Guide&#x20;

#### Preparing the MicroSD Card&#x20;

1. Remove the microSD rom the Double 4K
2. Insert the microSD card into the computer
3. Navigate to the “0\_format\_sdcard.exe” file within the most recent Rev folder
4. Double click the “0\_format\_sdcard.exe” file
   1. If the user account window pops up, hit “Yes”
5. Close all file explorer windows
6. Ensure that the selected drive letter displays “63G exFAT” to the right of the field
7. Select the proper “Allocation unit size” of 32768
8. Fill in the Volume Label field according to the part number of the Double 4K
   1. For the 21022-XX, name the card “Double 4K”
   2. b. For the 21023-XX, name the card “Skyport”
9. Ensure the “Quick Format” Checkbox is filled
10. Click “Start”
11. Click “OK”.
12. Wait for the bar at the bottom of the window to fill with green and “Done” to be shown in the display window.
    1. If the format fails, eject the SD card, close the formatter window, and try again.&#x20;
13. Eject the microSD card from the computer an return the SD card to the sensor



#### Factory Flash USB

1. Secure the sensor into the 21924 – Jig, Focusing, Double 4K
2. Plug the JST end of the 21924 – Jig, Focusing, Double 4K into the sensor
3. Plug the power pole end of the 21924 into the 24182 – Cable Assembly, Power, Focusing
4. Power on camera and focusing mount fan
5. Ensure that the blue light on the back of the camera is illuminated. If not illuminated, do not proceed
6. Plug the micro USB end of the micro USB to USB Cable into the double 4K, and the USB end of the cable into the computer
   1. Wait until you hear the windows device connect tone
7. Navigate to the “1a\_factory\_flash\_usb.bat” file within the most recent Rev folder
8. Double click the “1a\_factory\_flash\_usb.bat” file
9. Follow on screen prompts, using the latest firmware release.
   1. If the program is not working try “1b\_factory\_flash\_usb\_no\_erase” file
10. Wait for the camera to finish. After a few minutes if the programming hangs during “Waiting for version info”, clicking enter can help as well as unplugging and re-plugging in the Micro USB cable can help.
11. Once done, close the command prompt, disconnect the USB cable and move onto the next step.

#### Update Hardware Configuration

1. Double click the “2\_update\_hw\_config.bat” file.
2. Follow the on screen prompt and select the appropriate part number
3. If an incorrect hardware error is displayed, the incorrect part number was selected
4. Follow the on screen prompt and select the appropriate serial number
5. Wait for the configuration to finish and to display the configuration information
6. Confirm that the part number and serial number displayed match the sticker on the side of the Double 4K
7. Press any key to close the window.

#### Focus Camera Script&#x20;

1. Unplug the micro USB cable used in steps 3.2 and 3.3 from the Double 4K
2. Plug in the 8 pin ethernet end of 24140 from your computer to the camera
3. Set static IP ->
   1. &#x20;set to manual
   2. IPv4 enabled
   3. set IP 192.168.143.242 and subset 255.255.255.0
4. Double click 3\_focus\_camera.bat
5. Wait for the onscreen prompt to ask for an input
6. Type 1 and click enter
7. Wait for camera LED to blink red
8. Power cycle and Close the 3\_focus \_camera.bat
9. Restart application and reconnect power wait for LED to turn green

#### Configure Camera Script

{% hint style="info" %}
Cameras come in many hardware configurations, the -XX identifies the filters and lenses used and the part number tells the programmer what HW-config to apply. The operational mode is often unknown when building the camera but must be selected to configure the camera. Therefore, unless otherwise stated

21022-06 should always be programmed for Sentera protocol,&#x20;

21022-XX (excluding -06) should always be programmed for DJI protocol

21023-XX should always be programmed to PSDK DJI protocol
{% endhint %}

1. Remove the SD card from the camera and plug into your computer&#x20;
2. Double click the “4b\_configure\_sdcard” file
3. Follow the on-screen prompts and select the correct configuration file for the sensor being configured
