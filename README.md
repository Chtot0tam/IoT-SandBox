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

## 📊 Example Test Script (Postman)

```javascript
const json = pm.response.json();

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Devices array exists", function () {
    pm.expect(json.devices).to.be.an("array");
});

pm.test("Check socket devices", function () {
    const sockets = json.devices.filter(d => d.type === "Socket");

});

pm.test("Leak detection logic", function () {
    const sensors = json.devices.filter(d => d.type === "WaterLeakSensor");

    sensors.forEach(sensor => {
        if (sensor.leak === true) {
            pm.expect(sensor.warnings).to.include("WATER_LEAK_DETECTED");
        }
    });
});
