# Remote Control Ping Pong Ball Throwing Machine

A DIY remote-controlled table tennis (ping pong) ball throwing machine built with ESP32.

![System Architecture](photos/System_Architecire.jpeg)

> Demo video: [YouTube Short](https://www.youtube.com/shorts/ksmupxvY3Tg)

---

## Features

- Remote control via ESP32
- Brushless motor (HI TECH 3508/3510) for high-speed ball launching
- Dual DC motors for ball feeding
- Servo motor for angle / direction control
- Emergency stop button for safety
- Clean power distribution (24V → 12V / 6V / 5V)

---

## Hardware Overview

### Main Components

| Component                    | Description                              |
|-----------------------------|------------------------------------------|
| ESP32 Breakout Board        | Main controller                          |
| HI TECH 3508/3510 Motor     | 3-phase brushless motor (launcher)       |
| Motor Driver (CAN)          | Controls the brushless motor             |
| Dual DC Motor Driver        | Controls two DC motors (ball feeder)     |
| Servo Motor                 | Controls throwing angle                  |
| 24V LiPo Battery            | Main power source                        |
| Emergency Stop Button       | Safety cut-off                           |
| Power Distribution Board    | XT60 distribution                        |
| Buck Converters             | 24V → 12V and 24V → 6V                   |

### Power System

- **24V** → Brushless motor + power distribution
- **12V** → Dual DC motor driver
- **6V**  → Servo motor
- **5V**  → ESP32 (via Micro USB)

---

## Wiring Summary

- Brushless motor → CAN H / CAN L + 24V
- DC Motor 1 & 2 → Dual motor driver board
- Servo → ESP32 GPIO (PWM)
- Emergency Stop → Between battery and power distribution board
- ESP32 powered by 5V Micro USB

> Full wiring diagram is available in the repository.

---

## Getting Started

### Prerequisites
- ESP32 development board
- Arduino IDE or PlatformIO
- Required libraries (to be added)

### Installation
```bash
git clone https://github.com/yourusername/ping-pong-ball-thrower.git
cd ping-pong-ball-thrower
