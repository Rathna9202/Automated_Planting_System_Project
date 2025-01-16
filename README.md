Automated Planting System 🌱

This project is an Automated Planting System that uses an STM32 microcontroller to efficiently manage soil moisture levels by controlling a water pump. It is designed to make plant care simple and hassle-free, ensuring optimal soil hydration while conserving water.

🛠 Features

Soil Moisture Monitoring:
A soil moisture sensor continuously measures the soil's moisture levels.

Smart Water Pump Control:
Based on the moisture levels, the water pump is automatically turned ON or OFF via a relay module.

Real-Time Data Processing:
The STM32 microcontroller processes sensor data using its built-in ADC (Analog-to-Digital Converter).

Energy Efficient:
The system minimizes power consumption by running the pump only when necessary.

Customizable Thresholds:
Users can set specific moisture thresholds to suit different types of plants or soil conditions.

⚙️ System Workflow

The soil moisture sensor outputs an analog signal proportional to the soil's moisture content.
The STM32 microcontroller reads the analog signal using its ADC.
The microcontroller processes the ADC values and compares them against a predefined threshold.
If the moisture level is below the threshold:
The microcontroller activates the relay module.
The relay powers the water pump, watering the soil.
Once the soil reaches the desired moisture level, the pump is turned off automatically.

🛒 Components Used

STM32 Microcontroller
(e.g., STM32F446RE)
Soil Moisture Sensor
Outputs analog voltage proportional to moisture.
Relay Module
Controls the water pump.
Water Pump
Used to irrigate the plants.
Power Supply
Suitable for the STM32, relay, and pump.
Miscellaneous
Connecting wires, resistors, and a breadboard (optional PCB).

Hardware Connection:

![con](https://github.com/user-attachments/assets/52c02b7b-4c1d-4ce8-bbb7-8cfca03ee723)

PIN CONFIGURATION:

ADC Input:
Pin: PA0 (ADC Channel 0)
Purpose: Reads the analog signal from the soil moisture sensor.
Mode: Analog Input (Default after reset).

LED Output (Water Pump Indicator):
Pin: PA5
Purpose: Drives an LED to indicate the water pump's ON/OFF state.
Mode: GPIO Output (Push-Pull).
Default State: Low (OFF).

🔧 How to Build the Project

Hardware Setup:
Connect the Soil Moisture Sensor to the STM32 ADC pin.
Connect the Relay Module to a GPIO pin of the STM32 to control the water pump.
Power the Water Pump through the relay module.
Ensure a common ground for the STM32, relay module, and power supply.

Software Setup:
Write Firmware:
Use STM32 HAL/LL libraries or bare-metal programming for efficient ADC and GPIO control.
Read the soil moisture sensor values using the ADC.
Compare the values with a predefined threshold to decide pump operation.
Use GPIO to activate/deactivate the relay.
Compile and Flash:
Use an IDE like Keil, STM32CubeIDE, or PlatformIO to write, compile, and flash the code to the STM32.

Moisture Level Using ADC:

LOW:

![adc1](https://github.com/user-attachments/assets/3dd85ca5-d33f-4989-aed1-2662836379da)

HIGH:

![adc2](https://github.com/user-attachments/assets/f2ba2261-8925-4161-9367-b6f1af0cafe7)


