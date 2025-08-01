## 🚗 Collision Avoidance System Using CAN Protocol

### 📌 Introduction

This project implements a **Collision Avoidance System** using the **CAN (Controller Area Network) protocol** on an **STM32 microcontroller**. It improves vehicle safety by allowing multiple ECUs (Electronic Control Units) to communicate and respond to potential collision threats using sensor data.

🚦 **Why CAN?**
CAN is widely used in the automotive industry due to:

* 🛡️ High noise immunity & error detection
* 📶 Efficient, message-based multi-node communication
* ⚡ Real-time performance
* 🧩 Simple wiring and scalability

---

### 🧠 System Overview

Each node performs the following:

* 📡 Monitors surroundings using **ultrasonic** and **IR sensors**
* 🧠 Processes local sensor data (e.g., distance, proximity)
* 📤 Sends CAN messages to other nodes on risk detection
* 📥 Receives data from peers and takes preventive action
* 🚨 Triggers alerts (buzzer/LED) on detecting a collision risk

---

### 🛠️ Hardware Components

| Component             | Description                             |
| --------------------- | --------------------------------------- |
| STM32 Microcontroller | STM32F103 / STM32F407 or compatible     |
| CAN Transceiver       | MCP2551                                 |
| Ultrasonic Sensor     | HC-SR04 (distance measurement)          |
| IR Sensor             | LM393 (Proximity)                       |
| Alert Devices         | Buzzer, LED, OLED/LCD (optional)        |
| Power Supply          | 9V Battery or 5V Regulated Source      |
| Wiring                | CAN\_H, CAN\_L, GND, Sensor Connections |

---

### ⚙️ Technical Features

* 🧮 STM32 programmed via HAL / STM32CubeMX
* 📡 Ultrasonic via GPIO & timer capture
* 🔦 IR sensor via analog/digital read
* 🛠 CAN protocol with ID filtering, TX/RX interrupts
* 📤 Broadcast of collision detection alerts
* 🚨 Audible/visual indication at any node receiving warning

---

### 💡 Applications

* 🚘 Automotive collision detection
* 🤖 Robot proximity coordination
* 🏭 Industrial safety in AGVs
* 🎓 Educational projects in embedded CAN systems

---

### 🧩 Future Improvements

* Add vehicle speed estimation
* Integrate automated braking logic
* Use higher-layer CAN protocols (e.g., CANopen)
* Insert rain/fog sensor to activate fog lights
* Real-time logging via SD card or telemetry
