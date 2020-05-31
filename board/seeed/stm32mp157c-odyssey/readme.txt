Seed Studio STM32MP157C-ODYSSEY

Intro
=====

This configuration supports the STM32MP157C-ODYSSEY:

  https://www.seeedstudio.com/ODYSSEY-STM32MP157C-p-4464.html

How to build
============

 $ make stm32mp157c-odyssey
 $ make

How to write the microSD card
=============================

Once the build process is finished you will have an image called
"sdcard.img" in the output/images/ directory.

Copy the bootable "sdcard.img" onto an microSD card with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX

Boot the board
==============

 (1) Insert the microSD card in SD card connector.

 (2) Plug a usb-uart converter in debug uart connector and run your serial
     communication program on /dev/ttyUSBx.

 (3) Plug a USB-C cable to power-up the board.

 (4) The system will start, with the console on UART.
