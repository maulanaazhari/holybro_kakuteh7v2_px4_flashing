# holybro_kakuteh7v2_px4_flashing

## download the boot loader into the board
- ```sudo apt-get install dfu-util```
- connect the board while pushing the DFU button
- ```dfu-util -a 0 --dfuse-address 0x08000000:force:mass-erase:leave -D ./holybro_kakuteh7v2_bootloader.bin```
- disconnect the board
- connect the board while pushiong the DFU button
- ```dfu-util -a 0 --dfuse-address 0x08000000 -D ./build/holybro_kakuteh7v2_bootloader/holybro_kakuteh7v2_bootloader.bin```
- disconnect the board
- open QGC/Firmware page
- connect the board normally
- the flashing page will open -> check advanced -> choose local build firmwar **holybro_kakuteh7v2_default.px4**
- wait several minutes until the board is connected
## done!
