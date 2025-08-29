# Raspberry Pi Pico PIN Brute-Force Tool

![Raspberry Pi Pico](https://www.raspberrypi.com/app/uploads/2021/01/pico-1-768x512.jpg)

## **📌 Project Overview**
This project demonstrates a **PIN brute-force testing tool** built using the **Raspberry Pi Pico** microcontroller. It uses **USB HID emulation** to attempt PIN codes automatically, with **OLED live feedback**, **lockout detection**, and **randomized delays**.

⚠️ **Educational Use Only** — Designed for **authorized penetration testing** and **college cybersecurity research**.

---

## **✨ Features**
- **OLED Feedback** → Displays real-time PIN attempts and lockout status.
- **Smart Lockout Detection** → Uses a photoresistor to pause automatically when lockout occurs.
- **Randomized Delays** → Mimics human typing speed to evade detection.
- **Common PIN Optimization** → Prioritizes frequently used PINs before brute-forcing sequentially.
- **Portable Operation** → Powered by LiPo battery; works standalone.
- **USB HID Compliance** → Identifies as a standard keyboard.

---

## **🛠 Hardware Requirements**
| Component            | Purpose                      | Cost (USD) | Key Feature |
|---------------------|-------------------------------|------------|-------------|
| Raspberry Pi Pico   | Main microcontroller         | $4         | USB HID via CircuitPython |
| 0.96" OLED (I2C)    | Live feedback display        | $3         | Real-time status |
| LiPo Battery (500mAh) | Portable power             | $5         | Standalone operation |
| TP4056 Charger Module | Battery recharging         | $1         | Safe charging |
| Photoresistor (LDR) | Detects lockout screens     | $0.50      | Adjusts delays |
| 3D-Printed Case     | Stealth enclosure           | $2         | Optional |

💰 **Total Cost:** ~ **$15 – $20**

---

## **🔌 Wiring Guide**
| Pico Pin | Component       | Connection |
|----------|----------------|------------|
| GP0 (SDA) | OLED           | SDA |
| GP1 (SCL) | OLED           | SCL |
| 3V3      | OLED + LDR      | VCC |
| GND      | OLED + LDR      | GND |
| A0       | Photoresistor   | Signal |
| VBUS     | LiPo Charger    | 5V Input |

*(See `wiring_diagram.png` for a visual guide.)*

---

## **⚡ Installation & Setup**
1. Flash **CircuitPython** on your Raspberry Pi Pico.
2. Install required libraries:
   ```bash
   adafruit-hid
   adafruit-ssd1306
   ```
3. Copy `main.py` to your Pico.
4. Connect the OLED, photoresistor, and LiPo battery as per wiring diagram.
5. Safely test the setup **only on authorized devices**.

---

⚠️ **Disclaimer:**
> This tool is intended for **educational and authorized security testing** only. Using it on devices or systems **without explicit permission** is illegal.

---

## **📄 Documentation**
For the complete build guide, CircuitPython code, and full explanations, see the PDF report:

📄 **[Raspberry Pi Pico PIN Brute-Force Tool - Vijay]

---

## **👨‍💻 Author**
**Vijay** — Cybersecurity Enthusiast & Researcher
