# BigGreenData 🌡️ Sensor Data Receiver （Under Development）

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

## :eyes: Structure
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
2. **Start the MQTT Broker**:
   ```bash
   mosquitto -v
   ```

### Building the Application

1. **Clone the repository**:
   ```bash
   git clone https://github.com/0YJ/sensor-data-receiver.git
   cd sensor-data-receiver
   ```

2. **Build the application using Maven**:
   ```bash
   mvn clean install
   ```

3. **Run the application**:
   ```bash
   java -jar target/sensor-data-receiver-1.0-SNAPSHOT.jar
   ```

## 🔧 Configuration

Modify the `application.properties` file to adjust the MQTT server settings:

```properties
mqtt.url=tcp://localhost:1883
mqtt.topic=sensorTopic
```

## 🚀 Usage

Once the application is running and the MQTT broker is configured, ensure your Raspberry Pi is publishing data to the `sensorTopic` MQTT topic. The application will receive messages and output them to the console.

## 🤝 Contributing

We welcome contributions! Please consider the following steps if you're interested in contributing:

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/CoolFeature`).
3. Commit your changes (`git commit -m 'add some cool commit'`).
4. Push to the branch (`git push origin feature/CoolFeature`).
5. Open a Pull Request.

## 📬 Have Questions?

For questions or support, please open a [ticket](https://github.com/0YJ/BigGreenData/issues/). We're here to help!
