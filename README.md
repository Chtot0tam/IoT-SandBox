# 🧪 IoT Smart Home API Testing Project

## 📌 Overview

This project demonstrates **manual API testing skills** for a simulated IoT Smart Home system.

It covers testing of a REST API that manages smart home devices such as sockets, sensors, a smart light, and a gateway device.

The project focuses on:
- Functional API testing
- Business logic validation
- Negative testing scenarios
- Data consistency checks

---

## 🏠 System Description

The simulated IoT system includes the following devices:

- 🔌 **Smart Sockets** (4 devices)
- 💧 **Water Leak Sensors** (2 devices)
- 🌡 **Temperature Sensor** (1 device)
- 💡 **Smart Light** (1 device)
- 🌐 **Gateway Device** (1 device)

Each device has its own state, attributes, and behavior.

---

## 📡 API Endpoints

### 📦 Devices
- 💧 Sensors
- 💡 Light
- 🌐 Gateway


---

## 🧪 Test Coverage

### ✔ Functional Testing
- API response validation (status codes)
- JSON schema validation
- Required fields verification
- Data type validation

### ✔ Business Logic Testing
- Water leak detection → warning validation
- Battery level < 20 → LOW_BATTERY alert
- Smart socket must include OnOff cluster
- Offline devices behavior validation
- Gateway consistency with connected devices

### ✔ Negative Testing
- Offline device handling
- Missing telemetry validation
- Incorrect state handling
- Data inconsistency checks

---

## 📋 Test Cases Summary

Total test cases: **22**

### 📦 Devices
- Response structure validation
- Device type verification
- Offline device checks
- Device count validation

### 🔌 Device Details
- Endpoint validation
- Power meter validation
- Device state verification

### 💧 Water Sensors
- Leak detection logic
- Battery warning logic
- False positive prevention

### 🌡 Temperature Sensor
- Range validation (-40 to +100)
- Schema validation

### 💡 Smart Light
- Status validation (On/Off)
- Brightness range validation (0–100)
- State consistency checks

### 🌐 Gateway
- IP format validation
- Firmware presence
- Connected devices consistency

---

## 🛠 Tools Used

- Postman
- JavaScript (Postman test scripts)
- Mock API (Mockoon / simulated backend)
- Manual API testing approach

---

## 📸 ScreenShots

<img width="199" height="254" alt="image" src="https://github.com/user-attachments/assets/f4f8d898-61f5-4bea-9439-dc3dd893fef8" />

<img width="792" height="311" alt="image" src="https://github.com/user-attachments/assets/b1e5af0a-f80a-4c95-914f-ddc0696efecf" />

<img width="1037" height="126" alt="image" src="https://github.com/user-attachments/assets/1164d79f-16ea-4381-9455-4b6f465e49e3" />






