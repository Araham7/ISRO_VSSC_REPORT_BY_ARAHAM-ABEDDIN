# 🌞 Dual Axis Solar Tracker with GPS-based Sun Positioning using PIC18F Microcontroller

---

## 🏫 Project Details
**Student Name:** Araham Abeddin  
**Department:** Electronics and Communication Engineering  
**Institution:** Maulana Abul Kalam Azad University of Technology, West Bengal  
**Academic Year:** 2025  
**Project Guide:** ___________________

---

## 🧾 Abstract
This project presents a **dual-axis solar tracking system** using the **PIC18F microcontroller** and a **GPS module**. The system calculates the **real-time position of the sun** (elevation and azimuth) using trigonometric formulas derived from GPS data (latitude, longitude, and UTC time). Two **stepper motors** control the solar panel’s tilt and rotation to maintain optimal sunlight exposure throughout the day. The design ensures improved solar efficiency, energy harvesting, and automation without the need for external light sensors.

---

## 🪐 1. Introduction
Solar tracking is a method to orient solar panels toward the sun to maximize energy generation. Traditional fixed solar panels face energy loss due to varying sunlight angles.  
This project aims to develop an **automated, precise, and reliable solar tracking system** based on **GPS and astronomical calculations**, eliminating the dependency on light-dependent resistors (LDRs).

---

## 🎯 2. Objectives
- To design and implement a **dual-axis solar tracker** using a PIC18F microcontroller.  
- To extract **latitude, longitude, and time** from GPS data.  
- To calculate **solar elevation and azimuth** using trigonometric functions.  
- To control **two stepper motors** for accurate sun alignment.  
- To optimize the **power capture** of solar panels dynamically.

---

## ⚙️ 3. System Components

| Component | Description |
|------------|-------------|
| **PIC18F2523 Microcontroller** | Core controller for processing and motor control |
| **GPS Module (e.g., NEO-6M)** | Provides location and time data (NMEA strings) |
| **Stepper Motors** | Adjust solar panel tilt and rotation |
| **Limit Switches** | Detect and calibrate home position |
| **Power Supply Unit** | Provides stable DC voltage to all modules |

---

## 🧭 4. System Overview
The GPS module sends NMEA data to the microcontroller. The program parses this data to obtain date, time, latitude, and longitude. Using solar position equations, it computes the **solar declination, hour angle, elevation, and azimuth**. The calculated values are converted into stepper motor steps, which rotate the solar panel along **two axes** — elevation and azimuth.

---

## 🧩 5. Block Diagram
![Block Diagram](./block_diagram.png)

---

## 🔄 6. Flowchart of the Code
![Flowchart](./flowchart.jpeg)


## 🧮 7. Algorithm / Pseudocode
```text
BEGIN
  Initialize ports, UART, timers
  WHILE (1)
    READ GPS NMEA data
    PARSE latitude, longitude, UTC time
    CALCULATE day_of_year()
    COMPUTE solar_declination(), solar_hour_angle()
    FIND sun_position (elevation, azimuth)
    CONVERT angles → motor steps
    MOVE elevation and azimuth motors
    CHECK limit switches
  END WHILE
END
```
