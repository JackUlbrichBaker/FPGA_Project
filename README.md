# FPGA_Project
This is my first FPGA project, with the aim of emulating a vintage cpu cores.

# Inspiration
I drew inspiration from many different Boards, but primarily from the Hackaday SuperCon "badge" and the Orange Crab Dev board:
 - https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/
 - https://orangecrab-fpga.github.io/orangecrab-hardware/

# Component Selection
FPGA: ECP5-12F FPGA
I selected this family of FPGAs for their low cost primarily as well as their upgradability as I can prototype with the cheaper 12k LUT version and when it is finalised I can develop with up to 85k LUTs (way overkill for my application anyway).  Specs shown below;

- 12 K - Look Up Tables
- 1008 Kb - Embedded Block RAM
- 194 Kb - Distributed RAM
- 28 - 18x18 Multipliers
- PLLs: 2
- Internal oscillator
- Flexible I/O for DDR3 Memory Support

### Memory: DDR3L 
- MT41K64M16TW-107 DDR3 RAM
- 128 Mbytes (1Gbit)
- 64M x16
- 1.35V low voltage operation

### Flash:
- I selected to use the Winbond W25Q128JVSIM
- enable config loading from flash to avoid reflashing on every power up 
- SPI enabled

### USB: 
- FT2232H interface (USB C plug)

### Power:
- The board needs: 1.1V, 2.5V, 3.3V and can supply 5V
- The board will be able to be powered by USB or barrel Jack
- to supply this I will use the following:
  - 1.1V: 500mA max -- Buck Converter
  - 2.5V: 200mA max -- Linear Regulator
  - 3.3V: 700mA - designed for 1A -- Switching step up
  - 5.0V: 500mA - designed for 1A -- Switching step up

### IO:
- Array of 8 LEDS that can be used as generic LEDs or to represent an 8 bit bus/memory
- Array of 8 switches for the same reason

### Connectivity:
- USB-C
- JTAG
- UART

# Software:

To include HDMI I will utilize this repo:
- https://github.com/hdl-util/hdmi/
As a DFU Bootloader I will be using this:
- https://github.com/no2fpga/no2bootloader

# TODO:
- [ ] Select Components
- [ ] Create Schematic
- [ ] Route PCB
- [ ] Design review
- [ ] Production
- [ ] Testing
