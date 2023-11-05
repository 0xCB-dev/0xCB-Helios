# 0xCB-Helios

### RP2040 pro micro drop in

|                              Licence                               |                                                      OSHWA                                                       |
| :----------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------: |
| ![](https://github.com/0xCB-dev/0xcb-Helios/blob/main/LICENSE.svg) | [![](https://github.com/0xCB-dev/0xcb-Helios/blob/main/rev1.0/OSHWA.svg)](https://certification.oshwa.org/de000131.html) |

### Available here

[KeebSupply](https://keeb.supply/products/0xcb-helios)

[Ringer Keys](https://ringerkeys.com/collections/modders-tools/products/0xcb-helios)

[Keycapsss](https://keycapsss.com/keyboard-parts/mcu-controller/257/0xcb-helios-pro-micro/elite-c-compatible-microcontroller-with-rp2040?c=22)

#### Flashing

- `qmk clone`
- `cd qmk_firmware`
- To go to bootloader press the reset button longer than 500ms and release. Alternatively you can short the RST pin to GND, as it's wired to the reset button.
- `make 0xcb/helios:default:flash`

### Assembly

The PCBs are assembled at the fab with the production files located in the /kikit/prod/ dir.

### Integration in your own design

We strongly recommend that you take a look at [ebastler's symbol and footprint library for KiCAD](https://github.com/ebastler/marbastlib).
The Helios files are located in the "promicroish" folder with various mounting options to choose from. 
If you need any help integrating Helios into your keyboard PCB, please feel free to contact us.

### PCB

KiCad 6 stable

[Schematic](https://github.com/0xCB-dev/0xcb-Helios/blob/main/rev1.0/helios.pdf)

### Pinout

![](https://github.com/0xCB-dev/0xCB-Helios/blob/main/rev1.0/helios.webp)

| GPIO | F1       | F2        | F3       | F4     | F5  | F6   | F7   | F8           | F9            |
| ---- | -------- | --------- | -------- | ------ | --- | ---- | ---- | ------------ | ------------- |
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

#### BOM:

| Comment                 | Designator                             | Footprint                                           | LCSC     |
| ----------------------- | -------------------------------------- | --------------------------------------------------- | -------- |
| 4u7                     | C1                                     | Capacitor_SMD:C_0402_1005Metric                     | C23733   |
| 10u                     | C2,C3,C4,C5                            | Capacitor_SMD:C_0402_1005Metric                     | C15525   |
| 100n                    | C6,C11,C12,C13,C14,C15,C16,C17,C18,C19 | Capacitor_SMD:C_0402_1005Metric                     | C1525    |
| 15p                     | C7,C8                                  | Capacitor_SMD:C_0402_1005Metric                     | C1548    |
| 1u                      | C9,C10                                 | Capacitor_SMD:C_0402_1005Metric                     | C52923   |
| Power LED               | D1                                     | Diode_SMD:D_0402_1005Metric                         | C130719  |
| User LED                | D2                                     | Diode_SMD:D_0402_1005Metric                         | C130724  |
| PMEG2010BELD            | D3                                     | 0xcb:SOD882D                                        | C552820  |
| 500mA                   | F1                                     | Fuse:Fuse_0603_1608Metric                           | C210357  |
| 600R                    | FB1                                    | Resistor_SMD:R_0402_1005Metric                      | C160977  |
| USB_C_Receptacle_USB2.0 | J1                                     | 0xcb:GT-USB-7014C                                   | C963373  |
| 2N7002VC-               | Q1,Q2                                  | Package_TO_SOT_SMD:SOT-563                          | C504145  |
| 10k                     | R1,R2,R3,R11,R17                       | Resistor_SMD:R_0402_1005Metric                      | C25744   |
| 51K                     | R4,R5,R6                               | Resistor_SMD:R_0402_1005Metric                      | C25794   |
| 5k1                     | R7,R8,R16                              | Resistor_SMD:R_0402_1005Metric                      | C25905   |
| 1K                      | R9                                     | Resistor_SMD:R_0402_1005Metric                      | C11702   |
| 1k                      | R10,R14,R15                            | Resistor_SMD:R_0402_1005Metric                      | C11702   |
| 27R                     | R12,R13                                | Resistor_SMD:R_0402_1005Metric                      | C25100   |
| SWITCH                  | SW1                                    | 0xcb:1.9x2.8mm SW                                   | C589221  |
| USBLC6-2P6              | U1                                     | Package_TO_SOT_SMD:SOT-666                          | C2827693 |
| TLV75533PDQNR           | U2                                     | 0xcb:X2SON-4                                        | C2861882 |
| W25Q128JVPIQ            | U3                                     | 0xcb:W25Q128JVPIQ                                   | C190862  |
| RP2040                  | U4                                     | Package_DFN_QFN:QFN-56-1EP_7x7mm_P0.4mm_EP3.2x3.2mm | C2040    |
| 74LVC1T45               | U5                                     | Package_TO_SOT_SMD:SOT-563                          | C352970  |
| 12MHz                   | Y1                                     | Crystal:Crystal_SMD_2520-4Pin_2.5x2.0mm             | C2149204 |

### Credits

The awesome one button reset circuit is based on the one used on the [Sea-picro](https://github.com/joshajohnson/sea-picro) by joshajohnson and this very well written [article](https://acheronproject.com/reset_article_1/reset_article_1/) by the Acheron Project.

Thank you! :heart:
