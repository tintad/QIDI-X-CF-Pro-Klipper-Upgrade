Firmware support BTT Relay 1.2

1. 
cd ~/klipper/
make menuconfig

2.
* [*] Enable extra low-level configuration options
* Micro-controller Architecture (STMicroelectronics STM32) --->
* Processor model (STM32H723) --->
* Bootloader offset (128KiB bootloader (SKR SE BX v2.0)) --->
* Clock Reference (25 MHz crystal) --->
* Communication interface (USB (on PA11/PA12)) --->

3.
Set pin PD15 and PF8 to high on startup:
Add "PD15,PF8" to "GPIO pins to set at micro-controller startup (NEW)"
If want to set low, input "!PD15,!PF8"

4. Compile firmware at "home/pi/klipper/out/klipper.bin"
make clean
make

5.Flash firmware
press BOOT0 and RESET on the board to go to boot mode
make flash FLASH_DEVICE=0483:df11

