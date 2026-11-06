# ESP32-CAM IoT Smart Security Camera

An IoT-based smart security camera system using **ESP32-CAM, PIR Motion Sensor, and Telegram Bot API** for motion detection, remote photo capture, and real-time security notifications.

<p align="center">
  <strong>Microcontroller Lab Project | CSE-3116</strong><br>
  Department of Computer Science & Engineering<br>
  Mymensingh Engineering College
</p>

---

## 📌 Project Overview

This project aims to develop a low-cost, IoT-based smart security camera using the ESP32-CAM module.

The system uses a PIR (Passive Infrared) motion sensor to detect movement within a monitored area. When motion is detected, the ESP32-CAM captures a photograph and sends it directly to the user's smartphone through a Telegram bot.

Users can also remotely request photographs, control the flash LED, and enable or disable motion detection using Telegram commands.

The goal is to develop an affordable, portable, and remotely accessible security solution.

## ✨ Planned Features

- **Motion Detection:** Detect movement using an HC-SR501 PIR sensor.
- **Automatic Photo Capture:** Capture images when motion is detected.
- **Telegram Notifications:** Send captured photographs to the user's Telegram account.
- **Remote Photo Capture:** Request a photograph using Telegram commands.
- **Flash LED Control:** Remotely turn the camera light ON or OFF.
- **Motion Control:** Enable or disable motion detection remotely.
- **User Authorization:** Restrict system access to authorized Telegram chat IDs.
- **Wi-Fi Connectivity:** Communicate with the Telegram Bot API over the internet.

## 🛠️ Hardware Components

| Component | Purpose |
|---|---|
| ESP32-CAM (AI-Thinker) | Main controller and camera |
| OV2640 Camera | Image capture |
| HC-SR501 PIR Sensor | Motion detection |
| White LED / Flash LED | Night-time illumination |
| FTDI / USB-to-TTL Programmer | Firmware uploading |
| Resistors (220Ω, 10kΩ) | Circuit interfacing |
| 5V 2A Power Supply | Power source |
| Breadboard / Veroboard | Circuit assembly |
| Jumper Wires | Connections |
| Push Button | Reset |
| Enclosure Box | Hardware protection |

## 💻 Software & Technologies

- Arduino IDE
- C/C++ (Arduino Framework)
- ESP32 Board Support Package
- Telegram Bot API
- Wi-Fi Communication
- HTTPS

### Libraries

- `esp_camera.h`
- `WiFi.h`
- `WiFiClientSecure.h`
- `UniversalTelegramBot`
- `ArduinoJson`

## ⚙️ Working Principle

1. The ESP32-CAM initializes the camera and connects to the configured Wi-Fi network.
2. The PIR sensor continuously monitors the surrounding area.
3. When motion is detected, the ESP32-CAM receives the sensor trigger.
4. The camera captures a JPEG photograph.
5. The captured image is sent to the authorized user's Telegram account.
6. The user can interact with the Telegram bot to request photographs, control the flash LED, and manage motion detection.
7. Unauthorized users are prevented from controlling the system.

## 📱 Planned Telegram Commands

| Command | Function |
|---|---|
| `/start` | Start bot interaction |
| `/photo` | Capture and send a photograph |
| `/flash` | Control flash LED |
| `/enable` | Enable motion detection |
| `/disable` | Disable motion detection |

*Command names and behavior will be finalized during firmware development.*

## 🏗️ System Architecture

```text
       PIR Motion Sensor
               |
               v
          ESP32-CAM <------ OV2640 Camera
               |
          Wi-Fi Router
               |
            Internet
               |
       Telegram Bot API
               |
               v
       User's Smartphone
```

The ESP32-CAM also controls the flash LED/light based on user commands and system requirements.

## 👨‍💻 Development Team

| Name | Roll | Responsibility |
|---|---|---|
| Mohammad Rifat | 220336 | Firmware, camera configuration and Telegram integration |
| Jahidul Islam | 220353 | Hardware design, PIR/LED interfacing, soldering and enclosure |
| Sadia Islam | 220352 | Wi-Fi connectivity, authorization, testing and documentation |

**Institution:** Mymensingh Engineering College  
**Department:** Computer Science & Engineering  
**Course:** Microcontroller Lab (CSE-3116)

## 🚧 Development Progress

This project is currently under development. Progress and implementation details will be updated regularly.

- [ ] Literature study and component research
- [ ] ESP32-CAM camera testing
- [ ] PIR sensor testing
- [ ] Wi-Fi connectivity setup
- [ ] Telegram bot creation and integration
- [ ] Remote photo capture implementation
- [ ] Automatic motion-triggered photo capture
- [ ] Flash LED control
- [ ] Telegram user authorization
- [ ] Hardware circuit assembly
- [ ] System integration and debugging
- [ ] Performance testing
- [ ] Final prototype and documentation

## 🔮 Future Improvements

- Live video streaming
- SD card image storage
- Battery backup and solar power
- Face recognition
- Buzzer or GSM-based backup alerts

## 📂 Repository Structure

```text
esp32cam-iot-smart-security-camera/
│
├── README.md
├── src/
│   └── main.ino
│
├── circuit/
│   ├── circuit-diagram.png
│   └── wiring-diagram.png
│
├── images/
│   └── project-setup.jpg
│
├── docs/
│   ├── project-proposal.pdf
│   └── development-log.md
│
└── LICENSE
```

*Files and folders will be added as development progresses.*

## 🔐 Security Note

- Never upload your Telegram Bot Token or Wi-Fi password to GitHub.
- Store sensitive credentials separately from the source code.
- Restrict bot access using authorized Telegram chat IDs.

## 📖 Project Documentation

Development notes, circuit diagrams, hardware configurations, implementation details, and testing results will be documented in this repository as the project progresses.

---

**Project Status:** Under Development 🚧

**Developed with ❤️ by the CSE Team, Mymensingh Engineering College.**
