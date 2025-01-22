# Distance Measurement Using HCSR04 and LCD 2004 I2C with NUCLEO-F411RE

This project demonstrates how to measure distance using the HCSR04 ultrasonic sensor and display it on an LCD 2004 using the I2C protocol. The project is implemented on the **NUCLEO-F411RE** microcontroller.

---

## 💜 Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Hardware Components](#hardware-components)
- [Circuit Diagram](#circuit-diagram)
- [Software Description](#software-description)
- [Getting Started](#getting-started)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 🖍 Introduction

The goal of this project is to measure the distance to an object using the HCSR04 ultrasonic sensor and display the result on an LCD 2004 screen. The system uses the I2C interface for LCD communication and GPIO for controlling the HCSR04 sensor.

---

## 🌟 Features

- **Distance Measurement**: Measures distances accurately using the HCSR04 ultrasonic sensor.
- **LCD Display**: Displays the measured distance on an LCD 2004 screen via I2C.
- **Real-Time Updates**: Continuously updates the distance measurement in real time.

---

## 💪 Hardware Components

1. **NUCLEO-F411RE** (STM32 microcontroller board)
2. **HCSR04 Ultrasonic Sensor**
3. **LCD 2004** with I2C backpack
4. **Jumper Wires**

---

## 🔍 Circuit Diagram

### Connections:

1. **HCSR04**:
   - `VCC`: 5V (NUCLEO)
   - `GND`: GND (NUCLEO)
   - `TRIG`: Connect to a GPIO pin (e.g., `PA9`).
   - `ECHO`: Connect to another GPIO pin (e.g., `PA8`).

2. **LCD 2004 with I2C Backpack**:
   - `SDA`: Connect to `PB7` (I2C1 SDA on NUCLEO-F411RE).
   - `SCL`: Connect to `PB6` (I2C1 SCL on NUCLEO-F411RE).
   - `VCC`: 5V (NUCLEO)
   - `GND`: GND (NUCLEO)

---

## 💻 Software Description

The project is developed using **STM32CubeIDE** with HAL libraries.

### Key Functionalities:

1. **HCSR04 Sensor**:
   - Sends ultrasonic pulses using the `TRIG` pin.
   - Measures the duration of the echo signal to calculate distance.

2. **LCD 2004 Display**:
   - Configured to communicate over the I2C bus.
   - Displays the measured distance in centimeters.

3. **Main Loop**:
   - Continuously triggers the HCSR04 sensor to measure distance.
   - Updates the LCD display in real time with the calculated distance.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/job-space/NUCLEO-LCD-HCSR04.git
cd NUCLEO-LCD-HCSR04
```

### 2. Configure STM32CubeIDE Project

1. Open STM32CubeIDE and import the project.
2. Enable the following peripherals in **CubeMX**:
   - GPIO for `TRIG` and `ECHO` pins.
   - I2C1 for LCD communication.
3. Generate code and add the HCSR04 driver and LCD I2C driver files.

### 3. Program the Microcontroller

1. Connect your NUCLEO-F411RE board to the computer using a micro-USB cable.
2. Build and flash the project onto the board.

---

## 🔐 Commands and Functionality

1. **Distance Measurement**: The HCSR04 sensor measures the distance to an object in real time.
2. **LCD Display**: The measured distance is displayed in centimeters on the LCD 2004.

---

## Developers

[y.kovalchuk](https://github.com/job-space)

---

## License

This project is distributed under the MIT License.

