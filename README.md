# Tait TM8100 USB programming module

Design files and documentation for Tait TM8100 USB programmer board. This board plugs into a Tait TM8100 series radio
via the front panel db9 connector. It can then be programmed with a Windows PC (or virtual machine) using the Tait
programming software. See [TARPN Tait documentation](http://tarpn.net/t/builder/tait_tm8105_notes/builders_radios_tait8105.html) 
for more details.

Once assembled, the board must be configured using the [software from Microchip](https://www.microchip.com/en-us/product/MCP2200).
This is needed to invert the UART rx/tx signal levels as required by the Tait radios.

<img width="1027" alt="Screen Shot 2021-07-30 at 9 13 10 AM" src="https://user-images.githubusercontent.com/55116/127658022-1a494baf-c691-4a6c-842f-5ee45fdfba4d.png">

