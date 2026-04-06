---
layout:
  width: wide
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: false
  tags:
    visible: true
---

# ✅ Initial Setup

## Required Equipment

| Emlid RS3 Base Station | 15W USB-C charging cable | iPad with Emlid Flow app |
| ---------------------- | ------------------------ | ------------------------ |
| Laptop                 |                          |                          |
|                        |                          |                          |

## Notes

The Base station should be plugged in and charging during the setup process. Refer to the 'Battery Status' section for charge amount and method of checking.



## Setup Instructions

### Turn on and connect

1. Plug the base station in using the USB plug under a rubber protection flap.

<figure><img src="../../../.gitbook/assets/IMG_7961.jpeg" alt="" width="375"><figcaption></figcaption></figure>

2. Press and hold the button on the base station until the lights turn on.
3. Use a laptop or iPad to connect to the Wi-Fi.
   1. The name will be Reach:AB:CD (A,B,C,D could be any alphanumeric character)
   2. if prompted for a pin instead of a password, click on <mark style="color:blue;">connect using a password instead</mark>.
   3. the password is _emlidreach_

```
emlidreach
```

you are now connected to the base station

|                                                                                          |                                                                            |                                                                                      |
| ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| <p><img src="../../../.gitbook/assets/2 (1).png" alt="" data-size="original"></p><p></p> | <img src="../../../.gitbook/assets/3 (1).png" alt="" data-size="original"> | <p><img src="../../../.gitbook/assets/4.png" alt="" data-size="original"></p><p></p> |

### Webpage

1. Navigate to 192.168.42.1 in a browser (iPad or laptop).
   1. For an iPad, using chrome is easiest (screenshot).

```
192.168.42.1
```

<figure><img src="../../../.gitbook/assets/File.png" alt="" width="375"><figcaption></figcaption></figure>

2. If prompted, check both boxes in a popup and click <mark style="color:blue;">Accept</mark>.

<figure><img src="../../../.gitbook/assets/5.png" alt="" width="563"><figcaption></figcaption></figure>

3. Configure Base Output Settings
   1. Navigate to <mark style="color:blue;">Base Output</mark> from the left-hand menu.
   2. In the 'Channel' dropdown box, select <mark style="color:blue;">Serial</mark>.
   3. In the 'Port' dropdown box, select <mark style="color:blue;">USB OTG</mark>.
   4. In the 'Baud Rate' dropdown box, select <mark style="color:blue;">115200</mark>.
   5. Click <mark style="color:blue;">Apply</mark>.

<figure><img src="../../../.gitbook/assets/6.png" alt="" width="563"><figcaption></figcaption></figure>

4. Set the base station's name.
   1. Navigate to <mark style="color:blue;">General</mark> > <mark style="color:blue;">Receiver info</mark> using the left-hand menu.
   2. Click <mark style="color:blue;">Edit</mark>.
   3. Change the name to 'PixelScout-XXX' where XXX is the serial number of the system.
   4. Click <mark style="color:blue;">Apply</mark>.

<figure><img src="../../../.gitbook/assets/7.png" alt="" width="563"><figcaption></figcaption></figure>

4. Configure the base settings.
   1. Navigate to <mark style="color:blue;">Base Settings</mark> from the left-hand menu.
   2. in the 'Coordinate entry method:' dropdown box, select <mark style="color:blue;">Average FIX</mark>.
   3. In the antenna height box, click <mark style="color:blue;">Edit</mark>.
   4. Set the 'Measured Height' to 1.194m (3.917ft) and click <mark style="color:blue;">Save</mark>.
   5. Click <mark style="color:blue;">Apply and average again</mark>.

{% hint style="info" %}
Note: After clicking 'save', the height will change to 1.328m. This is because the system automatically adds the distance to the phase center of the antenna. This is the CORRECT and expected value.
{% endhint %}

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/8.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/9.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

6. Update RTCM3 Settings
   1. Still in the 'Base Settings' page
   2. Update all 6 of the dropdowns to '1Hz'.
   3. Click <mark style="color:blue;">Apply</mark>.

<figure><img src="../../../.gitbook/assets/10.png" alt="" width="563"><figcaption></figcaption></figure>

7. Power cycle the base station to update the base station name.
   1. Hold the button to turn off or turn on the base station.
   2. The base station cannot turn on again immediately, wait about 20-30 seconds before turning back on.
8. Reconnect to the base station Wi-Fi and navigate back to the webpage.
   1. The only difference to previously is the Wi-Fi name, now it will be PixelScout-XXX:AB:CD.
      1. XXX indicates the systems serial number
      2. A,B,C, and D are alphanumeric characters.
   2. Password is 'emlidreach'.

```
emlidreach
```

<figure><img src="../../../.gitbook/assets/11.png" alt="" width="280"><figcaption></figcaption></figure>

9. Configure Wi-Fi
   1. Navigate to <mark style="color:blue;">Wi-Fi</mark> using the left-hand menu.
   2. Click on the <mark style="color:blue;">pencil</mark> in the 'Hotspot Mode' menu.
   3. Change the password to _pixelscout_
   4. Click <mark style="color:blue;">Save</mark>.

