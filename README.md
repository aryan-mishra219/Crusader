# 🤖 Crusader: Voice & Gesture Controlled Bot

> **Command the future with your voice and hands.**
> *A dual-mode robotic vehicle powered by Arduino.*

![Project Banner](https://via.placeholder.com/1000x300?text=Crusader+Voice+%26+Gesture+Bot)

## 📖 Overview

**Crusader** is a multi-functional robotic vehicle designed to demonstrate the power of human-machine interaction. Unlike standard RC cars, Crusader offers two advanced modes of operation:

1.  **Voice Control:** Recognizes spoken commands (e.g., "Forward", "Left", "Stop") to navigate.
2.  **Gesture Control:** Uses a wearable remote (Hand Gesture) to drive the bot by tilting your hand.

This project combines embedded systems, sensor integration, and motor control logic into one robust platform.

## ✨ Key Features

* **Dual Control Modes:** Seamless switching between Voice and Gesture commands.
* **Precision Steering:** Differential drive mechanism using high-torque gear motors.
* **Wireless Communication:** Reliable transmission for remote operation (Bluetooth/RF).
* **Rugged Design:** Built to handle basic terrain.

## ⚙️ Hardware Components

### Main Robot Unit
* **Microcontroller:** Arduino Uno R3
* **Motor Driver:** L298N / L293D H-Bridge Module
* **Motors:** 2x (or 4x) DC Gear Motors (BO Motors)
* **Chassis:** Acrylic/Metal 2WD or 4WD chassis
* **Power:** Li-ion Batteries (18650) or 9V/12V source
* **Communication:** HC-05 Bluetooth Module (for Voice App)

### Gesture Remote
* **Microcontroller:** Arduino Nano / Uno
* **Sensor:** MPU6050 Accelerometer & Gyroscope (for detecting hand tilt)
* **Communication:** RF Transmitter/Receiver (433MHz) or Bluetooth Master

## 🛠️ Software & Tech Stack

* **Language:** C++ (Embedded)
* **IDE:** Arduino IDE
* **Libraries used:**
    * `Wire.h` (for I2C communication)
    * `MPU6050.h` (for gesture data)
    * `SoftwareSerial.h` (for Bluetooth communication)

## 🔌 Circuit & Connections

### Motor Driver Logic
| Arduino Pin | L298N Pin | Function |
| :--- | :--- | :--- |
| D3 | IN1 | Left Motor Fwd |
| D4 | IN2 | Left Motor Rev |
| D5 | IN3 | Right Motor Fwd |
| D6 | IN4 | Right Motor Rev |

*(Note: Pin mapping may vary based on your specific code configuration defined in `crusader.ino`)*

## 🚀 How to Run

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/aryan-mishra219/Crusader.git](https://github.com/aryan-mishra219/Crusader.git)
    ```
2.  **Hardware Setup:** Assemble the chassis and wire the motors to the driver and Arduino as per the circuit diagram.
3.  **Upload Code:**
    * Open `robot_receiver.ino` in Arduino IDE and upload to the **Robot Arduino**.
    * Open `gesture_remote.ino` in Arduino IDE and upload to the **Remote Arduino**.
4.  **Connect:** Power on both units. Connect your smartphone to the HC-05 module (for voice mode).
5.  **Drive:** Say "Forward" or tilt your hand to watch Crusader move!

## 👤 Author

**Aryan Mishra**
* **GitHub:** [@aryan-mishra219](https://github.com/aryan-mishra219)
* **Institution:**Balvantray Mehta Vidya Bhawan

---
*Built with logic, wires, and a bit of magic.*
