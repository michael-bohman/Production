# P900 Radio Programming

## Parts Needed:

* TTL-232RG USB Cable.
* AC Power Adapter (12V)
* Y Adapter (Labeled 'P900')

## Guide

{% stepper %}
{% step %}
### Open 'Pico Config'

\as-taurus.jdnet.deere.com\Data\Part Database (things we sell)\SW-32011 -- P900 Radio\_tools\PicoConfig1.7
{% endstep %}

{% step %}
### Plug in the P900 Board

Use the items listed in 'Parts Needed'.

(INSERT PICTURES HERE)
{% endstep %}

{% step %}
### Program the Board

NOTE: If the light stutters/dims and TURNS OFF at any point in the process, unplug the board immediately and place in a bag marked 'BAD'. Refer to Fault Isolation for more information.

1. In the Pico Configurator program, the 'Current Value' column should populate. In the 'New Value' and 'Modify' columns, change the Power to be '23dBm - 200mW'. and click 'PGM/Save'.
   1. This is to keep the power low as often as possible to avoid bricking.
2. Select the correct option under 'Load Factory Defaults' and click 'Default Unit'
   1. 'PP Master' for air units.
   2. 'PP Remote' for ground units.

NOTE: This is the most common place for a board to be bricked, be aware of the status of the board.

3. Set the values to the following.
4. The 'Network Address' should be set to the Remote Net ID intended for the air/ground units. It should be 32011-XXXXX.
5. Click 'Read Board' to double check the values have been set correctly, and the board itself has not been bricked.
   1. The light should be the following:
      1. Ground module: Scrolling.
      2. Air module: One light solid.
{% endstep %}
{% endstepper %}
