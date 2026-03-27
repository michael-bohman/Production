---
description: Stage 2 in the 65R Process 21030-02
---

# 65R Programming

## Programming Instructions

1. Remove the microSD card from the 65R and put it in the computer.
2. Navigate to the folder and copy the contents to the microSD card.
   1.  "taurus\Production\Technical Packages\65R SENSOR\IN PROGRESS\65R SENSOR - Technical Data Package\65R SENSOR - PROGRAMMING\65R\_Programming\firmware - sdcard"

       <figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>
3. Eject the microSD card from the computer and put it back in the 65R camera.
4.  Remove the rear cover of the camera attached with 7 screws. (4 outer, and 3 fan)

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="350"><figcaption></figcaption></figure>
5. Replace one of the screws on the fan to hold it in place.
6. Secure the board stack to the front cover using two screws opposite each other.
7. Set the dip switches present on the imager baseboard CCA to the following positions:
   1. **Mode: ON**
   2.  **JTAGEN: OFF**

       <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt="" width="323"><figcaption></figcaption></figure>
8. Connect the SWI24-12-N-P5 12V Power Supply between an outlet and the 65R camera.
9.  Connect the USB-C (or micro USB for -04 cameras) to USB cable between a PC and the 65R.

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt="" width="304"><figcaption></figcaption></figure>
10. Navigate to 192.168.42.1 on chrome.
11. Navigate to the 'Update Firmware' tab on the left side of the webpage.
12. Click on the 'Firmware Update' field and select the file **65r-factory-update\_X.X.X-21060.swu** where ('X.X.X' is the release version) from the **firmware-factory update** folder.
13. Once the firmware update is completed (approx. 5 minutes), power down the 65R.
    1. Note: The firmware update page may not show the correct firmware. This will be fixed once the switches are in the correct position later.
    2. Note: When unplugging the barrel0jack power connector, hold the heat-sink down with one hand pulling up on the connector with the other. This ensures the board-to-board connectors do not become loose or separate.
14. Remove the microSD card from the camera and place it in the computer.
15. Delete all files from the microSD card.
16. Copy folder **configs/21030-XX/firmware** to the microSD card. Select the **21030-XX** folder based on what camera model is being programmed.
    1.  Note: the 65R PHX configuration is applied as the initial configuration so that the camera operation and focusing can be accomplished without being connected to a gimbal.

        <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
17. On the microSD card, open file **firmware/hw\_config.yaml** and update the serial number to the intended serial number of the camera (surrounded by single quotes).

    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
18. Eject the microSD card from the computer and place it in the 65R camera.
19. Set the DIP switches present on the Imager Baseboard CCA to the following positions:
    1. **Mode: OFF**
    2. **JTAGEN: OFF**
20. Power on the camera.
21. Navigate to 192.168.42.1 on a web browser.
22. Navigate to the 'Configuration' tab on the left side of the webpage.
23. Verify that the OEM configuration is being used.
    1.  Use 'Sentera PHX' if focusing will be performed immediately.

        <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
24. Navigate to the 'Diagnostics' tab on the left side of the webpage.
25. Verify that the Part Number and Serial Number are what is expected for the camera.

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
26. Navigate back to the 'Home' tab on the left side of the webpage.
27. Under 'Session Control', type 'prog test session' and click 'Start Session'.
    1.  Ensure the lights on the camera turn green and no errors pop up on the webpage.

        <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
28. Under 'Trigger Control', click 'Capture Image'.

    <figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
29. In a file explorer, navigate to //192.168.42.1/.
30. Go tot Data>Snapshots>prog test session>rgb and open the image.
    1. Ensure it opens correctly and the file is not corrupted.
31. Re-secure the rear cover to the camera using the same 7 screws that were removed with new Loctite. Torque to 40 in-oz.
    1.  Ensure the push button did not fall out during programming.

        <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

