This is a quick write up on how do deal with BTT parts as it relates to CAN. this in no way is meant to take away from the awesome work that Maz0r did, which is [here](https://github.com/maz0r/klipper_canbus/).

Rather, this document covers using the U2C 2.1 and EBB36 to get CAN going for a typical setup.

Why write this? its a prettu common setup and it can be confusing/easy to miss some of the steps, so here we go.

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

3. Save the file with `CTRL-x'

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
3. When this is done, ADD THE JUMPER for the 120 ohm resistor to the U2C and set it aside

# Ebb




![image](https://user-images.githubusercontent.com/4265254/213817757-1c06da9b-09d2-4e6c-9193-34c6f895c70f.png)





![image](https://user-images.githubusercontent.com/4265254/213817745-aa9538a4-3514-4722-9ea6-e516d97aa357.png)


