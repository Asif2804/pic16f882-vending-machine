# Coin-Operated Vending Machine Simulation (PIC16F882)

This project simulates a fully functional, coin-operated drink vending machine using a PIC16F882 microcontroller. It handles drink selection, coin insertion, dispensing, change return, and tilt-detection alarms, all through embedded C programming and real-time control logic.

---

## 🧠 Project Overview

This embedded system mimics a retail vending machine, enabling:
- Drink selection via push buttons
- Coin insertion (10p, 20p, 50p)
- Simulated drink dispensing and change return using LEDs
- Anti-tamper detection with a tilt sensor
- LCD-based user interface
- Real-time interrupt and ADC management

---

## 🔧 Technologies & Tools
- **Microcontroller**: PIC16F882
- **Programming Language**: C
- **Development Environment**: MPLAB X IDE with XC8 compiler
- **Hardware Simulation**: PIC development board
- **Inputs**: Push buttons, potentiometer (tilt sensor)
- **Outputs**: Character LCD, LEDs

---

## 🕹️ System Functionality

| Feature            | Description                                              |
|-------------------|----------------------------------------------------------|
| **Drink Selection** | Cycle through drinks using RB0, confirm with RB1         |
| **Coin Insertion** | Add 10p (RB0), 20p (RB1), 50p (RB2)                       |
| **Dispensing**     | RA0 LED lights up for 5s when balance is sufficient      |
| **Change Return**  | RA1 LED lights up if user overpays                       |
| **Tilt Detection** | Simulated using a potentiometer (VR2) on ADC channel AN0 |
| **Alarm State**    | Triggers LCD alert and locks machine on tilt detection  |

---

## ⚙️ System States
Implemented as a **finite state machine**:
1. Idle
2. Drink Selection
3. Coin Insertion
4. Dispensing
5. Change Dispense
6. Drink Ready
7. Alarm (Tilt Detected)

---

## 🧪 Testing Summary

| Test                          | Result                        |
|------------------------------|-------------------------------|
| Drink Selection               | Pass – correct item selected  |
| Coin Insertion & Balance     | Pass – correct total tracked  |
| Dispensing Logic             | Pass – RA0 LED for 5s         |
| Change Return                | Pass – RA1 LED for 5s         |
| Tilt Detection & Alarm       | Pass – triggers immediately   |
| LCD Display & Feedback       | Pass – clear and accurate     |

---

## 🚀 Future Improvements
- Use TMR1 for improved timing precision
- Add EEPROM logging for transaction history
- Expand to multiple drink prices and inventory
- Add physical coin return mechanism
- Support for more user input modes (e.g., touch or keypad)

---

## 📄 License
MIT License — feel free to use or adapt for educational purposes.

---

## 👤 Author
Asif Hussain    
🔗 [asifh.me](https://asifh.me/work/Embedded-System)
