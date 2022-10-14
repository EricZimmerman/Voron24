## Debug

if you are switching to CW2,  then at that time, i would :
1) dbl check no shorts in soldering
2) test with 3 wire cable to one of the endstop ports. it should behave fine and be nice and cool
if not, then i would exhcnage yours to see what is going on.

## General
- install spring in sexbolt
    - use other parts
- FINISH ELLIS TUNING
    - input shaper
        - blue goes to inside of connector
    - pressure advance, etc
- put printer on UPS
- LAN vs wireless
- reduce length of bowden tube in printer case
- start using bed mesh
- Mainsail timelapse
    - https://www.youtube.com/watch?v=n-BVPidUDLI 
- KlipperScreen?
    - https://klipperscreen.readthedocs.io/en/latest/
- Filament sensor
    - https://www.amazon.com/dp/B07Z97582P/?coliid=I278JGHS5OD8M7&colid=3T6GGJW7T3YSG&psc=1&ref_=lv_ov_lig_dp_it
- add to super slicer
  - Printer Settings -> Custom G-code -> Before layer change Gcode -> TIMELAPSE_TAKE_FRAME
- C920 webcam
  - https://www.teamfdm.com/files/file/275-c920-mount/

## TO PRINT
- purge bucket/nozzle wipe? 
   - https://github.com/Dfdye/Voron_Mods/tree/main/Purge_Bucket_for_WP_Kinetic_Mount
   - have one in macros already, but https://github.com/Hartk-PrinterConfigs/DoomConfig/blob/master/purge.cfg
   - maybe not tall enough https://www.printables.com/model/201999-nozzle-scrubber-with-a-little-bucket-for-voron-24
- Quick release clips
  - https://github.com/richardjm/voron-parts/tree/main/voron-2.4/FilamentLatch
- nevermore
  - https://github.com/nevermore3d/Nevermore_Micro 
- led case light clips (need 42 in black)
  - https://github.com/VoronDesign/VoronUsers/blob/master/printer_mods/eddie/LED_Bar_Clip/LED_Bar_Clip_Misumi_version2.stl
- SB diffuser
  - clear filament from LDO kit
- z belt cover for led wire
  - https://github.com/MotorDynamicsLab/LDOVoron2/blob/main/STLs/z_belt_cover_a_led.stl
- exhaust cover
  - https://voronregistry.com/mods/fiction-exhaustcoversfs
- nozzle holding skirt
  - https://github.com/VoronDesign/VoronUsers/blob/master/printer_mods/README.md
- Top mount spool holder
  - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/elcrni/V2.4-Trident-Spool-Holders
- Rock and roll for electronics access
  - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/RockNLol/RockNRoll
- Door hinges
  - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/randell/Door_Hinges
- Scraper
  - https://www.printables.com/model/28337-scraper-for-build-plate-version-2
- Updated z joints with bearing
  - https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Voron%202/2.4/Voron2.4_GE5C



## TO BUILD
### CW2 VERIFY AGAINST BOM at [https://vorondesign.com/voron_stealthburner](https://vorondesign.com/sourcing_guide?model=VSB)
- hartk 2 piece pcb (got it)
    - https://github.com/hartk1213/MISC/tree/main/PCBs/Stealthburner_Toolhead_PCB
    - https://www.youtube.com/watch?v=PCIwZRPYMZ8
- need motor (ordered)
- gear kit (ordered)
- set ratio to 50:10
- reprint face?
    - will need fans and leds if so
    - https://www.fabreeko.com/products/stealth-burner-pre-soldered-and-crimped-leds?_pos=1&_psq=led&_ss=e&_v=1.0
    - https://kb-3d.com/store/fans/501-sunon-5015-blower-fan-24v-maglev-1646515411413.html or https://www.fabreeko.com/products/gdstime-5015-24v-blower-fan?_pos=1&_sid=76b2a2b69&_ss=r
    - https://www.fabreeko.com/products/sunon-mag-lev-4010-24v-fan?_pos=1&_psq=4010&_ss=e&_v=1.0
- 3 of M3x6 FHCS 
    - https://www.boltdepot.com/Product-Details.aspx?product=13249
