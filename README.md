# FPGA_Project
This is my first FPGA project, with the aim of emulating a vintage cpu cores.

# Inspiration
I drew inspiration from many different Boards, but primarily from the Hackaday SuperCon "badge" and the Orange Crab Dev board:
https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/
https://orangecrab-fpga.github.io/orangecrab-hardware/

# Component Selection
FPGA: ECP5-12F FPGA
I selected this family of FPGAs for their low cost primarily as well as their upgradability as I can prototype with the cheaper 12k LUT version and when it is finalised I can develop with up to 85k LUTs (way overkill for my application anyway).  Specs shown below;

12 K - Look Up Tables
1008 Kb - Embedded Block RAM
194 Kb - Distributed RAM
28 - 18x18 Multipliers
PLLs: 2
Internal oscillator
Flexible I/O for DDR3 Memory Support

Memory: DDR3L 
128 Mbytes (1Gbit)
64M x16
1.35V low voltage operation

Connectivity:
USB-C
JTAG
UART
