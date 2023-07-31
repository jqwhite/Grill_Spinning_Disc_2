# Grill_Spinning_Disc_2 Startup Sequence
 
 Current startup sequence for Grill Spining Disc 2 in 454.

## Boos Power Manager ##

Switch on in sequence left to right:

0. Main power (black switch) on (if off).  On = in, off = out.
1. CSU-X1 (Spinning disc)
2. Blue Box (Spinning disc controller)
3. Sutter filter wheel (between spinning disc and camera)
4. Zeiss power (turns on power supply in the gantry)
5. Hamamatsu Orca (camera)
6. Triggerscope 4 (controls Z-stage and lassers)

## Individual equipment ##

Switch on in sequence left to right facing optical table:

7.  Omicron LightHub (laser system): Press blue switch, turn key to 1.  Emission light should come on.
8.  Uniblitz shutter VMM-D1 (transmitted light shutter): switch at back-left.
9.  Zeiss stand (stand functions / objective revolver): button on left side of stand. Keypad next to computer displays should light up.
10. ASI MS-200 (stage XYZ motors & Z-piezo).
11. PC (on gantry)

## Login info ##

For usual experiments, use **Griller** account:

```
Username: GRILL-PC-3
Password: Griller
```
For system administration and setup, use **admin** account:

```
Username: admin
Password: trueGriller
```
## Z-axis orientations ##

There are two devices controlling the Z-focus: the Zeiss focus axis, which moves the objective turret, and the ASI Z-piezo insert, which moves the piezo insert of the stage.

The ASI insert has a range of 150µm.  Currently (2023-07-20) the range is set to a values from -75µm to +75µm.

Currently (2023-07-20) for both Zeiss and piezo, **as the values become more positive, the sample moves closer to the objective.**  

Physically, this means that as Z-values become more positive the Zeiss focus moves the objectives **up** toward the slide, and the piezo moves the stage **down.**

**Example:** if a sample is in focus, you can move it -20µm out of focus with the Zeiss focus, which physically moves the objective **down** to **increase** the distance between the objective and the sample.  You can move it back into focus with the ASI piezo by moving it +20µm, which physically **decreases** the distance between the objective and the sample, this time, however, by physically moving the Z-stage down.

## TTL Control ##


