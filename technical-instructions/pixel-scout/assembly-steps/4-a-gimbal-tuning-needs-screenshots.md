# 4-A Gimbal Tuning (Needs Screenshots)

## Notes

While changing values through Basecam GUI, click 'write' **often** (especially after adjusting **any** value) to upload the correct values to the gimbal. Additionally, click 'Restart' fairly often to make sure the gimbal will act accordingly. If the gimbal is making any unexpected actions, click write and/or restart to see if that fixes it.

## Pre-tuning Balancing

Before the gimbal is tuned, it must be balanced as much as possible for the most effective tune.

1. Connect the gimbal to a drone, do not turn it on.
2. If the gimbal leans all the way left (facing the gimbal), tape a weight on the high side of the gimbal frame until it's balanced, noting how heavy it is.
3. Take the gimbal off and unscrew the 4 M3x6 screws on the pitch motor side of the camera pod.
4. Choose a spacer to start with based on what weight was used to balance the gimbal.

| Weight                      | Spacer Thickness |
| --------------------------- | ---------------- |
| minimal (Sskyport cap, etc) | 30 mil           |
| 6 grams                     | 40 mil           |
| 12 grams                    | 60 mil           |

5. Insert the spacer between the pitch motor and camera pod. Re-secure using 4 new screws (<mark style="color:yellow;">91698A304 M3x8 Flat Head Black</mark>) and Loctite.
6. Double check how balanced the gimbal is, repeat with a new size spacer if needed until the gimbal is fairly level.

## Tuning Setup

1. Attach the camera gimbal to a DJI M300 or M350.
2. Connect a USB TTL cable from a computer to the back of the gimbal.
3. Power on the drone.

<figure><img src="../../../.gitbook/assets/IMG_7718 (1).jpg" alt="" width="375"><figcaption></figcaption></figure>

## Tuning

1. Open Basecam GUI.
2. Select the corresponding COM port and click 'connect'.
3. Restore the 'Starting Point' EEPROM.
   1. At the top, go to Board>Backup Manager.
   2. In the 'Restore from Backup' tab, click on browse and upload the 'Starting point' EEPROM.
   3. Click 'Upload'
4. Go to the 'Hardware' tab
5. Ensure the roll output is disabled and the pitch output is enabled.
6. The P and I values may need to be lowered in the 'stabilization' tab.
   1. 'P' values for the pitch and roll may be set to \~80.
   2. 'I' value for the top one may be set to \~5.
7. Under the 'Encoders' tab, click 'E Field Calibration' and allow the gimbal to self-calibrate.
8. Click 'Offset Calib' and allow the gimbal to self-calibrate again.
   1. Note the offset value. Add or subtract 4096 to correct it.
   2. The white arrow in the 'Pitch' circle on the right should be perpendicular to the black.
      1. <-5,000 --> ADD 4096
      2. \>-5,000 --> SUBTRACT 4096
      3. If later in the tuning process, the gimbal is not able to tune the roll offset, this may need to be switched (added instead of subtracted, etc)
9. Under the 'Hardware' Tab, enable the roll output.
   1. Keep the Pitch enabled as well.
10. Under the 'Encoders' tab, click 'E Field Calibration' and allow the gimbal to self-calibrate.
11. Click 'Offset Calib' and allow the gimbal to self-calibrate again.
    1. If the self-calibration fails twice, try switching adding/subtracting 4096 to the PITCH offset.
    2. Readjust the PITCH offset value to the same as previously calculated.
12. Under the 'UNKNOWN TAB, CHANGE NAME LATER' tab, click on 'auto-tune PID'.
    1. Click 'Start' and allow the gimbal to self-tune itself.
    2. Ensure the errors are staying <\~20 (<\~10 is ideal)
    3. Click 'Stop' once the auto-tuning is complete
13. Gently shake the entire drone around to ensure there are no points in the range of motion where the gimbal freaks out/gets stuck.
14. Backup a tuned version of the EEPROM to the SN folder corresponding to the gimbal.
15. click 'Disconnect' and power down the drone.



When completed: return to 3-A End Gimbal Assembly page

[3-a-end-gimbal-assembly-needs-pictures.md](3-a-end-gimbal-assembly-needs-pictures.md "mention")
