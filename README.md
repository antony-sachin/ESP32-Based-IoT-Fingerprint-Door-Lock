ESP32-Based IoT Fingerprint Door Lock with Status Monitoring
Project Overview

This project implements a biometric access control system using an ESP32 microcontroller and an R307 fingerprint sensor, integrated with IoT-based remote monitoring.
It replaces traditional key-based locking mechanisms with fingerprint authentication and provides real-time access status locally via an OLED display and remotely via a mobile application.

The system is designed as a low-cost, scalable smart security solution suitable for homes, offices, and academic demonstrations.

Key Features

Fingerprint-based biometric authentication

ESP32 with built-in Wi-Fi for IoT connectivity

Real-time access notifications using Blynk

Automatic door relocking after a fixed interval

OLED display for system and access status

Relay-controlled 12V electronic solenoid lock

Hardware Components

ESP32 WROOM-32

R307 Fingerprint Sensor

5V Relay Module

12V Electronic Solenoid Door Lock

SH1106 128x64 OLED Display (I2C)

External 12V power supply and USB power

Breadboard and jumper wires

System Architecture

Data Flow:
Fingerprint Sensor → ESP32 → Relay & OLED → Solenoid Lock
→ Blynk Cloud → Mobile Application

The ESP32 validates fingerprint data, controls the locking mechanism through a relay, updates the OLED display, and sends access events to the cloud for remote monitoring.

Pin Configuration
Module	ESP32 Pin
Fingerprint TX	GPIO16 (RX2)
Fingerprint RX	GPIO17 (TX2)
OLED SDA	GPIO21
OLED SCL	GPIO22
Relay IN	GPIO23
Working Principle

ESP32 initializes Wi-Fi, fingerprint sensor, and OLED display

System waits for fingerprint input

If fingerprint matches:

Relay activates and unlocks the door

Access status displayed on OLED and Blynk

If fingerprint does not match:

Access denied message shown

Alert sent to Blynk

Door automatically locks after a predefined delay

Software and Tools

Arduino IDE

Embedded C/C++

Blynk IoT Platform

Adafruit Fingerprint Library

U8g2 OLED Graphics Library

Testing and Validation

Registered fingerprint unlocks the door successfully

Unregistered fingerprint is denied access

All access events are reflected on the Blynk mobile app in real time

Future Enhancements

Detailed mobile access logs and remote unlocking

Multi-factor authentication (RFID, face recognition)

Battery or solar-powered operation

Cloud-based data storage and analytics

Repository

GitHub Link:
https://github.com/antony-sachin/ESP32-Based-IoT-Fingerprint-Door-Lock

License

This project is developed for academic and learning purposes.
