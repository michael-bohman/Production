# 5 System Configuration (Needs Screenshots)

## Prep

* Go to taurus>Productin>Technical Packages>PIXELSCOUT PHASE 4
* Download the entire 'Configuration Files' folder to your machine. This has all the programs required to configure different parts of the system

## Guide

### Gimbal

All files for this section are in the '1. Gimbal' folder in the configuration files

1. Gimbal PIC32
   1. Plug into the rear gimbal board using the Pickit™ 3 into the 'PROG' port.
   2. In the configuration files, go to 1. Gimbal > 1. Gimbal PIC32 > SW-23138 — Dual Gimbal > program-23138-03.
   3. Edit the 'program.bat' file in notepad
   4. Set the 6th line to say 'SET pgmDev=PK3'
   5. Turn on the drone
   6. Run the program
   7. Check that the heartbeat LED is flashing (Red light on the bottom, pictured).
   8. Turn off the drone.
   9. Flip the DIP switch at the top to the ON position (right).

<figure><img src="../../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/dual_gimbal_heartbeat.jpeg" alt=""><figcaption><p>Red Light at the bottom is the Heartbeat LED</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/DIP Switch.jpeg" alt=""><figcaption><p>DIP Switch at the top is to be switched to the ON Position (right)</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}



2. Comms PIC32
   1. Plug the Pickit™ 3 into the center board 'PROG' and an ethernet cable into the center board.
   2. In the 'Configuration files' folder, go to 1. Gimbal > 2. Comms PIC32 > SW-23162 — Dual Comms > program
   3. edit the .bat file in notepad to use PK3 in the same way as the first step.
   4. Turn on the drone
   5. run the program
   6. Check that the heartbeat LED is flashing (upper right side, pictured)
   7. The gimbal should go limp when ethernet is plugged in because the boards are talking to each other.
   8. Turn off the drone and unplug the Pickit™ 3.

<figure><img src="../../../.gitbook/assets/dual_comms_heartbeat.jpeg" alt="" width="375"><figcaption><p>Red light is the Heartbeat LED</p></figcaption></figure>

3. Check the status of both boards just programmed.
   1. Turn the drone back on with the ethernet cable still plugged it.
   2. In a webpage, go to 192.168.5.130.
      1. 'Software Status' should say "Good: Normal Operation - PPS: Boom"
   3. Go to 192.168.5.131
      1. 'Software Status' should say "Good: Normal Operation"

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption><p>192.168.5.130</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/image (122).png" alt=""><figcaption><p>192.168.5.131</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}



4. Encoder Calibration
   1. Keep the ethernet cable plugged in.
   2. In the 'Configuration Files' folder, go to 1. Gimbal > 2. Encoder Calibration and open the 'Encoder Calibration Procedure.docx' file.
   3. Follow these steps to calibrate the encoders.
   4. When finished, verify values read as follows (-/neutral/+)
      1. Pitch: -35/7/110
      2. Roll: -25/0/25
5. SBG
   1. In the 'Configuration Files' folder, go to 1. Gimbal>4. SBG
   2. In a browser, go to 192.168.5.202
   3. go to the 'information' tab.
   4. In the 'Firmware & GNSS' field, click 'Upload Firmware'
   5. navigate to the SBG folder and select the .sar file with '6.0.5585' in its name.
   6. wait for the firmware update to finish. You may need to refresh the page.
   7. In the webpage, go to Configure > Administration > Import Settings > Import
   8. Apply .json configuration file with 'DJI - PixelScout-v4.0' in its name.
   9. Address will change to 192.168.5.132. You will have to navigate to the new address.
   10. Double check the firmware version.
   11. Turn off the drone

|                                                                                                                 |                                                                                  |
| --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/image (124).png" alt="" data-size="original">                                | <img src="../../../.gitbook/assets/image (125).png" alt="" data-size="original"> |
| <p><img src="../../../.gitbook/assets/Screenshot 2026-03-27 113834.png" alt="" data-size="original"></p><p></p> | <img src="../../../.gitbook/assets/configure1.png" alt="" data-size="original">  |

