# EV-Torque-Vectoring-Control

# Real-Time EV Torque Vectoring System

**Role:** Control Systems / Software | **Context:** Electric Vehicle Design Course - APS380 (Group Project)

## Project Overview
Designed and implemented an Electronic Differential System (EDS) for a prototype electric vehicle. The system integrates sensor fusion with a real-time control loop to optimize vehicle stability and traction during cornering and slip events.

## Tech Stack
* **Hardware:** Microcontroller (ESP32-WROOM-32), Brushless Motors for the Wheels and Servo for Steering, Wheel Encoders, IMU
* **Algorithms:** PI Control, Slip Ratio Calculation
* **Language:** Python

## System Architecture
```mermaid
graph TD
    A[Sensors] -->|Encoder Data| B(Slip Detection)
    A -->|IMU Data| C(Yaw Rate Estimation)
    B --> D{Control Logic}
    C --> D
    D -->|Error Signal| E[PI Controller]
    E -->|PWM Signal| F[Left Motor Inverter]
    E -->|PWM Signal| G[Right Motor Inverter]
