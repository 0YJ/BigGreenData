# BigGreenData 🌡️ Sensor Data Receiver

## 📜 Overview

The Sensor Data Receiver is a robust Java Spring Boot application designed to collect and process temperature and humidity data sent from Raspberry Pi devices. Utilizing MQTT for efficient and reliable data transmission, this platform is perfect for IoT enthusiasts and professionals looking to integrate sensor data into large-scale data processing workflows.

## ✨ Features

- **Real-time Data Processing**: Receive and process temperature and humidity data in real-time.
- **MQTT Integration**: Utilizes MQTT protocol for lightweight and reliable data transmission.
- **Scalable Architecture**: Designed to scale seamlessly with your IoT needs.
- **Data Visualization Interface**: Ready to integrate with front-end frameworks for data visualization (front-end not included).

## 📋 Requirements

- Java JDK 11 or newer
- Maven 3.6 or newer
- An MQTT Broker (e.g., Mosquitto) running locally or remotely
- Raspberry Pi with temperature and humidity sensors configured to send data

```bash
sensor-data-receiver/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── sensordata/
│   │   │               ├── SensorDataApplication.java
│   │   │               └── config/
│   │   │                   └── MqttConfig.java
│   │   ├── resources/
│   │   │   └── application.properties
│   │
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── sensordata/
│                       └── SensorDataApplicationTests.java
│
├── pom.xml
└── .gitignore
```

## ⚙️ Installation

### Setting Up the MQTT Broker

1. **Install Mosquitto Broker**:
   ```bash
   sudo apt-get install mosquitto
   sudo apt-get install mosquitto-clients
   ```
2. **Start the MQTT Broker:**:
   ```bash
    mosquitto -v
   ```
