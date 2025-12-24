
# ImpactWipe: Rain-Water Sensing Automatic Car Wiper

ImpactWipe is an intelligent, automated vehicle safety system designed to eliminate the need for manual wiper adjustments during adverse weather conditions. By integrating rain-sensing technology with a microcontroller, the system enhances driver safety, reduces distractions, and maintains optimal visibility.

---

## Project Overview

Statistics show that rain-related accidents account for nearly 46% of weather-related crashes. Manually adjusting wiper speeds while driving is a dangerous distraction that takes the driver's attention away from the road. 

**ImpactWipe** addresses this by introducing an intelligent control system that automatically regulates speed based on real-time rain intensity.



### Key Features
* **Dual Operating Modes**:
    * **Automatic Mode**: Automatically adjusts wiper speed from low to fast based on rain intensity detected by the sensor.
    * **Manual Mode**: Allows users to override the system and control wiping actions via a mobile app.
* **Bluetooth Connectivity**: Uses an HC-05 module to pair with a smartphone for wireless control.
* **Real-time Feedback**: The mobile app provides continuous status updates on the current speed settings and active mode.

---

## Technical Specifications

### System Architecture
The system utilizes a mapping of requirements to specific sensors and actuators:
* **Control Unit**: Arduino Uno Microcontroller.
* **Sensor**: Rain Sensor Module detects moisture on its surface using electrical conductivity.
* **Actuator**: SG90 Servo Motor receives PWM signals to move the wiper arm to specific positions (0° to 180°).
* **User Interface**: Custom app developed via MIT App Inventor.



### Performance Metrics
* **Response Time**: The system responds to rain detection and switching commands with a lag below **500 ms**.
* **Speed Range**: The servo motor aligns with three distinct wiping speeds (Low, Medium, High) based on intensity.

---

## Cost Analysis

The total production cost for this DIY solution is approximately **₹1,300**, making it significantly more affordable than commercial alternatives which can range from ₹5,000 to ₹20,000.

| Description | Qty | Cost (₹) |
| :--- | :--- | :--- |
| Arduino Uno | 1 | 300 |
| Rain Sensor Module | 1 | 250 |
| Servo Motor (SG90) | 1 | 200 |
| Bluetooth Module (HC-05) | 1 | 150 |
| Power Supply (Battery) | 1 | 200 |
| Cables & Connectors | 1 Set | 50 |
| Enclosure/Box | 2 | 150 |
| **Total** | | **1,300** |

---

## Technical Challenges & Learnings

* **Power Management**: The Bluetooth module was initially unstable when the servo was powered. This was resolved by providing the servo with an **external power supply**.
* **Communication Latency**: The system required real-time interactions, but standard code delays caused disconnections with the MIT App. This was managed by optimizing concurrency and timing.
* **Buffer Overflows**: High-frequency serial data commands sometimes caused buffer overflows, which was mitigated by refining the communication protocol.

---

## Team Members (Team 47)

* **Gautam Arora**: Hardware integration, soldering, assembly, and core Arduino motor control code.
* **Siddhant Gudwani**: Simulations, circuit design, project report, and MIT App development.

---

## References
* Bluetooth HC-05 Documentation (Electronic Wings)
* Arduino Servo Reference (Arduino.cc)
* MIT App Inventor Documentation
