# Getting Started

## Quick Setup

### 1. Hardware Connections

| Pin   | Description                        | Notes                                                                 |
|-------|------------------------------------|-----------------------------------------------------------------------|
| VCC   | 3.3V or 5V supply                  | Power supply                                                          |
| GND   | Ground                            | Common ground                                                         |
| SDA   | I2C Data Line (SDA)                | Connect to microcontroller I2C SDA pin                                |
| SCL   | I2C Clock Line (SCL)               | Connect to microcontroller I2C SCL pin                                |
| D0    | Digital I/O (separate connection)  | Not included in QWIIC connector, must be connected separately         |

> **Note:** Compatible with JST 1 mm pitch QWIIC connector for easy I2C integration (power only, D0 must be connected separately).

### 2. Software Installation

| Feature / Peripheral         | PY32F003L24D6TR |
|-----------------------------|:---------------:|
| Flash (Kbytes)              |       16        |
| SRAM (Kbytes)               |        2        |
| Advanced Timers (16-bit)    |        1        |
| General Purpose Timers      |        4        |
| Low Power Timer             |        1        |
| SysTick                     |        1        |
| Watchdog                    |        2        |
| SPI                         |        1        |
| I2C                         |        1        |
| USART                       |        1        |
| DMA Channels                |        3        |
| RTC                         |      Yes        |
| GPIOs                       |        7        |
| 12-bit ADC (ext+int)        |      4+2        |
| Comparators                 |        2        |
| Max. CPU Frequency (MHz)    |       24        |
| Operating Voltage (V)       |   1.7 ~ 5.5     |


### Package-Specific Information



```
            DFN8 Pinout (Top View):
               VCC  1 ┌─────┐ 8  PB5/LED
               PA0  2 │     │ 7  PA14-SWDCK/PB6
               PA1  3 │     │ 6  PA13-SWDIO/PA10
               PA2  4 └─────┘ 5  PB0/PF2-NRST



```

### Pinout PY32F003L24D6TR DevLab Development Board

- **VCC**: Power input for the board
- **GND**: Ground connection
- **PA0**: USART2 transmit (TX) or SPI MISO function
- **PA1**: USART2 receive (RX) or SPI SCK function
- **PA2**: Analog input channel 2 (ADC_IN2) or SPI chip select (CS)
- **PB0 / PF2**: General-purpose I/O (GPIO) or external reset (NRST)
- **PB5**: On-board LED, general-purpose I/O (GPIO), or SPI MOSI function
- **PA13 / PB6**: Serial Wire Debug I/O (SWDIO) or I2C clock line (I2C_SCL)
- **PA14 / PA10**: Serial Wire Debug clock (SWCLK) or I2C data line (I2C_SDA)
