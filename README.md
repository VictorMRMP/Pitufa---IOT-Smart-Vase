# Pitufa - Smart Plant Pot for Optimized Plant Growth

Pitufa is a smart plant pot designed to optimize the growth of specific plants by monitoring environmental conditions and automatically adjusting lighting and watering levels. Data is sent to an Arduino IoT Cloud Dashboard for remote monitoring.

## Project Overview

This project leverages an ESP32 microcontroller with various sensors and actuators to create a smart, self-sustaining environment for plant growth. The system monitors temperature, humidity, soil moisture, and light intensity, and controls a water pump and LED panel according to plant-specific parameters.

## Features

- **Real-time Monitoring**: Monitors temperature, humidity, soil moisture, and light intensity and displays data on an Arduino IoT Cloud Dashboard.
- **Automated Control**: Adjusts light and water levels based on predefined plant types, ensuring optimal growth conditions.
- **Customizable for Plant Types**: Select from preset parameters for different plants, including Crassula argentea, Chlorophytum comosum, and Peperomia caperata.
  
## Hardware Components

- **ESP32** - Main microcontroller
- **DHT11** - Temperature and Humidity Sensor
- **Capacitive Moisture Sensor** - For soil moisture detection
- **GY-30 (BH1750)** - Light intensity sensor
- **LED Panel** - Simulates sunlight for plant growth
- **5V Water Pump** - For automated watering
- **5V Relay Module (2 channels)** - Controls water pump and LED panel
- **3D Printed Parts** - Custom-designed for housing the components
- **PCB** - Custom PCB for connecting all components efficiently

## Software Setup

1. Clone this repository and open the code in the Arduino IDE.
2. Install the following libraries, if not already installed:
   - `DHT.h` for the DHT11 sensor
   - `BH1750.h` for the GY-30 light sensor
3. Set up an Arduino IoT Cloud account and configure the Thing properties to match the code.

## Code Structure

- **system_init()**: Initializes sensors, sets pin modes for the pump and LED.
- **getData()**: Reads sensor values for temperature, humidity, soil moisture, and light.
- **routine()**: Controls watering and lighting based on plant-specific thresholds.
- **typeSelector()**: Sets optimal light and moisture thresholds for selected plant types.

## How to Use

1. Power on the ESP32 and connect to the Arduino IoT Cloud Dashboard.
2. Select the plant type from the dashboard:
   - Type 1: *Crassula argentea* (low water and medium light requirements)
   - Type 2: *Chlorophytum comosum* (medium water and high light requirements)
   - Type 3: *Peperomia caperata* (high water and medium light requirements)
3. Monitor real-time data on the dashboard. The system will automatically adjust lighting and watering as needed.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

Developed by Victor Marcelo
