# 🦖 T-Rex Game with LDR & Servo Integration

An innovative enhancement to the classic **T-Rex running game** that incorporates real-world sensor input. By integrating an **LDR (Light Dependent Resistor)** and a **servo motor**, this project simulates physical interaction with the virtual game, offering a fresh and engaging gaming experience.

---

## 🏫 Project Information

* **University:** Benha University, Faculty of Engineering (Shoubra)  
* **Department:** Communications and Computer Engineering  
* **Course:** Measurement and Instrumentation 

---

## 👩‍💻 Team Members

* Mohamed Ahmed Mohamed Hassan  
* Farida Waheed Abdelbary 
* Raneem Ahmed Refaat
* Razan Ahmed Fawzy 

---

## 📌 Project Overview

This project introduces a hardware-driven way to control the T-Rex dinosaur in the well-known Chrome game using:

- An **LDR sensor** to detect light intensity.
- A **servo motor** to simulate physical movement in sync with the game.

The player can trigger a jump in-game by simply changing the ambient light — like waving a hand over the LDR.

---

## 🧠 System Features

- **LDR Sensor**: Detects light level changes and converts them to signals.
- **Servo Motor**: Responds to LDR signals by jumping (moving to 45°) or resetting (70°).
- **Arduino (UNO/Nano)**: Central controller running the `Dinasor.ino` sketch.
- **Game Interface**: Google Chrome’s T-Rex game, with servo-controlled jumps.

---

## ⚙️ Hardware Components & Circuit Connections

| Component       | Description                                       |
|----------------|---------------------------------------------------|
| LDR Sensor      | Detects changes in ambient light                 |
| Servo Motor     | Physically jumps the T-Rex using angular motion  |
| Arduino         | Runs the control logic (via `Dinasor.ino`)       |
| Resistors       | Pull-down or pull-up configuration               |
| USB Cable       | Connects Arduino to computer running the game    |
| Optional LED    | Indicates sensor activity visually               |

**Connection Highlights:**

- LDR to analog pin (e.g., A0)
- Servo to digital PWM pin (e.g., D9)
- Use voltage divider for LDR input
- Map LDR values to servo control angles

---

## 🧾 How It Works

1. The **Arduino** initializes the servo and reads the LDR input.
2. When ambient light decreases (e.g., hand covers LDR):
   - A threshold is passed.
   - The **servo jumps** (45° angle), signaling a T-Rex jump.
3. When light returns:
   - The servo resets to **70° angle**.
4. The cycle repeats — simulating real-time interaction with the game.

---

## 📐 Algorithm Flow

1. Initialize Arduino, LDR, and Servo.
2. Continuously read light level from the LDR.
3. Compare light value with threshold.
4. If light < threshold:
   - Rotate servo to simulate a jump.
5. Else:
   - Reset servo to default position.
6. Loop execution continuously during gameplay.

---

## 🧪 Testing Results

| Scenario                        | Expected Output                     | Status |
|---------------------------------|-------------------------------------|--------|
| Cover LDR                       | Servo jumps (T-Rex jumps)           | ✅     |
| Uncover LDR                     | Servo returns to 70°                | ✅     |
| Low ambient light               | Multiple jump triggers              | ✅     |
| Upload `.ino` file to Arduino  | Code compiles and runs successfully | ✅     |

---

## 💾 Code Files

* `Dinasor.ino` – Main Arduino sketch controlling LDR and servo.

---

## 🖼 Demonstration Media

* **Video**: [`Dinasour.mp4`](#) – Full gameplay with physical interaction  
* **Presentation**: `T-rex Game.pptx` – Summary of project setup and concept  
* **Report**: `T-rex.pdf` – Detailed technical and theoretical documentation  

---

## 🛠 Tools Used

* **Arduino IDE** – Code upload and testing  
* **Servo Motor & LDR** – Real-world input/output components  
* **Chrome T-Rex Game** – Virtual game interface  
* **Breadboard / PCB** – Circuit prototyping  

---

## 🏁 Conclusion

By blending sensor input with a virtual game, this project turns a traditional keyboard-based experience into a **physical, interactive adventure**. It showcases the possibilities of combining embedded systems with gamification for a **multi-sensory** experience.


