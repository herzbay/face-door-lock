# Face Recognition Smart Door Lock (ESP32-CAM)

An ESP32-CAM-based smart door lock system that uses face recognition for access control. The system provides a web-based interface for camera streaming, face detection, user enrollment, and door lock management.

## Overview

This project is an IoT-based smart door lock system developed using the ESP32-CAM AI Thinker module. It uses facial recognition to identify registered users and control an electronic door lock through a relay module.

The ESP32-CAM creates its own Wi-Fi access point, allowing users to access the system through a web browser without requiring an external Wi-Fi network or internet connection.

## Features

- **Face Detection** — Detects human faces through the ESP32-CAM camera.
- **Face Recognition** — Identifies registered users to authorize door access.
- **Face Enrollment** — Registers new users with their names and facial data.
- **Web-Based Interface** — Provides browser-based access to camera streaming and access control features.
- **Real-Time Camera Streaming** — Displays the camera feed through a web interface.
- **Access Control** — Controls the electronic door lock using a relay module.
- **Automatic Door Locking** — Automatically locks the door again after the configured unlock interval.
- **User Management** — Supports deleting individual registered faces or removing all enrolled users.
- **Status Indicators** — Uses red and green LEDs and a buzzer to provide system feedback.

## Hardware Components

| Component | Description |
|---|---|
| ESP32-CAM AI Thinker | Main microcontroller and camera module |
| OV2640 Camera | Captures images for face detection and recognition |
| Relay Module | Controls the electronic door lock |
| Electronic Door Lock | Physical locking mechanism |
| Buzzer | Provides audio feedback |
| Red LED | Indicates access or system status |
| Green LED | Indicates successful access |
| USB-to-TTL Converter | Used for programming the ESP32-CAM |
| Power Supply | Provides power to the system |

## Software & Technology

- **Arduino IDE** — Development environment
- **C/C++** — Programming language
- **ESP32-CAM** — Embedded hardware platform
- **Wi-Fi Access Point** — Local wireless connection
- **WebSocket** — Communication between the ESP32-CAM and web interface
- **HTML, CSS, JavaScript** — Web interface technologies
- **ESP32 Camera / Face Recognition** — Camera processing and facial recognition

## How It Works

1. The ESP32-CAM initializes the camera and creates a Wi-Fi access point.
2. A user connects to the ESP32-CAM network using a Wi-Fi-enabled device.
3. The user opens the system interface through a web browser.
4. The camera captures images and detects faces in real time.
5. Users can enroll new faces and manage registered identities through the interface.
6. When a detected face matches a registered user, the system activates the relay to unlock the door.
7. After the configured unlock interval, the relay returns to its locked state.

## Access Control Interface

The web interface provides several controls for managing the system:

| Feature | Description |
|---|---|
| Stream Camera | Displays the live camera feed |
| Detect Faces | Enables face detection |
| Add User | Registers a new user |
| Access Control | Activates the access control process |
| Delete All | Removes all registered face data |

## System Configuration

| Configuration | Value |
|---|---|
| Camera Model | AI Thinker ESP32-CAM |
| Camera Sensor | OV2640 |
| Wi-Fi Mode | Access Point (AP) |
| HTTP Camera Stream Port | 81 |
| WebSocket Port | 82 |
| Serial Baud Rate | 115200 |
| Face Enrollment Samples | 5 |
| Maximum Registered Faces | 7 |
| Relay Unlock Interval | 5000 ms |
