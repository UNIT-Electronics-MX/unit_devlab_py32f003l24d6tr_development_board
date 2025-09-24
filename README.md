
# PY32F003L24D6TR DevLab Development Board

## Introduction


The DevLab Development Board based on the PY32F003L24D6TR microcontroller is designed for rapid prototyping, embedded systems education, IoT experimentation, and wearable devices. This board combines flexible power options, modern connectivity, and accessible interfaces to accelerate your hardware development.


<div align="center">
  <img src="hardware/resources/unit_top_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.png" width="450px" alt="Development Board">
  <p><em>PY32f003L24D6TR Devlab</em></p>
</div>


## 📦 Overview

| Feature                 | Description                                                   |
|------------------------|---------------------------------------------------------------|
| Microcontroller         | PY32F003L24D6TR (32-bit ARM Cortex-M0) |
| Memory                  | 24KB Flash, 4KB SRAM                                          |
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


## 🧪 Use Cases

- Device Prototyping
- Embedded Systems Education
- Networked  Alambric Devices
- Wearable Technology Development


## 🚀 Getting Started

1. **Connect** the board via USB-C to your computer.
2. **Install** the appropriate board package for:
   - Rust (e.g., `cargo install cargo-embed`) 
   - Arduino (add the board via Board Manager using URL: `https://unit-electronics-mx.github.io/arduino-board-manager/`)


3. **Flash** a sample project or use one from `/software/examples`

4. **Power** via USB or external battery (if supported)


## 📚 Resources

- [Schematic Diagram](hardware/unit_schematic_v_0_0_1_ue0102_PY32f003L24D6TR_devlab.pdf)
- [Board Dimensions (DXF)](docs/dimensions.dxf)
- [Pinout Diagram](docs/pinout.png)
- [Code Examples](software/examples)
- [Getting Started Guide](https://unit-electronics-mx.github.io/unit_py32f003l24d6tr_devlab_development_board/)
- [Documentation](https://github.com/UNIT-Electronics-MX/py32f0xx-hal)

## 📝 License

All hardware and documentation in this project are licensed under the **MIT License**.  
Please refer to [`LICENSE.md`](LICENSE.md) for full terms.



<div align="center">
  <sub>Template created by UNIT Electronics </sub>
</div>

