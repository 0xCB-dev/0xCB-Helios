# 0xCB-Helios

### RP2040 pro micro drop in

|                              Licence                              |                                                      OSHWA                                                      |
| :---------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------: |
| ![](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/LICENSE.svg) | [![](https://github.com/0xCB-dev/0xcb-Pluto/blob/main/rev1.0/OSHWA.svg)](https://certification.oshwa.org/.html) |

### Available here:

[KeebSupply](https://keeb.supply/products/0xcb-helios)

### GPIO Functions

| GPIO | F1       | F2        | F3       | F4     | F5  | F6   | F7   | F8           | F9            |
|------|----------|-----------|----------|--------|-----|------|------|--------------|---------------|
| 0    | SPI0 RX  | UART0 TX  | I2C0 SDA | PWM0 A | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 1    | SPI0 CSn | UART0 RX  | I2C0 SCL | PWM0 B | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 2    | SPI0 SCK | UART0 CTS | I2C1 SDA | PWM1 A | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 3    | SPI0 TX  | UART0 RTS | I2C1 SCL | PWM1 B | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 4    | SPI0 RX  | UART1 TX  | I2C0 SDA | PWM2 A | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 5    | SPI0 CSn | UART1 RX  | I2C0 SCL | PWM2 B | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 6    | SPI0 SCK | UART1 CTS | I2C1 SDA | PWM3 A | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 7    | SPI0 TX  | UART1 RTS | I2C1 SCL | PWM3 B | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 8    | SPI1 RX  | UART1 TX  | I2C0 SDA | PWM4 A | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 9    | SPI1 CSn | UART1 RX  | I2C0 SCL | PWM4 B | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 10   | SPI1 SCK | UART1 CTS | I2C1 SDA | PWM5 A | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 11   | SPI1 TX  | UART1 RTS | I2C1 SCL | PWM5 B | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 12   | SPI1 RX  | UART0 TX  | I2C0 SDA | PWM6 A | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 13   | SPI1 CSn | UART0 RX  | I2C0 SCL | PWM6 B | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 14   | SPI1 SCK | UART0 CTS | I2C1 SDA | PWM7 A | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 15   | SPI1 TX  | UART0 RTS | I2C1 SCL | PWM7 B | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 16   | SPI0 RX  | UART0 TX  | I2C0 SDA | PWM0 A | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 17   | SPI0 CSn | UART0 RX  | I2C0 SCL | PWM0 B | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 18   | SPI0 SCK | UART0 CTS | I2C1 SDA | PWM1 A | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 19   | SPI0 TX  | UART0 RTS | I2C1 SCL | PWM1 B | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 20   | SPI0 RX  | UART1 TX  | I2C0 SDA | PWM2 A | SIO | PIO0 | PIO1 | CLOCK GPIN0  | USB VBUS EN   |
| 21   | SPI0 CSn | UART1 RX  | I2C0 SCL | PWM2 B | SIO | PIO0 | PIO1 | CLOCK GPOUT0 | USB OVCUR DET |
| 22   | SPI0 SCK | UART1 CTS | I2C1 SDA | PWM3 A | SIO | PIO0 | PIO1 | CLOCK GPIN1  | USB VBUS DET  |
| 23   | SPI0 TX  | UART1 RTS | I2C1 SCL | PWM3 B | SIO | PIO0 | PIO1 | CLOCK GPOUT1 | USB VBUS EN   |
| 24   | SPI1 RX  | UART1 TX  | I2C0 SDA | PWM4 A | SIO | PIO0 | PIO1 | CLOCK GPOUT2 | USB OVCUR DET |
| 25   | SPI1 CSn | UART1 RX  | I2C0 SCL | PWM4 B | SIO | PIO0 | PIO1 | CLOCK GPOUT3 | USB VBUS DET  |
| 26   | SPI1 SCK | UART1 CTS | I2C1 SDA | PWM5 A | SIO | PIO0 | PIO1 |              | USB VBUS EN   |
| 27   | SPI1 TX  | UART1 RTS | I2C1 SCL | PWM5 B | SIO | PIO0 | PIO1 |              | USB OVCUR DET |
| 28   | SPI1 RX  | UART0 TX  | I2C0 SDA | PWM6 A | SIO | PIO0 | PIO1 |              | USB VBUS DET  |
| 29   | SPI1 CSn | UART0 RX  | I2C0 SCL | PWM6 B | SIO | PIO0 | PIO1 |              | USB VBUS EN   |


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
