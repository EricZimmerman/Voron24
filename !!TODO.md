## Debug

if you are switching to CW2,  then at that time, i would :
1) dbl check no shorts in soldering
2) test with 3 wire cable to one of the endstop ports. it should behave fine and be nice and cool
if not, then i would exhcnage yours to see what is going on.

## General

- ~~mandela plate with magnets~~
    - ~~https://mandalaroseworks.com/products/voron-350-ultraflat-bed~~
    - ~~build plate https://west3d.com/products/double-sided-texture-smooth-flex-plate-with-3m-magnetic-backing-energetic-west3d-collab?variant=41130207445160 (NO MAGNET)~~
    - ~~https://www.fabreeko.com/collections/pei/products/honeybadger-v2-4-single-sided-black-pei-textured?variant=42614568452351~~
    - ~~https://dfh.fm/products/silicone-heating-pad?_pos=10&_sid=da818c221&_ss=r~~
- igus cables direct
    - https://www.igus.com/product?artNr=CF10-05-04
- sensorless end stops for x and y (SEE NOTE AT END)
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
    - Rear cable mount
        - https://github.com/hartk1213/MISC/blob/main/Voron%20Mods/Archived/Voron2.4_umbilical_strain_relief(OLD)/STL/A_Drive/%5Ba%5D_pigtail_cable_cover.stl
        - https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Voron%202/2.4/CW2_SB2040_CAN_Umbilical/STLs
- Macro ideas
    - https://github.com/zellneralex/klipper_config/tree/master
    - https://docs.vorondesign.com/community/macros/macros/120decibell.html
- FINISH ELLIS TUNING
- ~~Mainsail timelapse~~
    - ~~https://www.youtube.com/watch?v=n-BVPidUDLI ~~
    - ~~add to super slicer~~
    - ~~Printer Settings -> Custom G-code -> Before layer change Gcode -> TIMELAPSE_TAKE_FRAME~~
- KlipperScreen?
    - https://klipperscreen.readthedocs.io/en/latest/
- Filament sensor
    - https://www.amazon.com/dp/B07Z97582P/?coliid=I278JGHS5OD8M7&colid=3T6GGJW7T3YSG&psc=1&ref_=lv_ov_lig_dp_it
- C920 webcam
  - ~~https://www.teamfdm.com/files/file/275-c920-mount/~~
  - Mount under z rail https://media.discordapp.net/attachments/710952853514223617/1031599846202822697/20221016_174843.jpg
- verify tension
    - The way I find the tension is to loosen the tension, heat up the hotend so extruder motor is energized, open the latch, insert filament, close the latch, pull. If it comes out, tighten one full turn. Pull again and repeat if it slips. Once it does not slip, add another full turn, maybe one and a half turns.


## TO PRINT
- mandela bed with wago mounts at back? slick
    - https://github.com/Ramalama2/Voron-2-Mods/tree/main/Mandalaroseworks/BedPan
- ~~thermistor mount for chamber temp~~
    - ~~https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/Z_Chain_Guide_Thermistor_Mount~~
- ~~wago mounts~~
    - ~~https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Boingomw/Wago_mount~~
- 270 degree hinges, or other removable ones
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/chrisrgonzales/270_degree_hinge
    - https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/randell/Door_Hinges
    - https://github.com/LoganFraser/VoronMods/tree/main/ParametricRemovable270Hinges
- ~~purge bucket/nozzle wipe?~~
   - ~~https://www.printables.com/model/201999-nozzle-scrubber-with-a-little-bucket-for-voron-24~~
- ~~Quick release clips~~
  - ~~https://github.com/richardjm/voron-parts/tree/main/voron-2.4/FilamentLatch~~
- ~~nevermore~~
  - ~~https://github.com/nevermore3d/Nevermore_Micro~~
  - ~~https://github.com/MapleLeafMakers/KlipperMacros/blob/main/air_filter_timer.cfg~~
- SB diffuser
  - clear filament from LDO kit
