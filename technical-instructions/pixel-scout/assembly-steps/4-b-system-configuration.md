# 4-B System Configuration

THIS PAGE MAY BE TEMPORARY

This page is used to organize thoughts/steps for the process between gimbal tuning and calibration flights. It includes many things and will probably be split up later.



## Prep

download the entire folder to your machine this has all the programs required to configure different parts of the system



## Guide

### Gimbal

1. Gimbal PIC32
   1. plug into the rear gimbal board with PK3 into 'PROG' port.
   2. go to \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-23138 -- Dual Gimbal\program-23138-03
   3. edit the .bat file in notepad to use PK3
   4. Turn on the drone
   5. Run the program
   6. Check the heartbeat LED
   7. Turn off the drone.
   8. Flip the DIP switch
   9. Check later with 192.168.5.130 (Software Status: Good: Normal Operation)

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/dual_gimbal_heartbeat.jpeg" alt=""><figcaption><p>Red Light at the bottom is the Heartbeat LED</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/DIP Switch.jpeg" alt=""><figcaption><p>DIP Switch at the top is to be switched to the ON Position (right)</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}



2. Comms PIC32
   1. Plug the PK3 into the center board 'PROG'
   2. Go to \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-23162 -- Dual Comms\program
   3. edit the .bat file in notepad to use PK3
   4. Turn on the drone
   5. run the program
   6. check the heartbeat LED
   7. The gimbal should go limp because the boards are talking to each other
   8. Turn off drone and unplug the PK3
   9. Check with 192.168.5.131 (Software Status: Good: Normal Operation)

<figure><img src="../../../.gitbook/assets/dual_comms_heartbeat.jpeg" alt="" width="375"><figcaption><p>Red light is the Heartbeat LED</p></figcaption></figure>

3. Encoder Calibration
   1. Plug in using Ethernet cable
   2. Follow 'Encoder Calibration Procedure.docx' in 'SW-23162 — Dual Comms'.
   3. Verify values read as follows (-/neutral/+)
      1. Pitch: -35/7/110
      2. Roll: -25/0/25
4. SBG
   1. go to 192.168.5.202
   2. Information > Upload Firmware > select the one with 6.0.5585
   3. Configure > Administration > Import Settings > Import
   4. Apply .json configuration file
   5. Address will change to 192.168.5.132. Check this.
5. Basecam SBGC
   1. This is the 'Gimbal Tuning' Step
6. Cameras
   1. Pull SD cards
   2. Copy config folder into firmware folder on both
   3. change the 'network.yaml' file in both to have the following
   4. eth0 address
      1. 192.168.5.141 for Primary
      2. 192.168.5.142 for Secondary
   5. eth0 gateways
      1. 192.168.5.200 for both
   6. Power cycle the drone twice
      1. Turn on, wait a couple minutes, turn off, turn on, continue
   7. Apply firmware update through website (back to 192.168.42.1/2)
      1. "\as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-xxxx-xxxx -- 65MP Firmware\firmware\21030-65MP\User Updates\65r-update\_4.5.0-21030.swu"
   8. Change configurations
      1. Primary - Spotting
      2. Secondary
      3. Set these as the factory defaults
         1. copy the config folder to the firmware folder, rename to 'factory-config'
   9. If the hw\_config has anything other than 'defaults' for calibration and zeros for rig\_relatives, change it to that.
7. Skyport V2
   1. Update the firmware through DJI assistant
   2. Bind the Skyport-V2 puck
      1. Payload SDK > Click 'Bind'
   3. verify through webpage that each camera has USB 3.0 super speed.

### Ground Radio

1. P900
   1. Configure radio using PicoConfigurator.

### Boom (Antenna)

1. PIC32
   1. Navigate to \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-23163 -- DGR Boom
   2. change the program.bat file to include the PK3
   3. Plug it into the 'PROG' port on the board.
   4. Power the board either using the drone/gimbal or the barrel jack on the bottom.
   5. Run the .bat program
2. P900
   1. Ensure the P900 board on the antenna is configured correctly
   2. You can plug in both the antenna and ground station to power to check that they connect (solid green)
3. U-blox
   1. Ensure the firmware on both the Rover and Moving base are up to date (HPG-1.51 release)
   2. U-Center > connections > network > new > tcp://192.168.5.135:6059X
      1. Rover: X = 2
      2. Moving Base: X = 3
   3. Find the firmware update here:
      1. \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-33026-01 - ZED F9P\firmware
