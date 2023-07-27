# Setup and Configuration options

This page will cover the basics of setting up the CYD

## Hardware Setup

There really is nothing to setup here, just connect the CYD to a computer using a micro USB cable (it even comes with one)

## Software Setup

The USB to UART driver needs to be setup on your computer for uploading to the CYD, also needed for flashing projects directly from a webpage.  
The CYD uses the CH340 USB to UART chip. If you do not have a driver already installed for this chip you may need to install one. Check out [Sparkfun's guide for installation instruction](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all)

## Coding Setup

Follow these instructions if you want to write new code for the CYD

### Arduino IDE

You will need to have to install the Arduino-ESP32 support in your Arduino IDE, [instructions can be found here](https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html).

You can then select basically any ESP32 board in the boards menu. (I usually use "ESP32 Dev Module", but it doesn't really matter)

If you see errors uploading a sketch, try setting board upload speed to `115200`

#### Library Configuration

The CYD can work with a selection of different libraries, but the main one this repo will focus on is [TFT_eSPI](https://github.com/Bodmer/TFT_eSPI) as it is a fairly popular library for working with these types of dsiplays and there are lots of examples. 

This can be installed from the library manager by searching for "TFT_eSPI".

 > Note: After install of the library, copy the file [User_Setup.h](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/blob/main/DisplayConfig/User_Setup.h) to the `libraries\TFT_eSPI` Arduino folder. This sets up the library for use with this display.

### PlatformIO IDE

If you prefer the [PlatformIO IDE](https://platformio.org/platformio-ide), you will have to install the [Espressif 32 development platform](https://registry.platformio.org/platforms/platformio/espressif32). The examples are created to use with the Arduino IDE, but I provide an example of the needed platformio.ini and the code in the ino can be copied to main.cpp.  
The content of platformio.ini will take care of the installation of "TFT_eSPI" and the settings in User_Setup.h.

### Examples

I have provided examples for you to try out to get some ideas or inspiration. [Check them out here.](/examples/)
