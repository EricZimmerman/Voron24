# Print start

```
M104 S0 ; Stops PS/SS from sending temp waits separately
M140 S0
PRINT_START BED_TEMP=[first_layer_bed_temperature] EXTRUDER_TEMP={first_layer_temperature[initial_extruder]+extruder_temperature_offset[initial_extruder]} CHAMBER_TEMP=[chamber_temperature] SIZE={first_layer_print_min[0]}_{first_layer_print_min[1]}_{first_layer_print_max[0]}_{first_layer_print_max[1]} MATERIAL=[filament_type]
```

optional other variables
```
Z_ADJUST=0.x
SOAK=20
CHAMBER_TEMP=110
CHAMBER_MAXTIME=5
```


# before layer change
```
TIMELAPSE_TAKE_FRAME
```

![image](https://user-images.githubusercontent.com/4265254/197418259-1bb9ad23-bcfa-406e-bdac-0d90683a772e.png)
