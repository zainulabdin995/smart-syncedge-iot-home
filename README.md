# Smart SyncEdge IoT Home Automation Platform

## Overview
The Smart SyncEdge Platform is an end-to-end Internet of Things (IoT) smart home automation system. Designed to bridge the gap between physical appliances and cloud computing, this project utilizes an ESP32 microcontroller to enable seamless control of high-voltage home appliances via web dashboards, mobile applications, and voice assistants like Google Home and Amazon Alexa.


## Tech Stack & Hardware
* **Microcontroller:** ESP32 (NodeMCU)
* **Programming Language:** C++ (Arduino IDE)
* **Cloud Platform:** Arduino IoT Cloud
* **Voice Integration:** Google Assistant, Amazon Alexa APIs
* **Sensors & Actuators:** DHT11 (Temperature & Humidity), 4-Channel 5V Relay Module, Physical Push Buttons

## Key Features
* **Multi-Modal Control:** Appliances can be operated via the Arduino Cloud dashboard, voice commands, or traditional physical switches.
* **State Synchronization:** If a physical switch is toggled offline, the new state is instantly synced to the cloud dashboard once the internet connection is restored, preventing state mismatch.
* **Real-Time Environmental Monitoring:** Continuously tracks room temperature and humidity using the DHT11 sensor and visualizes the data on the web dashboard.
* **Multi-User Access:** Secured cloud architecture allows up to 6 different authorized users to control the home environment simultaneously from their own devices.


## Setup & Installation
1. **Hardware Assembly:** Connect the 4-channel relay to the ESP32 GPIO pins (23, 19, 18, 5) and the DHT11 sensor to pin 4, as outlined in the `schematics/` directory.
2. **Cloud Configuration:** Create an Arduino IoT Cloud account, set up a new "Thing," and map the `CloudSwitch` and `CloudTemperatureSensor` variables.
3. **Software Flashing:** * Clone this repository.
    * Open `src/smart_home.ino` in the Arduino IDE.
    * Update the `SSID`, `PASS`, `DEVICE_LOGIN_NAME`, and `DEVICE_KEY` macros with your specific network and cloud credentials.
    * Flash the code to your ESP32 board.
4. **Voice Setup:** Link your Arduino IoT Cloud account to the Google Home or Alexa app to enable voice commands.
