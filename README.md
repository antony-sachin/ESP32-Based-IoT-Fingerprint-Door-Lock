🔐 ESP32-Based IoT Fingerprint Door Lock with Status Monitoring
📌 Project Overview

This project implements a biometric door locking system using an ESP32 microcontroller and an R307 fingerprint sensor, integrated with IoT-based remote monitoring via the Blynk platform.
It enhances physical security by replacing traditional keys with fingerprint authentication while providing real-time access status on both a local OLED display and a mobile application.

🎯 Key Features

Fingerprint-based biometric authentication

ESP32 Wi-Fi enabled IoT connectivity

Real-time access notifications via Blynk mobile app

Automatic door locking after a fixed interval

OLED display for local system status

Relay-controlled 12V electronic solenoid lock

🧩 Hardware Components

ESP32 WROOM-32

R307 Fingerprint Sensor

5V Relay Module

12V Electronic Solenoid Door Lock

SH1106 128×64 OLED Display (I²C)

External 12V power supply + USB power

Jumper wires and breadboard

🛠️ System Architecture

Flow:
Fingerprint Sensor → ESP32 → Relay & OLED → Solenoid Lock
↳ Blynk Cloud → Mobile App

The ESP32 validates fingerprint data, controls door access through a relay, updates the OLED display, and sends access logs to the Blynk IoT platform.


🚀 How It Works

ESP32 initializes Wi-Fi, fingerprint sensor, and OLED

System waits for fingerprint input

If fingerprint matches:

Door unlocks via relay

“Access Granted” shown on OLED & Blynk

If fingerprint fails:

Access denied

Alert sent to Blynk

Door automatically locks after timeout

🧪 Testing

Registered fingerprint → Door unlocks successfully

Unregistered fingerprint → Access denied

All events logged in real time on Blynk app

📈 Future Enhancements

Mobile access logs & remote unlock feature

Multi-factor authentication (RFID / Face ID)

Battery or solar-powered operation

Cloud-based analytics for entry data

📂 Repository

🔗 GitHub:
https://github.com/antony-sachin/ESP32-Based-IoT-Fingerprint-Door-Lock

📜 License

This project is intended for academic and learning purposes.
