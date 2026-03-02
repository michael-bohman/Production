# PixelScout Configuration

## Required Equipment

* [ ] Emlid RS3 Base Station
* [ ] 15W USB-C Charging Cable
* [ ] Laptop (or iPad)
* [ ] Emlid Flow App (Optional, UI may differ than instructions)

## Instructions

### Charge Base Station



{% stepper %}
{% step %}
### Power On Base Station


{% endstep %}

{% step %}
### Connect to Base Station Wi-Fi

Open your wifi menu and select Reach:xx:xx.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Select "Connect using a password instead".

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

Enter emlidreach as the password, then press next/connect.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

You are now connected to the base station.

<figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Connect to Base Station Webpage

Open a web browser.&#x20;

<figure><img src="../../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the address bar type 192.168.42.1 and press enter/go

```
192.168.42.1
```

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

The base station webpage will appear. Check the two checkboxes and press accept.&#x20;

<figure><img src="../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Configure Base Output Settings

Select the Base output page from the left hand menu.

<figure><img src="../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

Select the channel dropdown box and select Serial.

<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

Select the Port dropdown box and select USB OTG.

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

Select the Baud rate dropdown box and select 115200.

<figure><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

Press Apply.

<figure><img src="../../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Set Base Station Name

Select the General dropdown from the left hand menu.

<figure><img src="../../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure>

Select Receiver info from the left hand menu.

<figure><img src="../../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>

Press Edit.
{% endstep %}

{% step %}
<figure><img src="../../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

Change the Receiver name to PixelScout-XXX where the XXX is the serial number of the system.&#x20;

Then press Apply.

<figure><img src="../../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Configure Base Settings

Select the Base settings page from the left hand menu.

<figure><img src="../../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure>

Select the Coordinate enter method dropdown box and select Average Fix.

<figure><img src="../../../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

Press the Edit button on the Antenna Height box.

<figure><img src="../../../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>

Set the Measured height to 1.194m (3.917ft).&#x20;

```
1.194
```

Then press Save

<figure><img src="../../../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
After you press save the antenna height box will read 1.328m. This is because the system automatically adds the distance to the phase center of the antenna. This is the CORRECT and expected value.&#x20;
{% endhint %}

Press Apply and average again.&#x20;

<figure><img src="../../../.gitbook/assets/image (23) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Update all RTCM3 Settings to output 1 Hz
{% endstep %}

{% step %}
### Power Cycle&#x20;

Power cycle the base station. This will update the new base station name for the base station "hot spot"

{% hint style="info" %}
This is the Wi-Fi network that the base station hosts.&#x20;
{% endhint %}
{% endstep %}

{% step %}
### Configure Wi-Fi&#x20;

Select the Wi-Fi page from the left menu.&#x20;

<figure><img src="../../../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>

Press the pencil button in the Hotspot mode menu.

<figure><img src="../../../.gitbook/assets/image (25) (1).png" alt=""><figcaption></figcaption></figure>

Change the password to pixelscout

```
pixelscout
```

Then press save.

<figure><img src="../../../.gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