- ~~z belt cover for led wire~~
  - ~~https://github.com/MotorDynamicsLab/LDOVoron2/blob/main/STLs/z_belt_cover_a_led.stl~~
- ~~exhaust cover~~
  - ~~https://voronregistry.com/mods/fiction-exhaustcoversfs~~
- nozzle holding skirt
  - https://github.com/VoronDesign/VoronUsers/blob/master/printer_mods/README.md
- ~~Top mount spool holder~~
  - ~~https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/elcrni/V2.4-Trident-Spool-Holders~~
- ~~Rock and roll for electronics access~~
  - ~~https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/RockNLol/RockNRoll~~
- ~~Scraper~~
  - ~~https://www.printables.com/model/28337-scraper-for-build-plate-version-2~~
- Updated z joints with bearing
  - https://github.com/Annex-Engineering/Other_Printer_Mods/tree/master/VORON_Printers/Reinforced_Gantry_Mounts
  - https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Voron%202/2.4/Voron2.4_GE5C
    - https://kb-3d.com/store/magnets-bearings/323-igus-ge5c-spherical-bearing-eglm-05-igubal-1634423649851.html
    - https://kb-3d.com/store/inserts-fasteners-adhesives/288-5x10x1mm-shim-ring-washer-pack-of-50-din988-1634423113147.html


## TO BUILD
### CW2 VERIFY AGAINST BOM at [https://vorondesign.com/voron_stealthburner](https://vorondesign.com/sourcing_guide?model=VSB)
- Delta fan https://west3d.com/products/delta-5015-bfb0524hh-dc24-0-16a-2-pin-cooling-fan
- ~~need motor (ordered)~~
- ~~gear kit (ordered)~~
- set ratio to 50:10
- reprint face?
    - will need fans and leds if so
    - https://www.fabreeko.com/products/stealth-burner-pre-soldered-and-crimped-leds?_pos=1&_psq=led&_ss=e&_v=1.0
    - https://kb-3d.com/store/fans/501-sunon-5015-blower-fan-24v-maglev-1646515411413.html or https://www.fabreeko.com/products/gdstime-5015-24v-blower-fan?_pos=1&_sid=76b2a2b69&_ss=r
    - https://www.fabreeko.com/products/sunon-mag-lev-4010-24v-fan?_pos=1&_psq=4010&_ss=e&_v=1.0
- 3 of M3x6 FHCS 
    - https://www.boltdepot.com/Product-Details.aspx?product=13249

# Parts URLs
- Brushes
    - https://www.aliexpress.us/item/2251832866802617.html?spm=2114.12010615.8148356.2.315e106dfzI86U&gatewayAdapt=glo2usa4itemAdapt&_randl_shipto=US
    - https://www.amazon.com/uxcell%C2%AE-Length-Plastic-Handle-Bristle/dp/B00X9HY5D4
    - https://www.amazon.com/gp/product/B092HWQG69/
- Tubing
    - https://west3d.com/products/capricornus-ptfe-tube-1-9mm-teflonto
    - https://west3d.com/products/bowden-ptfe-tube-4mm-od-2-5mm-id

I added this two jumpers, and pulled out the Y and X switches from the switches board. Then I modified printer.cfg:

[stepper_x]
...
endstop_pin: tmc2209_stepper_x:virtual_endstop #PG6
homing_retract_dist: 0 #5

[tmc2209 stepper_x]
...
diag_pin: ^PG6 # sensorless homming: use the same pin that was previously the endstop_pin!
driver_SGTHRS: 70 # sensorless homming: 255 is most sensitive value, 0 is least sensitive

[stepper_y]
...
endstop_pin: tmc2209_stepper_y:virtual_endstop #PG9
homing_retract_dist: 0 #5

[tmc2209 stepper_y]
...
diag_pin: ^PG9     # sensorless homming: use the same pin that was previously the endstop_pin!
driver_SGTHRS: 70 # sensorless homming: 255 is most sensitive value, 0 is least sensitive
