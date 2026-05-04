---
description: 'Owner: Simon'
---

# 📷 Calibration/Verification Flights

## Notes

* This is a reference guide for production members already familiar with flying the M300/350 system. This is not a guide to learn how to fly the drone. Many important notes will be missed because the reader is assumed to know them already.
* The calibration and verification flights are very similar, there are only a few differences. For this reason, the calibration flight guide will have every step and the verification flight guide will only have the differences.



## Calibration Flight Guide

1. Set up the System in the same manner as the ground test.
   1. [ground-test.md](ground-test.md "mention")
2. Set up a flight plan
   1. If a flight is already set up and imported, skip this step.
   2. Use an m350 to set up a plan, this is so that the start point may be selected/swapped for a/b flights.
   3. Choose a rectangular area over a parking lot or other flat area with many lines/corners
      1. choose an area about 60ft x 100ft. The flight plan should expect to take about 150 pictures. If it is much more than that, make the area smaller.
         1. The drone will actually take more than this, but its a good rule of thumb for creating a flight plan.
   4. Use these settings for the plan
      1. Drone: M300/350
      2. Camera: Custom Camera > Sentera 65R 60mm
      3. Altitude: 100ft (above takeoff point)
         1. GSD should automatically change to 0.16
      4. Elevation Optimization: OFF
      5. Course Angle: Set such that there are more, shorter legs rather than fewer, longer legs.
      6. Overlap: 80 and 80
      7. Margin: 20
      8. Start point: prefer the closer one but not very important.
   5. Save the plan with the name ending in 'a'. For example 'FlightPlanExample\_a'.
   6. Go to the flight plan library
   7. at the top, click the 'select' icon. Select the plan you just made and duplicate it.
   8. Rename the new flight plan to end in 'b'. For example 'FlightPlanExample\_b'.
   9. Edit the 'b' flight plan.
      1. Change the start point to the other end of the flight path where 'a' should finish. Otherwise, ensure it is the same.
   10. Save this flight plan.
3. Ensure the antenna lights show 4 green and the cameras started a session.
4. Ensure the ground module shows 3 solid green lights and the Emlid Flow app shows a 'FIX' status.
5. Take off manually and fly figure 8s around the area you are flying for at least 3 minutes. This is to let the GPS have a more accurate yaw measurement immediately.
   1. Note: It may also help to manually fly a similar path to the flight plan for the same amount of time. In the future, there may be a premade plan for this.
6. Fly the flight plan ending in 'a'.
   1. The flight plan can be started while the drone is hovering in air. You do not need to land before starting.
   2. When it starts, ensure pictures are being taken. Listen to audible shutter sounds and look for an increasing photo count.
7. When the first flight route is complete, before the drone lands, hit the pause button on the controller.
8. Go to the flight plan library and start the plan ending in 'b'.
   1. Ensure pictures are being taken in the same way.
9. Once the second flight plan finishes, let the drone land, turn it off, and pack everything up.







## Verification Flight Differences

The verification flight is the same as the configuration flight except for a few difference shown below. Otherwise, use the same flight plans as calibration to allow for better comparison.

1. Figure 8s are not needed before executing the flight plans.
2. Ensure the system has the calibration and BPR enabled before flying.
   1. Calibration found at the end of hw\_config.
      1. method should say pix4d
      2. rig\_relatives\_deg should be non-zero
   2. BPR enabled using webpage > Image adjustments > 'Bad Pixel Replacement'
      1. also make sure the bpr map csv file is loaded in the info folder of the camera alongside the hw\_config.
