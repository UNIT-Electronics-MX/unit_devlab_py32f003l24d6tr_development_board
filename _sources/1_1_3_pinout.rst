Multiplexing function mapping
=================================



GPIO Alternate Function Registers
---------------------------------

Pin multiplexing is controlled by the GPIO Alternate Function Registers
(AFR). Each pin uses 4 bits to select the alternate function.

AFR Bit Mapping
~~~~~~~~~~~~~~~

- Bits 0–3   : Pin 0
- Bits 4–7   : Pin 1
- Bits 8–11  : Pin 2
- Bits 12–15 : Pin 3
- Bits 16–19 : Pin 4
- Bits 20–23 : Pin 5
- Bits 24–27 : Pin 6
- Bits 28–31 : Pin 7

AF values:

- 0 → GPIO (default)
- 1 → AF1
- …
- 15 → AF15

Configuration Example
---------------------

Configure PA0 as USART2_TX (AF9):

.. code-block:: c

   GPIOA->AFR = (GPIOA->AFR & ~(0xF << 0)) | (9 << 0);

Design Considerations
---------------------

- PA13 / PA14 should remain reserved for SWD during development.
- I2C is recommended on PB6 / PA10 for applications.
- The onboard LED on PB5 shares SPI_MOSI.

Configuration Example
---------------------

Configure PA0 as USART2_TX (AF9):

.. code-block:: c

   GPIOA->AFR = (GPIOA->AFR & ~(0xF << 0)) | (9 << 0);

Design Considerations
---------------------

- PA13 / PA14 should remain reserved for SWD during development.
- I2C is recommended on PB6 / PA10 for applications.
- The onboard LED on PB5 shares SPI_MOSI.


PA0 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF1
     - USART1_CTS
   * - AF4
     - USART2_CTS
   * - AF7
     - COMP1_OUT
   * - AF9
     - USART2_TX
   * - AF10
     - SPI1_MISO
   * - AF13
     - TIM1_CH3
   * - AF14
     - TIM1_CH1N
   * - AF15
     - IR_OUT


PA1 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SPI1_SCK
   * - AF1
     - USART1_RTS
   * - AF4
     - USART2_RTS
   * - AF7
     - EVENTOUT
   * - AF9
     - USART2_RX
   * - AF10
     - SPI1_MOSI
   * - AF13
     - TIM1_CH4
   * - AF14
     - TIM1_CH2N
   * - AF15
     - MCO


PA2 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SPI1_MOSI
   * - AF1
     - USART1_TX
   * - AF4
     - USART2_TX
   * - AF7
     - COMP2_OUT
   * - AF10
     - SPI1_SCK
   * - AF12
     - I2C_SDA
   * - AF13
     - TIM3_CH1


PB0 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SPI1_NSS
   * - AF1
     - TIM3_CH3
   * - AF2
     - TIM1_CH2N
   * - AF5
     - EVENTOUT
   * - AF7
     - COMP1_OUT


PB5 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SPI1_MOSI
   * - AF1
     - TIM3_CH2
   * - AF2
     - TIM16_BKIN
   * - AF3
     - USART1_CK
   * - AF4
     - USART2_CK
   * - AF5
     - LPTIM_IN1
   * - AF7
     - COMP1_OUT


PA13 – Alternate Function Mapping
---------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SWDIO
   * - AF1
     - IR_OUT
   * - AF7
     - EVENTOUT
   * - AF9
     - USART1_RX
   * - AF10
     - SPI1_MISO
   * - AF13
     - TIM1_CH2
   * - AF15
     - MCO


PA14 – Alternate Function Mapping
---------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - SWCLK
   * - AF1
     - USART1_TX
   * - AF4
     - USART2_TX
   * - AF7
     - EVENTOUT
   * - AF15
     - MCO


PB6 – Alternate Function Mapping
--------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF0
     - USART1_TX
   * - AF1
     - TIM1_CH3
   * - AF2
     - TIM16_CH1N
   * - AF4
     - USART2_TX
   * - AF5
     - LPTIM_ETR
   * - AF6
     - I2C_SCL
   * - AF7
     - EVENTOUT


PA10 – Alternate Function Mapping
---------------------------------

.. list-table::
   :header-rows: 1
   :widths: 15 85

   * - AF
     - Function
   * - AF1
     - USART1_RX
   * - AF2
     - TIM1_CH3
   * - AF4
     - USART2_RX
   * - AF6
     - I2C_SDA
   * - AF7
     - EVENTOUT
   * - AF9
     - USART1_TX
   * - AF10
     - SPI1_NSS
   * - AF12
     - I2C_SCL





