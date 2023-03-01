# holybro_kakuteh7v2_px4_flashing

## clone PX4-Autopilot repository (main or minimum v1.14.0)
```git clone --recursive https://github.com/PX4/PX4-Autopilot.git```
## make the target
```cd PX4-Autopilot && make holybro_kakuteh7v2_default```
## download the boot loader into the board
- press bootloader button in the board and connect the board to the computer while pressing the button
- ```cd PX4-Autopilot/boards/holybro/kakuteh7v2/extras```
- ```sudo apt-get install dfu-util```
- ```dfu-util -a 0 --dfuse-address 0x08000000 -D  holybro_kakuteh7v2_bootloader.bin```
## flash the new firmware to the board
- open QGroundControl -> vehicle setup -> firmware
- reconnect the board normally
- flash the board using a custom file in ```PX4-Autopilot/build/holybro_kakuteh7v2_default/holybro_kakuteh7v2_default.px4```
## done!
