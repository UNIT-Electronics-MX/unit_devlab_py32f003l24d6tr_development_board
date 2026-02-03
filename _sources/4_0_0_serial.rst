Serial Communication (UART)
============================


The DevLab PY32F003L24D6TR Development Board offers robust serial communication capabilities, making it ideal for applications requiring reliable data exchange. The board features multiple serial interfaces, including USART, which supports various communication protocols. With a maximum baud rate of up to 115200 bps, the USART interface ensures efficient data transmission for a wide range of applications.

.. image:: _static/uart.png
   :alt: Serial Interface Diagram
   :align: center


Example Usage
-----------------

Here is a simple example of how to set up and use the USART interface on the DevLab PY32F003L24D6TR Development Board using the Arduino IDE:

.. code-block:: cpp

    void setup() {
    // Initialize serial communication
    // PA0 = TX, PA1 = RX automatically configured
    Serial.begin(115200);
    
    // Startup message
    Serial.println("=== PY32F003 Serial Echo ===");
    Serial.println("Type something and press Enter");
    }

    void loop() {
    // If there is data available in the serial buffer
    if (Serial.available()) {
        // Read and echo the character
        char c = Serial.read();
        Serial.write(c);
    }
    }


Overview of Serial Communication
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The DevLab PY32F003L24D6TR Development Board offers versatile serial communication through its USART interfaces, supporting UART protocols for efficient data transmission. Key features include:

- Configurable baud rates up to 115200 bps.
- Standard pin assignments, such as PA0 for TX and PA1 for RX on USART2.
- Multiple USART peripherals for flexible connectivity.

These capabilities make the board suitable for a broad range of applications requiring reliable serial data exchange.


