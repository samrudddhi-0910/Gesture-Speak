# Gesture-Speak
Bridging the communication gap with a smart glove that converts hand bends into spoken phrases in real-time.
# 🧤 Sign Language Detecting Glove

A hardware-software prototype built for an **Applied Physics project** that translates finger bends/gestures into readable text. Using an **Arduino Uno**, a **resistive flex sensor**, and an **I2C LCD display**, this smart glove aims to assist individuals who rely on sign language to communicate.

---

## 🚀 How It Works

1. **Auto-Calibration:** On startup, the system calibrates the flex sensor's range by prompting the user to bend their finger. 
2. **Real-Time Mapping:** The system calculates the bend percentage and maps it to vital communication phrases:
   * **0% Bend:** Ready / Active Status
   * **50% Bend:** *"I AM HUNGRY"*
   * **75% Bend:** *"THANK YOU"*
   * **100% Bend:** *"EMERGENCY!!"* or *"NEED WATER"*
3. **Display:** The text output is instantaneously pushed to a 16x2 LCD screen over an I2C communication bus.

---

## 📷 Project Gallery & Demo

### Circuit Schematic
This diagram shows the connection between the Arduino Uno, the Flex Sensor voltage divider, and the I2C LCD module.

![Circuit Diagram](./LCD_I2C_DIA.jpeg)

### The Working Prototype
Here is the assembled hardware displaying a live communication status.

![Glove Prototype](./Sign_language_detecting_glove.jpeg)

### Demo Video
*(Tip: Check out the repository files to see the full demo video!)*

---

## 🛠️ Hardware Requirements

* **Microcontroller:** Arduino Uno (R3)
* **Sensor:** Flex Sensor (2.2" or 4.5")
* **Display:** 16x2 LCD Display with I2C Backboard (saves pins!)
* **Resistor:** 10k Ohm (for the flex sensor voltage divider circuit)
* **Misc:** Breadboard, Jumper Wires, and a Glove to mount the sensor

---

## 🔌 Pin Connections

| Component | Arduino Pin | Description |
| :--- | :--- | :--- |
| **Flex Sensor Pin 1** | 5V | Power |
| **Flex Sensor Pin 2** | A0 | Analog input (via 10k resistor to GND) |
| **LCD SDA** | A4 | I2C Data |
| **LCD SCL** | A5 | I2C Clock |
| **LCD VCC** | 5V | Power |
| **LCD GND** | GND | Ground |

---

## 💻 Software & Libraries

To run this code, you will need the **Arduino IDE** and the following library:
* `LiquidCrystal_I2C` (by Frank de Brabander) — installable directly via the Library Manager in the Arduino IDE.

### How to Run:
1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/SignSense-Glove.git](https://github.com/YOUR_USERNAME/SignSense-Glove.git)