<figure><img src="../../../.gitbook/assets/12.png" alt="" width="563"><figcaption></figcaption></figure>

9. Disconnect from the base station Wi-Fi.



### Reconnect using Bluetooth

The Next steps require the use of a mobile device with Emlid Flow downloaded.

1. Open the Emlid Flow app.
2. Select the correct base station with 'Bluetooth' below it.

<figure><img src="../../../.gitbook/assets/IMG_0010.PNG" alt="" width="375"><figcaption></figcaption></figure>



### Emlid App

1. Turn off IMU
   1. Navigate to <mark style="color:blue;">Settings</mark>
   2. Click on the <mark style="color:blue;">IMU</mark> bar.
   3. Click <mark style="color:blue;">Turn off IMU</mark>.
   4. The page should now say 'Tilt compensation is inactive'.
   5. Back out to the main menu.

|                                                                                                 |                                                                               |                                                                               |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/IMG_0003.png" alt="" data-size="original">                   | <img src="../../../.gitbook/assets/IMG_0004.png" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0005.png" alt="" data-size="original"> |
| <p></p><p><img src="../../../.gitbook/assets/IMG_0006 (1).png" alt="" data-size="original"></p> |                                                                               |                                                                               |

2. Set the Corrections Input
   1. Navigate to <mark style="color:blue;">Correction Input</mark>.
   2. Select <mark style="color:blue;">NTRIP over Bluetooth</mark>.
   3. Input the following information. (this is for MNCors, it may be different for some people)
      1. Profile Name: \[Whatever you want]
      2. Address: mncors.dot.state.mn.us
      3. Port: 9000
      4. Username: \[Your MNCors username]
      5. Password: \[Your MNCors password]
      6. Mount Point: RTCM\_31\_NAD83(2011)
      7. Send receiver's position to the provider: Checked
   4. Click <mark style="color:blue;">Save</mark> at the top.

{% hint style="info" %}
Note: NTRIP credentials are stored on the device, not the base station. This means your personal MNCors account will not be seen by the customers.

Note: The position must be sent to the provider for this to work.
{% endhint %}

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/IMG_0007 (1).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/IMG_0008.png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

<figure><img src="../../../.gitbook/assets/IMG_0009.jpg" alt="" width="563"><figcaption></figcaption></figure>

3. Connect to Wi-Fi
   1. Navigate to <mark style="color:blue;">Wi-Fi</mark> in the Emlid Flow app.
   2. Connect the base station to the 'CaseWifi' Wi-Fi.
      1. This should deactivate the hotspot which means you cannot connect to the base station using anything other than Bluetooth.

|                                                                               |                                                                               |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/IMG_0012.PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0013.PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0014.PNG" alt="" data-size="original"> |

4. Update the firmware
   1. Back out to the main menu and Navigate to <mark style="color:blue;">Settings</mark> > <mark style="color:blue;">Firmware updates</mark>.
   2. There should be a new version available. If not, disregard step c.
   3. Click <mark style="color:blue;">Update Firmware</mark>.
   4. Wait for the update to complete

|                                                                               |                                                                               |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/IMG_0015.PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0016.PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0017.PNG" alt="" data-size="original"> |
| <img src="../../../.gitbook/assets/IMG_0018.PNG" alt="" data-size="original"> |                                                                               |                                                                               |

4. Forget the Wi-Fi
   1. Navigate back to <mark style="color:blue;">Wi-Fi</mark>
   2. In the hotspot area, click <mark style="color:blue;">Activate</mark>.
   3. Once the hotspot is activated, click on the <mark style="color:blue;">i</mark> icon next to the Wi-Fi that was used to perform the firmware update.
   4. Click on <mark style="color:blue;">Forget</mark>.

| Text                                                                              | Text                                                                          | Text                                                                          |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/IMG_0019.PNG" alt="" data-size="original">     | <img src="../../../.gitbook/assets/IMG_0020.PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0021.PNG" alt="" data-size="original"> |
| <img src="../../../.gitbook/assets/IMG_0022 (1).PNG" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_0023.PNG" alt="" data-size="original"> |                                                                               |

Emlid Reach RS3 Base Station is now configured for PixelScout use.



## Battery Status

PixelScout base stations should be shipping with 50-60% battery charge. During initial setup, it is ideal to charge them to \~60-70% and it will drop during calibration/test flights.

To check the status of the battery...

1. connect through Wi-Fi and navigate to 192.168.42.1 in a browser.
2. Click on <mark style="color:blue;">General</mark>.
3. Click on <mark style="color:blue;">Battery</mark>.
4. The battery percentage is shown on this screen.

<figure><img src="../../../.gitbook/assets/emlid battery picture.png" alt="" width="563"><figcaption></figcaption></figure>

Additionally, the LEDs on the base station indicate battery charge. Once 3 lights are illuminated and the 4th one is flashing. The base station is at 50%. About 30 minutes after that is sufficient for initial setup.
