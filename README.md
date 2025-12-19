# IoT Smart Parking System using ESP32 🚗

A real-time smart parking management system that automates entry/exit gates and displays slot availability on a web-based dashboard. This project uses an ESP32 acting as a local web server to provide latency-free updates without relying on cloud subscriptions.

## 🌟 Features
* **Automated Entry/Exit:** IR sensors detect vehicles and control the servo barrier gate automatically.
* **Real-Time Web Dashboard:** Displays available slots, occupied slots, and gate status instantly.
* **Visual Feedback:** Dynamic HTML/CSS interface with glowing indicators for "Open/Closed" states.
* **Non-Blocking Logic:** Uses `millis()` timers to ensure the web server remains responsive while the gate is moving.
* **WiFi Enabled:** Hosted locally on the ESP32 (accessible via IP address).

## 🛠️ Hardware Requirements
* **Microcontroller:** ESP32 Development Board
* **Sensors:** 2x IR Proximity Sensors (Entry & Exit)
* **Actuator:** 1x SG90 or MG995 Servo Motor
* **Indicators:** Red & Green LEDs
* **Power Supply:** 5V Micro USB or external battery
* **Misc:** Breadboard, Jumper Wires

## 🔌 Pin Configuration
| Component | ESP32 Pin | Description |
| :--- | :--- | :--- |
| **IR Entry Sensor** | GPIO 18 | Detects car entering |
| **IR Exit Sensor** | GPIO 19 | Detects car leaving |
| **Servo Motor** | GPIO 25 | Controls Barrier Gate |
| **Green LED** | GPIO 26 | Indicates "Available" |
| **Red LED** | GPIO 27 | Indicates "Full" |

## ⚙️ Software & Libraries
This project is built using the **Arduino IDE**.
* **Board Package:** ESP32 by Espressif Systems
* **Required Library:** `ESP32Servo` (Install via Library Manager)
* **Web Technologies:** HTML, CSS (Tailwind via CDN), JavaScript (AJAX for async updates).

## 🚀 How to Run
1.  **Install ESP32 Board:** Go to Arduino IDE > Preferences > Additional Boards Manager URLs and add the ESP32 URL.
2.  **Install Library:** Go to Sketch > Include Library > Manage Libraries and search for `ESP32Servo`.
3.  **Configure Network:** Open `SmartParkingSystem.ino` and update the `ssid` and `password` variables with your WiFi credentials.
4.  **Upload:** Connect your ESP32 and upload the code.
5.  **Access Dashboard:** Open the Serial Monitor (115200 baud) to find the ESP32's IP address (e.g., `192.168.1.X`). Type this IP into your browser.

## 📄 License
This project is open-source and available for educational purposes.
