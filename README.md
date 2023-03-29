# Tait TM8100 USB programming module

This board is bespoke USB to UART converter for programming Tait TM8100 series radios. It connects to the front
end of a radio using a DB9 connector and provides a sturdy USB-B connector for interfacing with a PC. The board
uses the MCP2200 chip from Microchip.

The current version is [v2](https://github.com/mumrah/tait-usb-programmer/tree/main/v2)

## Usage

To use the programmer, two pieces of software are required:

1) MCP2200 Windows Driver https://ww1.microchip.com/downloads/en/DeviceDoc/MCP2221_Windows_Driver_2021-02-22.zip
2) Tait TM8100 Programming Software (can be found in the [TARPN Tait documentation](http://tarpn.net/t/builder/tait_tm8105_notes/builders_radios_tait8105.html)).

If the MCP2200 driver link is dead, check the product page for a new link https://www.microchip.com/en-us/product/MCP2200 
and [file an issue](https://github.com/mumrah/tait-usb-programmer/issues) against this repository.

The board is designed to plug directly into the front panel of a TM810x radio. A USB-B to USB-A cable (such as a modern
printer cable) is then used to connect the programmer board into a PC. 

Once the board is plugged in and detected by Windows, check the Device Manager to determine which COM port
the programmer was registered as.

![Device Manager](https://user-images.githubusercontent.com/55116/228540396-b2e9b2b4-a6fe-42e1-aebd-1d566e8a1aa8.jpg)

In the Tait software, under Tools -> Options, select the COM port that was found in the Device Manager

![Tait COM Selection](https://user-images.githubusercontent.com/55116/228540702-20a0843b-406c-40a7-bac5-83022a005d45.jpg)

At this point, you can either "Read the Radio" or "Interrogate the Radio" using the Tait software. Refer to the 
[TARPN Tait documentation](http://tarpn.net/t/builder/tait_tm8105_notes/builders_radios_tait8105.html) for more details
on programming specifics.

## Programming the Programmer

This section only applies if you are building your own programmer. Once assembled, the board must be configured using 
the [software from Microchip](https://www.microchip.com/en-us/product/MCP2200). This is needed to invert the UART rx/tx 
signal levels as required by the Tait radios. With newer versions of the board (v2 and later), LEDs can be enabled by 
selecting "Enable Tx/Rx LEDs"

<img width="1027" alt="Screen Shot 2021-07-30 at 9 13 10 AM" src="https://user-images.githubusercontent.com/55116/127658022-1a494baf-c691-4a6c-842f-5ee45fdfba4d.png">


## Action Shot

Here is a video of a v2 board reading from a Tait TM8105

https://user-images.githubusercontent.com/55116/129118886-56906c2b-b291-4ea8-aef9-7abf3eee217b.mov


