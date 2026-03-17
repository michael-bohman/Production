# 4-B Gimbal Configuration

THIS PAGE IS TEMPORARY

This page is used to organize thoughts/steps for the process between gimbal tuning and calibration flights. It includes many things and will probably be split up later.



## Prep

download the entire folder to your machine this has all the programs required to configure different parts of the gimbal.



## Guide

1. Gimbal PIC32
   1. plug into the rear gimbal board with PK3 into 'PROG' port.
   2. go to \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-23138 -- Dual Gimbal\program-23138-03
   3. edit the .bat file in notepad to use PK3
   4. Turn on the drone
   5. Run the program
   6. Check the heartbeat LED
   7. Turn off the drone.
   8. Flip the DIP switch
2. Comms PIC32
   1. Plug the PK3 into the center board 'PROG'
   2. Go to \as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-23162 -- Dual Comms\program
   3. edit the .bat file in notepad to use PK3
   4. Turn on the drone
   5. run the program
   6. check the heartbeat LED
   7. The gimbal should go limp because the boards are talking to each other
   8. Turn off drone and unplug the PK3
3. Encoder Calibration
   1. Plug in using Ethernet cable
   2. Follow 'Encoder Calibration Procedure.docx' in 'SW-23162 — Dual Comms'.
4. SBG
   1. go to 192.168.5.201 or 202 for primary and secondary cameras
   2. Apply configuration
5. Basecam SBGC
   1. This is the 'Gimbal Tuning' Step
6. Cameras
   1. Pull SD cards
   2. Copy config folder into firmware folder on both
   3. change the 'network.yaml' file in both to have the following
   4. First address
      1. 5.141 for Primary
      2. 5.142 for Secondary
   5. Second address
      1. 5.200
   6. Power cycle the drone twice
      1. Turn on, wait a couple minutes, turn off, turn on, continue
   7. Apply firmware update through website (back to 192.168.42.1/2)
      1. "\as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-xxxx-xxxx -- 65MP Firmware\firmware\21030-65MP\User Updates\65r-update\_4.5.0-21030.swu"
   8. Change configurations
      1. Primary - Spotting
      2. Secondary
   9. If the hw\_config has anything other than 'defaults' for calibration and zeros for rig\_relatives, change it to that.
7. Skyport V2
   1. Update the firmware through DJI assistant
   2. Bind the Skyport-V2 puch
   3. verify through webpage that each camera has usb 3.0 super speed.
