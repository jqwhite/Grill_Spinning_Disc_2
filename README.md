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
- Omicron laser combiner with 445, 488, 515, and 594nm lasers commissioned.
- Original FCP8 fiber that arrived with Omicron exchanged by Omicron for an AFP fiber. See `Fiber_exchange` in `Omicron` folder.
- **Triggerscope** **ordered** for laser triggering and power control.
- **Filters** **ordered** for 488/594 dual-excitation imaging. A new dichroic in the CSU-X1 head blocks detection of both laser lines, and a dual-band emission filter allows the GFP and mKate2 signals to pass to the camera.  **Dual-color imaging is achieved by switching the lasers without switching the emission filters.**
- Archit improvised laser control with an Arduino.
