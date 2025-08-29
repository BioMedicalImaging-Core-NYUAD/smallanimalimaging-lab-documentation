.. _Ultima-specifications:

Ultima 2Pplus - System specifications
=====================================

.. image:: ../_static/Ultima2Pplus.jpg
   :alt: *Ultima 2Pplus*
   :width: 1000px
   :align: center

*Ultima 2Pplus*

.. raw:: html

Laser input
-----------
- Coherent Chameleon Discovery NX TPC dual-output femtosecond laser
    - Widely tunable from 660 to 13200 nm
    - Fixed secondary output at ~1040 nm (>2.8 W)
    - Peak power >2.7 W
- Laser power meter with pick-off window for monitoring
- Integrated AOM modules for imaging and uncaging pathways
- Switchable IR mirror mechanics for routing between galvo and resonant scanning paths

Laser scanner
-------------
- Dual independent sets of X-Y galvanometer mirrors for standard
    - Standard set for raster scan imaging
    - Second set for precise, programmable point scanning and photostimulation
- Resonant scanner (8 kHz resonant galvo for up to 30 fps)
- Field of view:
    - Galvo scanning: 22.7 mm field number (1.11 × 1.11 mm with 16× 0.8 NA objective)
    - Overscan mode: 28 mm field number (1.4 × 1.4 mm with 16× 0.8 NA objective)
- Scan modes: frame scanning, ROI scanning, freehand line scanning, scan rotation, optical zoom

Detectors
---------
- Two high-efficiency Hamamatsu GaAsP PMTs with mounting flanges
- Pre-amplifier and HV controller optimized for GaAsP tubes
- Close-proximity detector design for maximum photon collection with high NA objectives
- Dual emission filters: ET525/70m-2p and ET595/50m-2p with t565lpxr dichroic beam splitter
- 2″ collection optics for maximizing photon throughput

Optics and nosepiece
--------------------
- Single objective nosepiece (M32 threading) with rotational axis for angled imaging (±87°)
- Motorized Z-focus with reliable 250 nm step size (electronics capable of 100 nm increments)
- Motorized pitch nosepiece for precise rotational control
- Beam expander lens set (3×) for adapting to different objective back apertures
- Objectives supported
    - Nikon CFI Plan Apo Lambda 4×
    - Nikon CFI75 16×/0.8 NA
    - Nikon Apo 60× Water/1.0 NA
    - Nikon CFI75 Apo 25× Water Immersion

Epi-fluorescence imaging
------------------------
- Modified epi-illuminator arm with integrated LED excitation source
- Widefield fluorescence imaging for sample positioning and overview imaging
- Integrated CMOS camera for capturing epifluorescence images
- Available filter sets (Nikon cubes)
    - ET-DSRed (TRITC/Cy3): ET545/30x, ET620/60m; dichroic T570LP
    - ET-DAPI: AT350/50x, ET460/50m; dichroic T400LP
    - ET-YFP: ET500/20x, ET535/30m; dichroic T515LP
    - ET-GFP (FITC/Cy2): ET500/20x, ET535/30m; dichroic T515LP

Imaging chamber and enclosure
-----------------------------
- Light-tight Faraday cage enclosure (43.25″ × 36″ × 40″) with interlocked laser safety ports
- Table laser safety covers (for 4′ × 8′ table)

Electronics
-----------
- FPGA-based control electronics for precise synchronization
- Multi-channel analog integration with 12-bit A/D conversion
- Pre-amplifier and HV electronics tailored for GaAsP detectors
- Remote controller for motorized Z-axis

Software
--------
- Prairie View scan control and acquisition software
- Simultaneous acquisition from up to four channels with independent LUTs
- Time Series acquisition for flexible experimental design
- Resonant Galvo+ software module for high-speed imaging
- Integrated calibration and drift compensation for ETL remote focusing modules

Available accessories
---------------------



Operational protocols and risk assessments
------------------------------------------
The SOPs and RAs related to the use of the Ultima 2Pplus system are available https://drive.google.com/drive/u/0/folders/1biXgabX9BQkMIouT0Lx4Yg9P1y6UJ8bb,
upon request. These documents are stored in the designated folder and include:

- SOP for Ultima 2Pplus utilization
- RA for Ultima 2Pplus with anesthesia
