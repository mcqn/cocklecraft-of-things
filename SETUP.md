# Cockle Software Setup

## Hardware Requirements

 * A Sparkfun ESP8266 Thing board or an Adafruit Huzzah ESP8266 Breakout board
 * A micro-USB cable (if you've got the Sparkfun board)
 * A USB-serial cable (e.g. FTDI or CP2102) **At the moment this has only been tested with an Arduino USB2SERIAL board**
 * A computer

## Set up your development environment

### If you've got the Sparkfun ESP8266 Thing board

 1. Install the latest version of the Arduino IDE - [https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software)
 1. Plug the USB-serial board into the FTDI section of the Thing's header pins - the section marked DTR, TXO, RXI, 3V3, NC, GND.  Make sure the GND pins on both the Thing and the USB-Serial board match.
 1. Plug the other end of the USB-serial board into your computer
 1. Plug the micro-USB cable into the Thing
 1. Plug the other end of the micro-USB cable into your computer
 1. Run the Arduino IDE and follow the instructions in [Sparkfun's Thing Guide](https://learn.sparkfun.com/tutorials/esp8266-thing-hookup-guide/installing-the-esp8266-arduino-addon) to install the add-on for the ESP8266.

### If you've got the Adafruit Huzzah ESP8266 Breakout board

 1. Solder the header pins onto the breakout board - see [https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout/assembly](https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout/assembly) for details
 1. Install the latest version of the Arduino IDE - [https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software)
 1. Plug the USB-serial board into the FTDI section of the Huzzah board's header pins - the six pin header on the short side of the board.  Make sure the GND pins on both the Huzzah and the USB-Serial board match.
 1. Plug the other end of the USB-serial board into your computer
 1. Run the Arduino IDE and follow the instructions in [Adafruit's Huzzah learning guide](https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout/using-arduino-ide) to install the add-on for the ESP8266.

### If you've got a generic ESP-12 board piggy-backing onto a USB-serial board

These instructions are for [this super-cheap ESP8266 board](http://www.aliexpress.com/item/ESP8266-serial-WIFI-Witty-cloud-Development-Board-ESP-12F-module-MINI-nodemcu/32569199462.html)

Notes: These boards have an on-board RGB LED, wired to pins 15(red), 12(green) and 13(blue).

 1. Install the latest version of the Arduino IDE - [https://www.arduino.cc/en/Main/Software](https://www.arduino.cc/en/Main/Software)
 1. Run the Arduino IDE and follow the instructions in [Sparkfun's Thing Guide](https://learn.sparkfun.com/tutorials/esp8266-thing-hookup-guide/installing-the-esp8266-arduino-addon) to install the add-on for the ESP8266.
 1. Plug the micro-USB cable into the connector on the USB-serial board (the one with two buttons on it)
 1. Plug the other end of the micro-USB cable into your computer

When you're uploading code...

 1. Hold down the button marked `FLASH` (the markings are on the underside)
 1. Press the button marked `RST`
 1. Release both buttons.  The board will now be in flashing mode (and the RGB LED will be dimmer)
 1. Choose the "NodeMCU 1.0 (ESP-12E Module)" board in the `Tools -> Board` menu in the Arduino IDE
 1. Choose the right serial port in the `Tools -> Port` menu
 1. Upload the code

## Install Additional Libraries

For the temperature sensor we'll need an extra library.

 1. Run the Arduino IDE
 1. Open the library manager.  From the menu choose:
     Sketch -> Include Library -> Manage Libraries...
 1. Type "dallastemperature" into the search box in the top right corner.
 1. Click on the library by Miles Burton and others.
 1. Click on the Install button.

