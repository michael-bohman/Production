# RTK FIX Testing

{% file src="../../../.gitbook/assets/Example Checkout Document (1).pdf" %}

## Ground Radio Checkout

This is the first part of testing that both modules are operating properly. This is testing the ground module and air module connection.&#x20;

1. Turn on Emlid and confirm self self survey is complete
2. Plug in ground radio (SN # should be the same for both air and ground modules)
3. Confirm scrolling lights
4. Turn on drone with everything attached&#x20;
5. Confirm ground module lights are now solid&#x20;
6. Wait for 65R to start a session
7. Connect 65R to the webpage&#x20;
8. Look for accuracy to go down. Once it reaches 0.014 it will be a RTK Fix
9. Confirm Hand controller displays RTK FIX
10. Take 5 pictures from the controller
11. Circle RTK FIX on document&#x20;
    1. Write Time Sync Present for webpage verification
12. Unplug ground radio, keep everything else powered on
13. Wait for webpage and controller to verify Standard GPS
    1. While waiting navigate to file explorer \\\192.168.42.1
       1. Rename the session with "ground SN"00
       2. Confirm photos were taken
14. Power off when "standard GPS returns

## Hand Controller NTRIP

1. Turn on drone and turn on NTRIP
2. Wait for 65R to start a session
3. Connect 65R to the webpage&#x20;
4. Look for accuracy to go down. Once it reaches 0.014 it will be a RTK Fix
5. Confirm Hand controller displays RTK FIX
6. Take 5 pictures from the controller
7. Navigate to file explorer \\\192.168.42.1
   1. Rename the session with "ground SN"
   2. Confirm photos were taken
8. Power off drone
