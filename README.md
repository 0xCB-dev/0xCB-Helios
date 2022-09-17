# 0xCB-Helios

### RP2040 pro micro drop in

|                              Licence                              |                                                      OSHWA                                                      |
| :---------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------: |
| ![](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/LICENSE.svg) | [![](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/rev1.0/OSHWA.svg)](https://certification.oshwa.org/.html) |

### Available here:

[KeebSupply](https://keeb.supply/products/0xcb-helios)

#### Flashing

- `qmk clone`
- `cd qmk_firmware`
- `export LTO=Y`
- To go to bootloader press the reset button.
- `make 0xcb/pluto:via:flash`

### Assembly:

You can use the [humanpnp](https://files.0xcb.dev/0xCB-Pluto/humanpnp.html) to easily place components.

### PCB:

KiCad 6 stable

[Schematic](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/rev1.0/pluto.pdf)

|                                    Top                                     |                                    Bottom                                     |
| :------------------------------------------------------------------------: | :---------------------------------------------------------------------------: |
| ![](https://github.com/0xCB-dev/0xCB-Pluto/blob/main/rev1.0/pluto.top.png) | ![](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/rev1.0/pluto.bottom.png) |

#### BOM:

| References     | Value       | Quantity | Part Nb.            |
| -------------- | ----------- | -------- | ------------------- |
| C3, C4, C7, C8 | 100n        | 4        | C478888             |
| C2, C9, C10    | 1u          | 3        | C29936              |
| C5, C6         | 22p         | 2        | C85969              |
| C1             | 10u         | 1        | C85713              |
| R1, R2         | 5.1k        | 2        | C23186              |
| R4, R5         | 22          | 2        | C174301             |
| R3, R6         | 10k         | 2        | C98220              |
| D1             | SMF5.0CA    | 1        | 576-SMF5.0CA        |
| U1             | USBLC6-2SC6 | 1        | C7519               |
| U2             | ATMEGA32U4  | 1        | ATMEGA32U4RC-MU-ND  |
| Y1             | 16MHz       | 1        | C389842             |
| F1             | 1A          | 1        | C369150             |
| SW1            | SW_Push     | 1        | C589221             |
| FB1, FB2       | 600R        | 2        | C74330              |
| J1             | USB_IN      | 1        | 900-2169900001CT-ND |
