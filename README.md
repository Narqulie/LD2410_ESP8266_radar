# ESP-Home motion detection with an LD2410

## Overview

The ESPHome LD2410 Motion Detection project provides a comprehensive solution for those looking to integrate advanced motion detection capabilities into their smart homes or any other relevant applications. By utilizing the LD2410 sensor in tandem with the versatile NodeMCU platform, this project offers an innovative and efficient approach to track and differentiate between varying types of motion within a specified area.

### What is LD2410?
The LD2410 is a sophisticated motion sensor designed to detect and differentiate movements within its field of view. Unlike many other traditional motion sensors which only detect the presence or absence of motion, LD2410 goes a step further. It can discern between a moving target and a still one, providing a more granular perspective of the activity in the monitored area.

### Why NodeMCU?
NodeMCU, based on the ESP8266, is a popular and accessible IoT platform. It is favored for its open-source nature, Wi-Fi capabilities, and expansive community support. By integrating the LD2410 sensor with NodeMCU, we harness the power and flexibility of the platform to relay motion data seamlessly and in real-time. Whether you're looking to set up alerts, activate specific devices, or simply log data, NodeMCU's capabilities, combined with the ESPHome framework, can cater to an array of applications.

### Integration with Home Assistant
One of the project's highlights is its native support for Home Assistant, a leading platform for home automation. Users of Home Assistant can effortlessly incorporate the functionalities offered by this project, enabling them to automate tasks, set up alerts, or monitor their spaces based on the motion data provided by the LD2410.

### Potential Use-Cases
Security: Enhance your home security by setting up alerts or activating cameras/recording devices when motion is detected.
Energy Saving: Automatically control lighting, heating, or cooling devices based on the presence or absence of individuals in a room.
Data Logging: For those interested in analytics, the motion data can be logged over time to study patterns, peak times of activity, or any unusual occurrences.

## Wiring and setup

### Wiring Diagram for NodeMCU and LD2410:
#### Components:
NodeMCU (ESP8266 based)
LD2410 Motion Sensor
#### Connections:
##### Power:
Connect the VCC pin of the LD2410 to the 3.3V pin on the NodeMCU.
Connect the GND pin of the LD2410 to any GND pin on the NodeMCU.
##### UART Communication:
Connect the TX pin of the LD2410 to the RX (GPIO3) pin on the NodeMCU.
Connect the RX pin of the LD2410 to the TX (GPIO1) pin on the NodeMCU.

##### Notes:
Ensure that you're powering the LD2410 with the appropriate voltage. If the LD2410 requires 5V, you might need an external power source or a voltage regulator if your NodeMCU only provides 3.3V.
Avoid long wires to minimize potential interference.
Ensure all connections are secure and no pins are shorting.
Always power off the circuit when making changes to avoid potential damage.
