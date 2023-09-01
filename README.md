# ESP-Home motion detection with an LD2410

![ESP-Home motion detection with an LD2410](/images/cover.jpeg)

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

### Code Setup:

![ESP-Home yaml](/images/code.png)

##### The YAML code for this project is available in the `esphome-web-df88a5.yaml` file.

This configuration provides the essential setup for integrating an LD2410 motion sensor with an ESP8266-based NodeMCU board.

### Basic configuration: 

The main takeaways from the code are as follows:
The LD2410 is connected to the NodeMCU via UART. The TX and RX pins are connected to the D7 and D8 pins on the NodeMCU respectively. The Baud-rate is set to 256,000. This is very specific for the sensor.

### Sensor configuration:

The max move distance is set to 1.5 meters, and the max still distance is set to 0.75 meters. These values are used to differentiate between a moving target and a still one. the Gate Threshold-values are set for three gates, 0-2. These need to be set for both the move and still states. These values will need to be adjusted for your specific use-case. The values are in meters.
A filter of 10 seconds is used to prevent false negatives. This is the time the sensor needs to be still before it will report a still state.

---

When integrating this code into your device, ensure to keep all sensitive details, such as Wi-Fi credentials and encryption keys, private. Use the secrets mechanism (`!secret`) in ESPHome to manage this.

## 3D printed enclosure
![3D printed enclosure](/images/enclosure.png)

A 3D Printed enclosure to house the ESP8266 and the LD2410. Find a .3mf file in the "enclosure" folder.
The MCU in mounted on the bottom of the enclosure and the radar sensor is glued into the lid. A dab of superglue doesn't seem to hinder it's operation on the slightest, and the lid can be removed if needed and snaps on securely. The enclosure is designed to be mounted on a wall with a command strip or similar. 
There are holes for passthrough of the USB cable, as well as holes for other possible sensors to be wired outside the enclosure. 