# Initial Setup

## Required Equipment

* [ ] Emlid RS3 Base Station
* [ ] 15W USB-C Charging Cable
* [ ] Laptop (or iPad)
* [ ] Emlid Flow App (Optional, UI may differ than instructions)

## Setup Instructions

### Turn on and connect

1. plug the base station in using the USB plug under a rubber protection flap.
2. press and hold the button on the base station until the lights turn on.
3. Use a laptop or iPad to connect to the Wi-Fi.
   1. The name will be Reach:AB:CD (A,B,C,D could be any alphanumeric character)
   2. if prompted for a pin instead of a password, click on 'connect using a password instead'.
   3. the password is _emlidreach_

```
emlidreach
```

you are now connected to the base station

### Webpage

1. navigate to 192.168.42.1 in a browser.

```
192.168.42.1
```

2. If prompted, check both boxes in a popup and click 'Accept'.
3. Configure Base Output Settings
   1. Navigate to 'Base Output' from the left-hand menu.
   2. In the 'Channel' dropdown box, select 'Serial'.
   3. In the 'Port' dropdown box, select 'USB OTG'.
   4. In the 'Baud Rate' dropdown box, select '115200'.
   5. Click Apply.
4. Set the base station's name.
   1. Navigate to General>Receiver info using the left-hand menu.
   2. Click 'Edit'.
   3. Change the name to 'PixelScout-XXX' where XXX is the serial number of the system.
   4. Click 'Apply'.
5. Configure the base settings.
   1. Navigate to 'Base Settings' from the left-hand menu.
   2. in the 'Coordinate entry method:' dropdown box, select 'Average FIX'.
   3. In the antenna height box, click 'Edit'.
   4. Set the 'Measured Height' to 1.194m (3.917ft) and click 'Save'.
   5. Click 'Apply and average again'.

{% hint style="info" %}
Note: After clicking 'save', the height will change to 1.328m. This is because the system automatically adds the distance to the phase center of the antenna. This is the CORRECT and expected value.
{% endhint %}

6. Update RTCM3 Settings
   1. Still in the 'Base Settings' page
   2. Update all 6 of the dropdowns to '1Hz'.
   3. Click Apply.
7. Power cycle the base station to update the base station name.
   1. The base station cannot turn on again immediately, wait about 20-30 seconds before turning back on.
8. Reconnect to the base station wifi and navigate back to the webpage.
   1. The only difference to previously is the wifi name, now it will be PixelScout-XXX:AB:CD.
      1. XXX indicates the systems serial number
      2. A,B,C, and D are alphanumeric characters.
9. Configure Wi-Fi
   1. Navigate to 'Wi-Fi' using the left-hand menu.
   2. Click on the pencil in the 'Hotspot Mode' menu.
   3. Change the password to _pixelscout_
   4. Click 'Save'.
10. If not already, disconnect from the base station wifi.

### Reconnect using Bluetooth

The Next steps require the use of a mobile device with Emlid Flow downloaded.

1. Open the Emlid Flow app.
2. Select the correct base station with 'Bluetooth' below it.

### Emlid App

1. Turn off IMU
   1. Navigate to 'Settings'
   2. Click on the 'IMU' bar.
   3. Click 'Turn off IMU'.
   4. The page should now say 'Tilt compensation is inactive'.
   5. Back out to the main menu.
2. Set the Corrections Input
   1. Navigate to 'Correction Input'.
   2. Select 'NTRIP over Bluetooth'.
   3. Input the following information. (this is for mncors, it may be different for some people)
      1. Profile Name: \[Whatever you want]
      2. Address: mncors.dot.state.mn.us
      3. Port: 9000
      4. Username: \[Your MNCors username]
      5. Password: \[Your MNCors password]
      6. Mount Point: TRCM\_31\_NAD83(2011)
      7. Send receiver's position to the provider: Checked

{% hint style="info" %}
Note: NTRIP credentials are stored on the device, not the base station. This means your personal MNCors account will not be seen by the cutstomers.

Note: The position must be sent to the provider for this to work.
{% endhint %}

1. Update the firmware
   1. Navigate to 'Wi-Fi' in the Emlid Flow app.
   2. Connect the base station to the 'CaseWifi' Wi-Fi.
      1. This should deactivate the hotspot which means you cannot connect to the base station using anything other than bluetooth.
   3. Back out to the main menu and Navigate to Settings>Firmware updates.
   4. There should be a new version available. If not, disregard the next few sub-steps.
   5. Click 'Update Firmware.
