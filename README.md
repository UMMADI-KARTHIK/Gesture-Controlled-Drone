# 🖐️ Gesture-Controlled Drone using OpenCV and Arduino

This project implements a **Gesture-Controlled Drone** using a **webcam and OpenCV** to detect hand gestures. These gestures are interpreted by a Python program running on a laptop or Raspberry Pi, and corresponding flight commands are sent wirelessly to a drone controlled by Arduino.

---

## 🎯 Project Goal

Control a quadcopter's motion using real-time **hand gestures captured through a camera**, without physical buttons or sensors.

---

## 📌 Features

- Real-time hand tracking using **OpenCV**
- Detects basic hand gestures (e.g., open palm, fist, hand movement)
- Sends wireless control commands to drone via **Bluetooth/RF/Wi-Fi**
- Arduino-based flight controller receives commands and drives the motors
- Extensible for more advanced gesture sets and control modes

---

## 🛠️ Components Used

| Component           | Quantity | Description                           |
|--------------------|----------|---------------------------------------|
| Laptop or Raspberry Pi | 1      | Runs OpenCV + Python gesture software |
| Webcam              | 1        | For hand gesture input                |
| Arduino Uno/Nano    | 1        | Drone controller                      |
| RF / Bluetooth module | 1      | For wireless communication            |
| Quadcopter Frame    | 1        | With ESCs, motors, props              |
| LiPo Battery        | 1        | Power source for drone                |

---

## 🧠 How It Works

1. **OpenCV** captures live video and tracks your hand.
2. A Python script detects gestures (e.g., number of fingers, direction of movement).
3. Based on gesture, it sends a control command via **serial** or **Bluetooth/RF**.
4. Arduino on the drone receives the command and adjusts the motor speeds.
5. Drone moves accordingly.

---

## ✋ Gesture to Command Mapping

| Gesture            | Action            |
|--------------------|-------------------|
| Open palm (5 fingers) | Hover           |
| Fist (0 fingers)    | Stop              |
| Hand move up        | Move Up           |
| Hand move down      | Move Down         |
| Hand move left      | Turn Left         |
| Hand move right     | Turn Right        |
| Peace sign (2 fingers) | Move Forward  |

---

## 💻 Software Setup

### Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- NumPy
- pySerial (for serial communication with Arduino)
- MediaPipe (for hand detection) *(Optional but recommended)*

### Install dependencies

```bash
pip install opencv-python numpy pyserial mediapipe
# Gesture-Controlled-Drone
