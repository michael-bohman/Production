# Configuration

Note: need to use static IP (same as weedscouts)









```
Gimbal PIC32 (192.168.5.130):
	• [ ] Program firmware: pic32-DualGimbal.PPS_GEN.2025012100 .
	• [ ] Set the DIP switch so that Basecam UART is connected to PIC32.
Comms PIC32 (192.168.5.131):
	• [ ] Program firmware: pic32-DualComms.DEFAULT2.2024121100 .
	• [ ] Complete encoder calibration (MRE webpage tab).
Primary Camera - 6XT (192.168.5.141):
	• [ ] Perform a factory reset to clear any engineering artifacts.
	• [ ] Apply update to 3.18.0
	• [ ] Select if800-array-1 for the configuration.
	• [ ] Apply if800-array-1 as the factory default.
	• [ ] Verify that hardware configuration file matches the camera serial number and calibration is reasonable.
	• [ ] Clear the SD-card and "data" directory.
Secondary Camera - 6X (192.168.5.142):
	• [ ] Perform a factory reset to clear any engineering artifacts.
	• [ ] Apply update to 3.18.0
	• [ ] Select if800-array-2 for the configuration.
	• [ ] Apply if800-array-2 as the factory default.
	• [ ] Verify that hardware configuration file matches the camera serial number and calibration is reasonable.
	• [ ] Clear the SD-card and "data" directory.
```



192.168.5.130 IFT

<figure><img src="../../../.gitbook/assets/image (225).png" alt="" width="233"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (226).png" alt="" width="240"><figcaption></figcaption></figure>

192.168.5.131 DJI

<figure><img src="../../../.gitbook/assets/image (228).png" alt="" width="240"><figcaption></figcaption></figure>







192.168.5.131

<figure><img src="../../../.gitbook/assets/image (227).png" alt="" width="237"><figcaption></figcaption></figure>

do encoder calibration in MRE tab

Roll: -35/0/35

Pitch: -35/7/110













