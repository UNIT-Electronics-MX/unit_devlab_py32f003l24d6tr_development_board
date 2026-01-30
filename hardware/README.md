# Hardware

<div align="center">
<a href="./unit_schematic_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.pdf"><img src="resources/Schematics_icon.jpg?raw=false" width="300px"><br/> Schematics</a>
</div>

## Technical Specifications

- **Microcontroller:** PY32f003L24D6TR (ARM Cortex-M0)
- **Core Architecture:** 32-bit ARM Cortex-M0
- **Clock Speed:** 24 MHz
- **Flash / RAM:** 16 KB Flash, 2 KB SRAM
- **Wireless:** None
- **Interfaces:** I2C, SPI, UART, ADC
- **Connector:** QWIIC + Pin Headers
- **Power:**
  - Input via USB-C: 5V
  - Regulated Output: 3.3V
  - Battery Support: No
  - Microcontroller voltage: 3.3V or 5V selected by jumper bridge

### Electrical characteristics

<div align="center">

| **Parameter** |                 **Description**                 | **Min** | **Typ** | **Max** | **Unit** |
|:-------------:|:-----------------------------------------------:|:-------:|:-------:|:-------:|:--------:|
|      Vin      |      Input voltage to power on the module       |   2.5   |    -    |   5.5   |    V     |
|     Ivcc      | Current flowing into VCC pin of microcontroller |    -    |    -    |   100   |    mA    |
|     I3v3*     |        Maximum current of 3V3 regulator         |    -    |    -    |   600   |    mA    |
|      Iio      |       Maximum Input/Output current of IOs       |    -    |    -    |   20    |    mA    |
|     f_ext     |          User external clock frequency          |    -    |    8    |   32    |   MHz    |
|      Vih      |            Input high level voltage             | 0.7 VCC |    -    |    -    |    V     |
|      Vil      |             Input low level voltage             |    -    |    -    | 0.3 VCC |    V     |
|      Vol      |            Output low level voltage             |    -    |    -    |   0.4   |    V     |
|      Voh      |            Output high level voltage            | VCC-0.4 |    -    |    -    |    V     |

*Optimal thermal management is required for the regulator to perform reliably at maximum output current.

</div>


##  Pinout

<div align="center">
<a href="./unit_pinout_v_0_0_1_ue0102_py32f003_en.pdf"><img src="./resources/unit_pinout_v_0_0_1_ue0102_py32f003_en.jpg" width="500px"><br/> Pinout</a>
</div>

### **Pinout Details**

<div align="center">

| Pin Label | Function / Notes                |
|-----------|------------------|
| VCC       | Power Input     | 
| GND       | Ground          |
| PA0      |  USART2_TX  MISO  |
| PA1      |  USART2_RX  SCK |
| PA2      | ADC_IN2      CS|
| PB0  / PF2    |  GPIO / NRST    |
| PB5      | LED Built In / GPIO / MOSI     |
| PA14 / PB6    | SWC /  I2C_SCL   |
| PA13 / PA10    | SWD /  I2C_SDA   |

</div>

### Connectivity Options

- **I2C:** JST 1mm QWIIC connector (Power + I2C lines)
- **SPI:** JST 1mm connector (Power + SPI lines)
- **GPIO:** 2x 4-pin headers for general-purpose I/O
- **SWD:** Dedicated pins for programming and debugging

## Board Topology

<div align="center">
<a href="./resources/unit_topology_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.png"><img src="./resources/unit_topology_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.png" width="500px"><br/>Topology</a> <br/><br/>

| Ref.  | Description                                                                 |
|-------|-----------------------------------------------------------------------------|
| IC1   | PY32f003L24D6TR Microcontroller                                             |
| U1    | AP2112K 3.3V Regulator                                                      |
| SW1   | Reset Push Button                                                           |
| L1    | Power On LED                                                                |
| L2    | Built In LED to PB5                                                         |
| J1    | JST 1mm Connector for I2C or JTAG                                           |
| J2    | JST 1mm Connector for I2C or JTAG                                           |
| J3    | JST 1mm Connector for SPI                                                   |
| JP1   | Header for GPIOs                                                            |
| JP2   | Header for GPIOs                                                            |
| JP3   | Header for Power Supply Selection                                           |
| SB1   | Solder Bridge to Enable LED Built In                                        |
</div>

## Board Dimensions

<div align="center">
<a href="./resources/unit_dimension_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.png"><img src="./resources/unit_dimension_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.png" width="500px"><br/>Dimensions</a>
</div>

## References
- [Datasheet](https://download.py32.org/Datasheet/en/PY32F003_Datasheet_Rev1.7.pdf)
