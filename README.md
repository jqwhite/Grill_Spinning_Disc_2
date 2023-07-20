# Grill_Spinning_Disc_2
 Info, drivers, documentation for Grill Spining Disc 2 in 454

## Service notes ##

Changes to hardware and software are documented here.

### April 2023
- Relocated from 256 to 454 Optics suite (Jamie White).
- Cable connections and port assignments documented.
- Laser power low.  488 unuseable (~1mW), 561 barely (~5mW).

### Early May 2023

#### Pete Pitrone service visit:
- optimized laser output in the Andor combiner. 
- 488 to ~5mW and 561 to ~15mW
- 561 laser well beyond rated service life.  
- 488 relatively new but still weak.
- CSU-X1 aligned (didn't need it) and cleaned (didn't nead it).
- Hammamatsu camera failed.

### Mid-May 2023
- Hammamatsu camera revived with the help of Sebastian Bundschu and Archit. The status LED had been turned off in the software. The issue was getting the **driver version matched to the software version** of (µ-Manager?  Hammamatsu control software?).
- Andor laser combiner retired (Jamie White).
- Omicron laser combiner with 445, 488, 515, and 594nm lasers commissioned (Jamie White).
- Original FCP8 fiber that arrived with Omicron exchanged by Omicron for an AFP fiber. See `Fiber_exchange` in `Omicron` folder.  This chage was instigated after Pete Pitrone from Andor. (Turns out he was incorrect; see below). 
- **Triggerscope** **ordered** for laser triggering and power control.
- **Filters** **ordered** for 488/594 dual-excitation imaging. A new dichroic in the CSU-X1 head blocks detection of both laser lines, and a dual-band emission filter allows the GFP and mKate2 signals to pass to the camera.  **Dual-color imaging is achieved by switching the lasers without switching the emission filters.**
- Archit improvised laser control with an Arduino.
- Archit switched to using the Andor Precision Control Unit for laser control: lasers are triggered by the Orca camera

### Early-June 2023
- It turns out that the FCP8 was correctly specified.  Original fiber back from Omicron (oops) and verified by Sebatsion (specifications), Archit and Jamie (imaging).
- ## Original FCP8 fiber re-installed. ##
- Omicron laser input optimized by Stephan to ~75mW at the fiber tip.
- New dichroic for 488/594 GFP/mKate imaging: **ZT488/594TPC 13x15x0.5mm Lot#413707**
- New emission filter for 488/594 GFP/mKate imaging: **ZET488/594m 25mm die mounted Lot#412247**
- Filters from AHF Analysentechnik Dr. Michael Sommerauer
```
  Dr. Michael Sommerauer
  Sales Director Optical Filters
  AHF analysentechnik AG
  Kohlplattenweg 18
  DE -  72074 Tuebingen
  ms@ahf.de
  www.ahf.de
  fon: +49-7071/970901-15
  fax: +49-7071/970901-99
```
- Old filters kept in the AHF box

Current filters in the Sutter Lambda 10B are now:

```
  4 Label,Wheel-A,9,9: block
  3 Label,Wheel-A,8,8: BF (empty)
  2 Label,Wheel-A,7,7: 488 LP
  1 Label,Wheel-A,6,6: polarizer
  0 Label,Wheel-A,5,5: BF
  9 Label,Wheel-A,4,4: block
  8 Label,Wheel-A,3,3: ZET488-594m
  7 Label,Wheel-A,2,2: 525/50
  6 Label,Wheel-A,1,1: BP
  5 Label,Wheel-A,0,0: 512/630 db

```

Micro-manager configuration file updated with GFP, mKate, and GFP/mKate channels.

### June - July 2023

- Triggerscope setup according to Austin Blanco/Nico Sturman published recommendations

YouTube video here: 

https://youtu.be/5AC9UtiF0JM
  
