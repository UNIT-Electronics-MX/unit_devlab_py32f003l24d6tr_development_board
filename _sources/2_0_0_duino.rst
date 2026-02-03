Supported basic Arduino functions
==================================

Packages the basic functions of the Arduino IDE, allowing you to program the DevLab Development Board using the familiar Arduino environment. This includes digital and analog I/O operations, PWM control, serial communication, and more.


.. code-block:: bash 

    https://raw.githubusercontent.com/UNIT-Electronics-MX/unit_electronics_py32_arduino_package/main/package_unit_electronics_py32_index.json

Learn how to program the **DevLab: PY32F003L24D6TR** development board using
**Arduino IDE** and the **CH552 Multi-Protocol Programmer** in **CMSIS-DAP mode**.

- Rapid prototyping
- Embedded systems education
- Wearable device development


These resources are sufficient for a wide range of control, signal acquisition,
and communication applications.

Materials Required
------------------

To program the **DevLab: PY32F003L24D6TR** using Arduino IDE, you will need:

- USB Type-C cable
- JST 1.0 mm cable (4-pin)
- Arduino IDE installed on your computer
- DevLab: PY32F003L24D6TR board
- DevLab: CH552 Multi-Protocol Programmer

Required Installations
----------------------

This tutorial uses the **pyOCD Debugger**, therefore the following must be installed:

- Python (installed on your system)
- pyOCD (Python package)

CMSIS-DAP Mode
--------------

The programmer must operate in **CMSIS-DAP mode**.

The following repository contains all available firmware images for the
Multi-Protocol Programmer. For this tutorial, you only need:

::

   cmsis_dap.bin

Firmware – CMSIS-DAP
~~~~~~~~~~~~~~~~~~~~

.. warning::

   Before connecting the programmer, make sure the device is powered with **+5 V**.
   Use the onboard voltage selector switch to choose the correct supply level.

Flashing the Programmer
-----------------------

Use **WCHISPStudio** to flash the file ``cmsis_dap.bin`` to the
Multi-Protocol Programmer.

Wait until the update process is complete before using the programmer
in **CMSIS-DAP mode**.

Refer to the official tutorial for more details:

::

   WCHISPStudio Tutorial

Additional Boards Manager (Arduino IDE)
---------------------------------------

1. Open **Arduino IDE**
2. Go to **File > Preferences**
3. In **Additional Boards Manager URLs**, paste the following URL:

::

   https://raw.githubusercontent.com/UNIT-Electronics-MX/unit_electronics_py32_arduino_package/main/package_unit_electronics_py32_index.json

Board Manager
-------------

1. Open **Boards Manager**
2. Search for **"UNIT Electronics PY32"**
3. Install the package

.. image:: _static/board-manager.jpg
   :alt: DevLab PY32F003L24T6 Pinout Diagram
   :align: center
   :width: 50%


Selecting the Board
-------------------

In Arduino IDE, select:

::

   Tools > Board > UNIT DevLab: PY32F003


.. image:: _static/board-py32.jpeg
   :align: center
   :width: 90%

Programmer Selection
--------------------

Select the programmer:

::

   Tools > Programmer > pyOCD Debugger


.. image:: _static/pyocd-debugger.jpeg
   :alt: DevLab
   :align: center

Connections
-----------

With the Multi-Protocol Programmer operating in **CMSIS-DAP mode** and the
DevLab board already selected in **Arduino IDE**, follow the steps below.

Step-by-step connection
~~~~~~~~~~~~~~~~~~~~~~~

1. Connect the **CH552 Multi-Protocol Programmer** to your computer using a USB cable.
2. Using a **JST 1.0 mm (4-pin) cable**, connect the programmer to the
   **DevLab: PY32F003L24D6TR** board.
3. Verify that the SWD signals are correctly aligned between both devices.

Required pin alignment
~~~~~~~~~~~~~~~~~~~~~~

The following signals **must match exactly** between the programmer and the board:

- **VCC**   – Target power
- **GND**   – Ground reference
- **SWDIO** – SWD data line
- **SWCLK** – SWD clock line

Connection reference
~~~~~~~~~~~~~~~~~~~~

.. image:: _static/result.jpeg
   :alt: DevLab PY32F003L24D6TR connected to CH552 Multi-Protocol Programmer
   :align: center
   :width: 70%



Example Code (Blink)
--------------------

Compile and upload the following example to blink the onboard LED.

.. note::

   It is not necessary to select a COM port, since programming is performed
   via **CMSIS-DAP**.

.. code-block:: cpp

   void setup() {
     // Initialize digital pin LED_BUILTIN as an output
     pinMode(LED_BUILTIN, OUTPUT);
   }

   void loop() {
     digitalWrite(LED_BUILTIN, HIGH);  // LED ON
     delay(500);
     digitalWrite(LED_BUILTIN, LOW);   // LED OFF
     delay(500);
   }

Once the connections are completed and verified, the **DevLab: PY32F003L24D6TR**
is correctly connected to the **CH552 Multi-Protocol Programmer** and ready
to be programmed using **Arduino IDE** via **CMSIS-DAP**.

.. image:: _static/upload_firmware.png
   :alt: DevLab
   :align: center

Flashing Firmware operation 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  add html gift
.. raw:: html

   <div style="text-align: center;">
     <img src="_static/blink.gif" alt="Arduino IDE Uploading Firmware" />
   </div>