6. Cameras
   1. Pull both SD cards out of the cameras, being careful to remember which one is which.
   2. Using the computer, copy the config folder from the info folder into firmware folder on both SD Cards
   3. For both cameras, in the newly copied config folder (in the firmware folder), open the 'network.yaml' file and change the following settings.
      1. eth0 address
         1. 192.168.5.141 for Primary
         2. 192.168.5.142 for Secondary
      2. eth0 gateways
         1. 192.168.5.200 for both
      3. ros\_domain\_id
         1. 0 for Primary
         2. 1 for Secondary

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

Primary Settings
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

Secondary Settings
{% endcolumn %}
{% endcolumns %}

7. Power cycle the drone twice
   1. Turn on, wait a couple minutes, turn off, turn on, continue
8. Apply the 4.5.1 firmware update through website.
   1. Go to 192.168.42.1 (or 42.2 for secondary) in a browser.
   2. Go to the 'Update firmware' page.
   3. Drag the file into the section on the page.
   4. The firmware file is in the Camera folder in the 'Configuration Files' folder.

<mark style="color:red;">Pictures Here</mark>

9. Change configurations
   1. Still in the webpages, go to the 'Configuration' page.
   2. Change the configurations to the following.&#x20;
      1. Primary - Spotting
      2. Secondary
   3. Set these as the factory defaults
      1. copy the config folder to the firmware folder, rename to 'factory-config'

<mark style="color:red;">Pictures here</mark>

10. If the hw\_config has anything other than 'defaults' for calibration and zeros for rig\_relatives, change it to that.
11. Connect a high speed usb cable and verify through webpage that each camera has USB 3.0 super speed.

<mark style="color:red;">Pictures here</mark>

12. Skyport V2
    1. Connect a USB-C cable to the top of the drone.
    2. Open DJI Assistant and sign in.
    3. Update the firmware through DJI assistant
    4. Bind the Skyport-V2 puck
       1. Payload SDK > Click 'Bind'

<mark style="color:red;">Screensots here</mark>

{% hint style="info" %}
NOTE: the BPR step can be skipped if the process has already been completed in the focusing step.
{% endhint %}

12. Take BPR pictures.
    1. Mount the gimbal to a drone and turn it on. Connect to the gimbal using usb.
    2. Start a session for the each camera using the webpage.
       1. name it anything, the pictures won't be stored in the session.
    3. Run the bpr pictures program and follow the instructions.
       1. The program must be edited in notepad to set the ip address for the camera being worked on.
    4. Save the pictures created to a '\[PixelScout SN] BPR' folder.
    5. Send the folder to zach/brian/jon for processing (WILL PROBABLY CHANGE)
    6. After receiving the bprmap.csv file from processing, apply it to the cameras by placing it in the correct 'firmware' folder.
    7. Power cycle the cameras and ensure it is saved to the 'info' folder.

### Ground Radio

The files for this section are in the '2. Ground Radio' folder in the configuration files.

1. P900 Programming
   1. Follow the steps in the P900 Radio Programming Page.
      1. [3-c-p900-radio-programming.md](3-c-p900-radio-programming.md "mention")

### Boom (Antenna)

The files for this section are in the '3. Boom (Antenna)' folder in the configuration files.

1. PIC32
   1. in the Boom folder, navigate to 1. PIC32 > SW-23163 — DGR Boom > program
   2. change the program.bat file to include the PK3
   3. Plug it into the 'PROG' port on the board.
   4. Power the board either using the drone/gimbal or the barrel jack on the bottom.
   5. Run the .bat program

<mark style="color:red;">Pictures here</mark>

2. P900
   1. Ensure the P900 board on the antenna is configured correctly
   2. While the antenna is being powered on the drone, plug the ground radio into a laptop using a USB-C cable and ensure it connects to the antenna (Solid green lights on the ground radio).

<mark style="color:red;">Pictures here</mark>

3. U-blox
   1. Ensure the firmware on both the Rover and Moving base are up to date (HPG-1.51 release)
   2. U-Center > connections > network > new > tcp://192.168.5.135:6059X
      1. Rover: X = 2
      2. Moving Base: X = 3
   3. If the boards are not up to date, refer to the 'F9P programming' page
      1. [3-b-f9p-board-programming-needs-screenshots.md](3-b-f9p-board-programming-needs-screenshots.md "mention")
      2. Find the firmware update file in the 'Configuration files' folder in 3. Boom (Antenna) > 3. U-Blox > SW-33026-01 - ZED F9P > firmware

<mark style="color:red;">Pictures here</mark>
