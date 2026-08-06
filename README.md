# 🌱 IoT Based Smart Agriculture Monitoring System

An IoT-powered system that monitors soil, weather, and environmental conditions in real time and automates irrigation — helping farmers make data-driven decisions, save water, and improve crop yield.

> Project Report by **Kanishka S** & **Swathi R**
> B.E. Electronics and Communication Engineering
> Velammal Engineering College (Autonomous), Chennai — Anna University
> Even Semester 2024–25

---

## 📖 Overview

Traditional farming relies heavily on manual monitoring and guesswork for irrigation and crop care, which often leads to wasted water, poor resource management, and reduced yield.

This project builds a **Smart Agriculture Monitoring System** using IoT sensors that continuously measure environmental parameters (soil moisture, temperature, humidity) and transmit data to a cloud-based platform. Farmers can view real-time insights via a mobile/web dashboard and the system can automatically trigger irrigation, reducing manual labor and optimizing water usage.

## ✨ Features

- 📡 Real-time monitoring of soil moisture, temperature, and humidity
- 💧 Automated irrigation control via a relay-driven water pump
- 🖥️ On-device LCD display for live sensor readings
- ☁️ Cloud connectivity for remote monitoring via mobile/web app
- 📊 Data-driven insights to support farming decisions
- 🌍 Reduces water wastage and manual intervention

## 🧰 Hardware Components

| Component | Purpose |
|---|---|
| NodeMCU ESP8266 | Wi-Fi enabled microcontroller — the brains of the system |
| DHT11 Sensor | Measures ambient temperature and humidity |
| Capacitive Soil Moisture Sensor v1.0 | Measures soil moisture level |
| Relay Module | Switches the water pump on/off |
| Water Pump | Delivers irrigation water to the field |
| LCD Display | Shows live sensor readings on-site |

## 🔌 Circuit Diagram

The NodeMCU ESP8266 is the central controller, interfacing with the DHT11 (temperature/humidity), the capacitive soil moisture sensor, an LCD display for local readouts, and a relay module that drives the water pump for automated irrigation.

```
docs/images/circuit-diagram.png
```

*(Add your circuit diagram image to `docs/images/` and update the path above.)*

## ⚙️ How It Works

1. The **soil moisture sensor** and **DHT11** continuously collect environmental data.
2. The **NodeMCU ESP8266** reads sensor values and displays them on the **LCD**.
3. Sensor data is transmitted over Wi-Fi to a cloud platform (e.g., ThingSpeak/Blynk/Firebase).
4. If soil moisture drops below a set threshold, the NodeMCU triggers the **relay** to switch on the **water pump** — enabling automated irrigation.
5. Farmers can view live data and trends remotely through a mobile or web dashboard.

## 🚀 Applications

1. **Soil Monitoring** — Sensors measure soil moisture, pH levels, temperature, and nutrient content.
2. **Weather Monitoring** — IoT devices collect real-time weather data such as temperature, humidity, rainfall, and wind speed.
3. **Water Quality Monitoring** — IoT sensors measure the quality of water used for irrigation.
4. **Remote Monitoring and Control** — Farmers can monitor and control farming operations remotely via smartphones or computers.
5. **Crop Health Monitoring** — Drones or cameras with IoT connectivity capture images of crops to detect diseases, pests, or nutrient deficiencies.

## 🛠️ Getting Started

### Prerequisites
- [Arduino IDE](https://www.arduino.cc/en/software) with ESP8266 board support installed
- Required libraries: `DHT sensor library`, `LiquidCrystal_I2C` (or your LCD's library), `ESP8266WiFi`

### Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/smart-agriculture-monitoring.git
   ```
2. Open `src/smart_agriculture.ino` in the Arduino IDE.
3. Update your Wi-Fi credentials and cloud API keys in the config section of the sketch.
4. Wire up the hardware according to the circuit diagram in `docs/images/`.
5. Select **NodeMCU 1.0 (ESP-12E Module)** as the board, choose the correct COM port, and upload the sketch.

## 📈 Outcome

The prototype successfully enhances farming efficiency by integrating real-time monitoring and automation. It measures soil moisture, temperature, humidity, and other environmental parameters, transmitting data to a cloud-based platform for analysis. Farmers can access insights via a mobile or web application, enabling data-driven decision-making. The system also supports automated irrigation, optimizing water usage and reducing manual labor — improving resource management, increasing crop yield, and minimizing environmental impact.

## 📂 Repository Structure

```
smart-agriculture-monitoring/
├── src/
│   └── smart_agriculture.ino   # Main microcontroller sketch
├── docs/
│   └── images/                 # Circuit diagram & outcome photos
├── README.md
├── LICENSE
└── .gitignore
```

## 👩‍💻 Authors

- **Kanishka S** (113223041054)
- **Swathi R** (113223041155)

Department of Electronics and Communication Engineering
Velammal Engineering College (Autonomous), Chennai-66
Affiliated to Anna University, Chennai

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
