Hardware Pinout
===============

This section describes the pin mapping of the DevLab Development Board
based on the PY32F003L24T6 microcontroller.

Pinout Diagram
--------------

.. image:: _static/unit_pinout_v_0_0_1_ue0102_py32f003_en.jpg
   :alt: DevLab PY32F003L24T6 Pinout Diagram
   :align: center
   :width: 90%

The image above shows the physical pinout of the DevLab board and its
relationship with the PY32F003L24T6 MCU pins.

Board Pin Description
---------------------

.. list-table:: DevLab Pinout Overview
   :header-rows: 1
   :widths: 25 75

   * - Pin Label
     - Description
   * - VCC
     - Power input
   * - GND
     - Ground
   * - PA0
     - USART2_TX / SPI1_MISO
   * - PA1
     - USART2_RX / SPI1_SCK
   * - PA2
     - ADC_IN2 / SPI_CS
   * - PB0 / PF2
     - GPIO / NRST
   * - PB5
     - Built-in LED / GPIO / SPI_MOSI
   * - PA13
     - SWDIO / I2C_SDA
   * - PA14
     - SWCLK / I2C_SCL
   * - PB6
     - GPIO / I2C_SCL (alternate)
   * - PA10
     - GPIO / I2C_SDA (alternate)

Connectivity Interfaces
-----------------------

.. list-table:: Available Interfaces
   :header-rows: 1
   :widths: 20 80

   * - Interface
     - Description
   * - I2C
     - JST 1.0 mm QWIIC connector (Power + I2C)
   * - SPI
     - JST 1.0 mm connector (Power + SPI)
   * - GPIO
     - Two 4-pin headers for general-purpose I/O
   * - SWD
     - Dedicated programming and debugging interface






