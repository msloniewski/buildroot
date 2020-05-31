Seed Studio ODYSSEY-STM32MP157C

Intro
=====

This configuration supports the ODYSSEY-STM32MP157C:

  https://www.seeedstudio.com/ODYSSEY-STM32MP157C-p-4464.html

How to build
============

 $ make odyssey-stm32mp157c
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
