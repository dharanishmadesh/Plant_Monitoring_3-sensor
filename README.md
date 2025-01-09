

# **Automated Plant Watering System** 🌱💧

This project utilizes soil moisture sensors (MOS) to monitor the moisture levels of three plants. Based on the moisture readings, it automatically controls motors to water the plants when necessary. If the moisture level falls below a preset threshold, a motor is activated to water the corresponding plant.

---

## **📂 Project Files**

- `AutomatedPlantWatering.ino`  
  - Arduino code for the automated watering system.

---

## **🔧 Hardware Required**

- **Arduino Uno / Nano** (or any compatible board)
- **3x Soil Moisture Sensors**
- **3x DC Motors** (for watering)
- **3x Motor Drivers (e.g., L298N)**
- **Wires**
- **Breadboard**

---

## **🔨 Circuit Diagram**

- **Moisture Sensors** (MOS1, MOS2, MOS3) connected to **A0, A1, A2** pins respectively.
- **Motor Drivers** are connected to **Pins 2, 3, and 4** for controlling the motors.
- Motors are powered via the motor driver to water the plants.

---

## **💻 Code Overview**

### **Setup**

- The system uses three soil moisture sensors connected to analog input pins **A0, A1, and A2**.
- The motors are connected to digital pins **2, 3, and 4** to control watering based on moisture levels.
- The system initializes communication with the **Serial Monitor** and sets pin modes.

### **Loop**

1. **Soil Moisture Readings**:
    - The analog readings from the moisture sensors are obtained.
    - The readings are then mapped from a 0-1023 range to 0-100, representing the moisture percentage.
  
2. **Plant Moisture Monitoring**:
    - The moisture values for each plant are printed on the Serial Monitor for feedback.

3. **Motor Activation**:
    - If a plant's moisture level is lower than its preset threshold (`Pmosv1`, `Pmosv2`, `Pmosv3`), the corresponding motor is turned on to water the plant.
    - If all moisture levels are above their thresholds, all motors are turned off.

---

## **⚙️ Code Explanation**

- **Mapping**: The `map()` function is used to convert the analog values of the moisture sensors into a percentage for easier interpretation.
- **Threshold Comparison**: The moisture value of each plant is compared against a set threshold (`Pmosv1`, `Pmosv2`, `Pmosv3`), and if the value is below the threshold, the corresponding motor is activated.
- **Motor Control**: The motors are controlled using `digitalWrite()`, setting the corresponding pins HIGH or LOW.

---

## **⚠️ Notes**

- Adjust the **threshold values** (`Pmosv1`, `Pmosv2`, `Pmosv3`) based on the moisture levels appropriate for your plants.
- The motors will turn on for **3 seconds** when watering is needed, but you can adjust the duration as required.

---

## **💡 Future Improvements**

- **Add more plants**: You can scale the system by adding more moisture sensors and motors for additional plants.
- **Add a water pump**: Integrate a water pump with a relay for a more automated watering process.
- **Mobile App Integration**: Develop an app to monitor and control the watering system remotely.

---

## **👨‍💻 Author**

- **Technical Tamizha**  
  - [Website](https://www.procreativehub.com)

