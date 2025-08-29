# 🔐 Raspberry Pi Pico PIN Brute-Force Tool  
**Features:** OLED Feedback • Lockout Detection • Randomized Delays • USB HID  
**Author:** Vijay  
**⚠️ Legal Use Only – For Educational & Authorized Penetration Testing**

---

## 📌 Overview  
This project demonstrates how to build a **PIN brute-force testing tool** using a **Raspberry Pi Pico**.  
It leverages the Pico’s **USB HID capabilities** to simulate keystrokes, display feedback on an **OLED screen**, and intelligently handle lockouts using a **photoresistor-based detection system**.

⚠️ **Disclaimer**  
> This project is for **educational purposes** only.  
> Use it **only** on devices you own or have explicit permission to test.  
> Unauthorized use is illegal and may have consequences.

---

## 🛠️ Hardware Components

| Component                | Purpose                                | Cost (USD) | Key Feature                     |
|------------------------|-------------------------------------|-----------|--------------------------------|
| **Raspberry Pi Pico**      | Core microcontroller & USB HID       | $4        | CircuitPython, USB HID support |
| **0.96" OLED (I2C)**      | Displays PIN attempts               | $3        | Real-time feedback             |
| **LiPo Battery (500mAh)** | Portable power                      | $5        | Untethered operation           |
| **TP4056 Charger Module** | Safely recharge battery             | $1        | DIY power management           |
| **Photoresistor (LDR)**   | Detects screen lockouts             | $0.50     | Auto delay adjustment          |
| **3D-Printed Case**       | Disguises tool as USB drive         | $2        | Stealth look                  |

**💰 Total Cost:** ~$15–20 *(cheaper than commercial pentest tools)*

---

## ⚡ Features

- **OLED Live Feedback** → Displays current PIN, attempts, and lockout status  
- **Auto Lockout Detection** → Uses LDR to pause attempts during lockouts  
- **Randomized Delays** → Mimics human typing to avoid detection  
- **Common PIN Priority** → Tries common PINs first, then switches to random  
- **Portable Operation** → Works on LiPo battery, no PC required  
- **USB HID** → Appears as a keyboard to the target device

---

## 🔌 Circuit Wiring

| Pico Pin | Component       | Connection |
|---------|----------------|-----------|
| GP0     | OLED           | SDA       |
| GP1     | OLED           | SCL       |
| 3V3     | OLED + LDR     | VCC       |
| GND     | OLED + LDR     | GND       |
| A0      | Photoresistor  | Signal    |
| VBUS    | TP4056         | Battery Charging |

---

## 📜 Installation & Setup

1. **Flash CircuitPython**  
   - Download the latest **CircuitPython UF2** for Raspberry Pi Pico.
   - Drag & drop onto the Pico’s drive.

2. **Install Required Libraries**  
   Copy these to the Pico's `lib` folder:  
   - `adafruit_hid`
   - `adafruit_ssd1306`

3. **Upload the Code**  
   - Save `bruteforce.py` to the Pico.
   - Rename it to `code.py` if you want it to **auto-run** on boot.

4. **Connect to Target Device**  
   - Plug the Pico into your test device.
   - It will simulate keystrokes automatically.

---

## 🧩 Usage

- On startup, the OLED shows the **current PIN** and **attempt count**.
- The Pico automatically enters PINs via USB HID.
- If the LDR detects a **lockout**, attempts **pause** automatically.
- After the lockout delay, brute-forcing resumes automatically.

---

## 🛡️ Ethical Reminder  

⚠️ Use this tool **only** on systems you **own** or are **authorized** to test.  
⚠️ Misuse could lead to **legal action** and **security alerts**.

---


