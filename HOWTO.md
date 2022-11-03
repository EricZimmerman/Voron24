#  Klicky stuff
https://github.com/LoganFraser/VoronMods/tree/main/KlickySetup

# Verify extruder tension

- Loosen the tension
- Heat up the hotend so extruder motor is energized
- Open the latch
- Insert filament
- Close the latch and pull
- If it comes out, tighten one full turn
- Pull again and repeat if it slips
- Once it does not slip, add another full turn, maybe one and a half turns

# Update klipper firmware from the pi

1. Update all software
2. Run this

```
cd ~/klipper
make clean
make menuconfig
 ```

3. Set options per image below
5. Q and save when prompted
6. Flash with comand below (ADJUST YOUR ID ACCORDINGLY)
7. ???
8. Profit

```
sudo service klipper stop
make flash FLASH_DEVICE=/dev/serial/by-id/usb-Klipper_stm32f446xx_310012001550324E31333220-if00
sudo service klipper start
```


![image](https://user-images.githubusercontent.com/4265254/198883349-bb3c9e14-1339-4a10-8706-6c6e036a2dcb.png)
