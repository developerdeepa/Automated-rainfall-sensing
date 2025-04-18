

📄 README.md
markdown
Copy
Edit
# Automating Rainfall Sensing Car Wiper 🚗🌧️

## 🔍 Project Overview
This project aims to automate the operation of car wipers based on rainfall detection using a rain sensor. It eliminates the need for manual wiper control and enhances driving safety by automatically activating the wipers when rain is detected.

---

## 🧠 Key Features
- Automatic detection of rain using a rain sensor
- Controls a wiper motor via a relay module
- Low power consumption
- Simple and cost-effective design
- Can be extended to adjust wiper speed based on rain intensity

---

## 🛠️ Project Domain
**Embedded Systems / Automotive Electronics**

---

## ⚙️ Tools & Technologies Used
- Arduino UNO
- Rain Sensor (e.g., YL-83 / FC-37)
- Relay Module
- DC Motor
- Power Supply (Battery/Adapter)
- Arduino IDE
- Programming Language: C/C++
- (Optional) Python for simulation or Raspberry Pi version

---

## 🧾 Circuit Components
- Arduino UNO
- Rain Sensor
- Relay Module
- DC Motor (or Servo Motor)
- Jumper Wires
- Resistors
- Breadboard / PCB

---

## 🔌 Working Principle
1. Rain sensor detects water droplets.
2. The sensor sends an analog signal to the Arduino.
3. If rain intensity exceeds the threshold, the Arduino sends a HIGH signal to the relay module.
4. The relay turns on the motor (wiper starts moving).
5. When no rain is detected, the relay turns off the motor.

---

## 💻 Arduino Code (C++)
```cpp
const int rainSensorPin = A0;
const int relayPin = 7;
const int rainThreshold = 500;

void setup() {
  pinMode(relayPin, OUTPUT);
  digitalWrite(relayPin, LOW);
  Serial.begin(9600);
}

void loop() {
  int rainValue = analogRead(rainSensorPin);
  Serial.print("Rain Sensor Value: ");
  Serial.println(rainValue);

  if (rainValue < rainThreshold) {
    digitalWrite(relayPin, HIGH);
  } else {
    digitalWrite(relayPin, LOW);
  }
  delay(500);
}
🧪 Project Progress Status
✅ 85% Completed

Hardware assembled

Code written and tested

Final enclosure and calibration in progress

📈 Future Enhancements
Add wiper speed control based on rain intensity

Interface with vehicle display/dashboard

Add rain prediction using weather API

Integrate with IoT for remote monitoring

🙋‍♀️ Developed By
DEEPA – Student, VSB Engineering College
Domain: Electronics and Communication Engineering (ECE)

