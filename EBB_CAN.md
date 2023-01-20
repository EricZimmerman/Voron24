This is a quick write up on how do deal with BTT parts as it relates to CAN. this in no way is meant to take away from the awesome work that Maz0r did, which is [here](https://github.com/maz0r/klipper_canbus/).

Rather, this document covers using the U2C 2.1 and EBB36 to get CAN going for a typical setup.

Why write this? its a pretty common setup and it can be confusing/easy to miss some of the steps, so here we go.

# Pi

Summarized from https://github.com/maz0r/klipper_canbus/blob/main/controller/u2c.md

1. Use nano to create a new file with the command `sudo nano /etc/network/interfaces.d/can0`
2. Add the following code
```
allow-hotplug can0
iface can0 can static
 bitrate 1000000
 up ifconfig $IFACE txqueuelen 256
 pre-up ip link set can0 type can bitrate 1000000
 pre-up ip link set can0 txqueuelen 256
 ```

3. Save the file with `CTRL-x' and reboot the pi with `sudo reboot`

4. Verify the network via `ip -s link show can0` which should reflect that the CAN network is UP

# U2C

Note that the U2C does not need much done to it, short of making sure it has the newest firmware from BTT that fixed an earlier
issue with not being able to use CANBoot to flash things behind the U2C on older firmware. Once you do the steps below, you do not
have to touch the U2C again

1. make sure you have the latest firmware for the U2C from BTT, which is available here: https://github.com/Arksine/CanBoot/issues/44#issuecomment-1381555466
2. The steps to flash this firmware are (taken from above link):
  - Download the file from bigtreetech comment.
  - Stop klipper sudo systemctl stop klipper
  - Bring down the can interface sudo ifdown can0
  - Unzip the firmware file from bigtreetech
  - Unplug the u2c controller from usb
  - Press and hold the boot button on the u2c and plug the usb cable back in, then release the boot button.
  - Verify that the u2c is in dfu mode dfu-util -l You should see lines that contain Found DFU: [0483:df11]
  - Flash the new firmware to the u2c dfu-util -D G0B1_U2C_V2.bin -d 0483:df11 -a 0 -s 0x08000000:leave
  - Unplug and replug in the usb cable for the u2c to reset it
  - The CAN interface should now be back up
  - Follow the steps to compile and flash canboot to the EBB
  - Follow the steps to compile and flash klipper over CAN
  - Success
3. When this is done, ADD THE JUMPER for the 120 ohm resistor to the U2C and set the U2C aside

# Ebb

Go to https://github.com/maz0r/klipper_canbus/blob/main/toolhead/ebb36-42_v1.1.md and do what it says, with the following changes:

1. Use a CAN bus speed of 1000000 everywhere the guide shows 500000
2. When you get to step 7, STOP after disconnecting the board from USB
3. 3. When this is done, ADD THE JUMPER for the 120 ohm resistor to the U2C and set the EBB aside

# Connecting all the things

For my setup, I chose to wire things like this:

![image](https://user-images.githubusercontent.com/4265254/213817757-1c06da9b-09d2-4e6c-9193-34c6f895c70f.png)

Now there is nothing wrong with wiring up your 24v right to the EBB board (more on that in a minute), but for me, I found this to be the simplest way to set things up.

I am using 22awg Igus cable for my CAN cable. You will need to get motion rated wire, or something with a high strand count (19 or more) so you do not have issues with things breaking later.

Make your cable and route it however you want. Some people use a glad back the A motor mount, I chose to run it out up by where the bowden tube exits. As long as the 4 wires gets from the toolhead to under the deck, its probably not wrong.

Next up is wiring up the plugs for the CAN cable. Refer to the following images from GadgetAngel:

![image](https://user-images.githubusercontent.com/4265254/213820399-95616f29-eccd-40ab-8a78-5ed4f9fe95a3.png)

![image](https://user-images.githubusercontent.com/4265254/213820413-6fae73af-ae0e-40b9-a9ae-c058309c8147.png)


TRIPLE CHECK your plarity and wiring here. The BTT stuff is not the same on both sides.

Once you have the cable wired up (i used the molex connection), plug it into the toolhead and the U2C (or however you decided to power things up.

# Verifying you see CanBoot and flashing Klipper to the Ebb

(Some steps taken from https://github.com/maz0r/klipper_canbus/blob/main/toolhead/ebb36-42_v1.1.md, which you should review as well)

At this point, after checking twice that everything is connected correctly, power up the printer and SSH into the pi.

1. Open this webpage: https://github.com/maz0r/klipper_canbus/blob/main/toolhead/ebb36-42_v1.1.md
2. Scroll down to step 9
3. Do what it says, making sure to use a CAN bus speed of 1000000 vs 500000
4. Follow the rest of the page until the end, where it directs you to the config file

# Wiring up a config file

1. On the pi, run the following commands:

```
cd ~/printer_data/config
wget https://github.com/maz0r/klipper_canbus/blob/main/toolhead/example_configs/toolhead_btt_ebbcan_G0B1_v1.2.cfg
```

2. Edit the file using nano
```
nano toolhead_btt_ebbcan_G0B1_v1.2.cfg
```

3. Remember the UUID you recorded earlier? Find it and scroll down to the section that looks like this:
```
[mcu can0]
canbus_uuid: 2c77b9d71a11
```
5. Replace `2c77b9d71a11` with YOUR UUID
6. EXPLAIN WIRING UP FAN to teSt THINGS
7. Explain including it in printer.cfg
8. explain testing fan in mainsail manually
9. explain reversing the fan changes
10. explain removing all the old stuff and wiring up the toolhead to hot end, fans, etc.
