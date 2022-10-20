## Debug

if you are switching to CW2,  then at that time, i would :
1) dbl check no shorts in soldering
2) test with 3 wire cable to one of the endstop ports. it should behave fine and be nice and cool
if not, then i would exhcnage yours to see what is going on.

## General
- igus cables direct
    - https://www.igus.com/product?artNr=CF10-05-04
- sensorless end stops for x and y
    - https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html
- CANBUS WHEN CW2
    - https://github.com/maz0r/klipper_canbus/blob/main/controller/monster8v2.md
    - https://github.com/maz0r/klipper_canbus/blob/main/toolhead/ebb36-42_v1.1.md
    - https://www.teamfdm.com/forums/topic/672-how-to-use-can-toolhead-boards-connected-directly-to-octopus-octopus-pro-on-canboot/
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/LoCoCNC/Strain_Relief_w_Microfit
    - https://github.com/MotorDynamicsLab/LDOVoron2/blob/main/STLs/beefy_raspberry_bracket.stl
    - https://github.com/VoronDesign/Voron-2/blob/Voron2.4/STLs/Electronics_Bay/pcb_din_clip_x3.stl
    - https://github.com/MotorDynamicsLab/LDOVoron2/blob/main/STLs/toolhead_breakout_pcb_bracket.stl
    - https://github.com/KayosMaker/CANboard_Mounts
    - https://github.com/majarspeed/Misc-Voron/tree/main/StealthBurner%20Umbilical%20cover
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Minsekt/Rear_Umbilical
    - https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Voron%202/2.4/CW2_SB2040_CAN_Umbilical
    - canbus and SB/CWw2 stuff https://github.com/kejar31/VoronMods/tree/main/CB-C2
        - need a fan https://dfh.fm/products/sunon-mf20100v1-1000u-a99-2010-axial-fan?_pos=1&_sid=d08833795&_ss=r
- Macro ideas
    - https://github.com/zellneralex/klipper_config/tree/master
    - https://docs.vorondesign.com/community/macros/macros/120decibell.html
    - swap out existing for these or euclid ones
        - https://github.com/jlas1/Klicky-Probe/blob/main/Klipper_macros/klicky-macros.cfg
- FINISH ELLIS TUNING
    - input shaper
        - blue goes to inside of connector
    - pressure advance, etc
- put printer on UPS
- LAN vs wireless
- start using bed mesh
- Mainsail timelapse
    - https://www.youtube.com/watch?v=n-BVPidUDLI 
    - add to super slicer
    - Printer Settings -> Custom G-code -> Before layer change Gcode -> TIMELAPSE_TAKE_FRAME
- KlipperScreen?
    - https://klipperscreen.readthedocs.io/en/latest/
- Filament sensor
    - https://www.amazon.com/dp/B07Z97582P/?coliid=I278JGHS5OD8M7&colid=3T6GGJW7T3YSG&psc=1&ref_=lv_ov_lig_dp_it
- C920 webcam
  - https://www.teamfdm.com/files/file/275-c920-mount/
  - Mount under z rail https://media.discordapp.net/attachments/710952853514223617/1031599846202822697/20221016_174843.jpg
- verify tension
    - The way I find the tension is to loosen the tension, heat up the hotend so extruder motor is energized, open the latch, insert filament, close the latch, pull. If it comes out, tighten one full turn. Pull again and repeat if it slips. Once it does not slip, add another full turn, maybe one and a half turns.


## TO PRINT
- thermistor mount for chamber temp
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/Z_Chain_Guide_Thermistor_Mount
- wago mounts
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Boingomw/Wago_mount
- 270 degree hinges, or other removable ones
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/chrisrgonzales/270_degree_hinge
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/randell/Door_Hinges
- purge bucket/nozzle wipe? 
   - https://github.com/Dfdye/Voron_Mods/tree/main/Purge_Bucket_for_WP_Kinetic_Mount
   - have one in macros already, but https://github.com/Hartk-PrinterConfigs/DoomConfig/blob/master/purge.cfg
   - maybe not tall enough https://www.printables.com/model/201999-nozzle-scrubber-with-a-little-bucket-for-voron-24
- Quick release clips
  - https://github.com/richardjm/voron-parts/tree/main/voron-2.4/FilamentLatch
- nevermore
  - https://github.com/nevermore3d/Nevermore_Micro 
  - https://github.com/MapleLeafMakers/KlipperMacros/blob/main/air_filter_timer.cfg
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
