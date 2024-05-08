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
Set pin PD14 and PF8 to high on startup:
Add "PD14,PF8" to "GPIO pins to set at micro-controller startup (NEW)"
If want to set low, input "!PD14,!PF8"

4. make at home/pi/klipper/out/klipper.bin
make clean
make
