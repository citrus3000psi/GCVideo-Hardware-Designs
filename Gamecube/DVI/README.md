Thanks to Unseen and Happy_Bunny.  Without them, this project would not exsist.

This design consists of three PCBS.

QSB which attaches to the bottom of the Digital out port
Main PCB which attaches to the QSB
HDMI QSB Extentsion board which brings the HDMI signals to the back of the Gamecube.

The Three boards can be found here (BOM are listed in the descriptions):

https://oshpark.com/shared_projects/6uNkT6dc

https://oshpark.com/shared_projects/K7X2uxXV

https://oshpark.com/shared_projects/Zte7gvJZ

The flash is now listed as EOL, but this flash should be a drop in replacement (untested): MX25V4006EM1I-13

You will need to program the flash with an SPI programmer. I use an Lcsoft CY7C68013A  I program the board before installing, it is just eaiser that way.

CLK=PA0

MOSI=PA1

MISO=PA2

CS=PA3

GND=GND

3.3=3.3

Programming is easy once you know the steps.

You will need the following files:

Cypress USB Suite: http://www.cypress.com/documentation/software-and-drivers/suiteusb-34-usb-development-tools-visual-studio

LCSOFT Driver: http://www.retro-system.com/AN58764_with_spi.zip (Credits to Happy_Bunny)

Flash Program: http://www.retro-system.com/new_fpga_flash.zip (Credits to Happy_Bunny)

Flash File: 

Plug in the LCSoft, and use the supplied drivers.  You might need disable driver signature enforcement within windows.

-Load up CYConsole (You should see your device listed), hit options and go to EZ-USB-Interface.

-Hit the Download button and select the VirtualCom.Hex file located in the Virtual COM Example Code from the above zip.

-You now should have a COM port listed in device manager.  Find out what COM port number it is.

-You are now ready to flash.

new_fpga_flash.exe COM1 gcvideo-dvi-shuriken-v3-2.3.bin

This is a rough install guide.  There is a lot of assumptions here that you know how to use the Command Prompt etc.



