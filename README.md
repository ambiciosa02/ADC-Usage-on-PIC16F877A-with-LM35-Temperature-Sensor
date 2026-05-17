# ADC Usage on PIC16F877A with LM35 Temperature Sensor

## 🎯 1. Introduction

This practical work aims to study the use of the **Analog-to-Digital Converter (ADC)** of the **PIC16F877A** microcontroller by using the **LM35 analog temperature sensor**. The goal is to understand how a physical quantity (temperature) can be converted into a usable digital value.

---

## 📚 2. Objectives

- ✅ Understand the principle of analog-to-digital conversion
- ✅ Use the LM35 temperature sensor
- ✅ Configure and operate the ADC of the PIC16F877A
- ✅ Verify results under Proteus simulation
- ✅ Implement an overheating detection system

---

## 📐 3. Theoretical Background

**LM35 Temperature Sensor:** Vout = 0.01 × T (10mV per 1°C)

**PIC16F877A ADC:** Converts 0-5V to 10-bit value (0-1023)

**Conversion Formula:** ADC Value = (Vout / 5) × 1023

---

## 🧱 4. Project Structure

**Part A – LM35 Study under Proteus:** Simulate LM35 alone to verify linear behavior. 

<br>
<img width="223" height="135" alt="image" src="https://github.com/user-attachments/assets/24678e55-d9b0-4305-a112-53a8973f37e2" />
<br>

**Part B – ADC Reading:** Read LM35 output using ADC, display 10-bit binary result on LEDs (PORTC + RD0/RD1).

<img width="306" height="303" alt="image" src="https://github.com/user-attachments/assets/6c699dcc-2d98-4072-9a6c-9753f7c4c4b3" />
<br>

<img width="378" height="262" alt="image" src="https://github.com/user-attachments/assets/9d224a3e-c57a-42f4-a2e0-bf43eb6591af" />
<br>

**Part C – Experimental Verification:** Compare measured vs theoretical values.
<br>
<img width="470" height="116" alt="image" src="https://github.com/user-attachments/assets/3f4ffa2a-409d-4ae2-89aa-c50791ba445d" />
<br>

**Part D – Overheating Detection:** Threshold at 60°C triggers alarm LED. 
<br>
<img width="379" height="293" alt="image" src="https://github.com/user-attachments/assets/8b5705b5-0bf8-4a01-bfa4-6d357e50263b" />
<br>
<br>
<img width="378" height="209" alt="image" src="https://github.com/user-attachments/assets/abaf8615-e55a-4ce5-aca0-fba9c804db31" />
<br>
**Part E – Bonus (7-Segment Display):** Convert ADC value to temperature and display on two 7-segment digits. Formula: T(°C) = (ADC × 500) / 1023. 
<br>

<img width="377" height="258" alt="image" src="https://github.com/user-attachments/assets/2cf04e28-82d1-442a-82d5-5910c6b00690" />

<br>
<img width="379" height="205" alt="image" src="https://github.com/user-attachments/assets/9cec43cc-221f-40b9-9076-3b30e1bcbe40" />

<br>

## 🧰 5. Components Used

| Component | Reference |
|-----------|-----------|
| Microcontroller | PIC16F877A |
| Temperature sensor | LM35 |
| IDE | mikroC Pro for PIC |
| Simulator | Proteus ISIS |
| LEDs | 10x + 1x alarm |
| 7-segment displays | 2x |
| Resistors | 220Ω, 10kΩ |
| Clock frequency | 20 MHz |
| ADC resolution | 10 bits |

---

## 🔧 6. Key Register Configurations

| Register | Configuration | Purpose |
|----------|---------------|---------|
| ADCON1 | ADFM = 1 | Right-aligned result |
| ADCON0 | Channel AN0 | Select analog input |
| TRISA | RA0 as input | Analog input pin |
| TRISC | Output | Lower 8 bits |
| TRISD | Output for RD0/RD1 | Upper 2 bits |

---

## 📈 7. Formulas Used

| Formula | Purpose |
|---------|---------|
| Vout = 0.01 × T(°C) | LM35 output voltage |
| ADC Value = (Vout / 5) × 1023 | Voltage to digital |
| T(°C) = (ADC × 500) / 1023 | Digital to temperature |
| Vout = (ADC × 5) / 1023 | Digital to voltage |

---

## 🚀 8. How to Run the Project

**In mikroC:** Open project, verify PIC16F877A @ 20MHz, configure ADC, compile (F9) to generate .hex

**In Proteus:** Open schematic, load .hex into PIC, click Play ▶️, vary LM35 temperature, observe LEDs and 7-segment display

---

## 🧠 10. Key Learnings

- ✅ LM35 temperature sensor (10mV per °C)
- ✅ ADC configuration on PIC16F877A
- ✅ Analog voltage to 10-bit digital conversion
- ✅ Binary display on LEDs
- ✅ Overheating detection for safety systems
- ✅ ADC value to temperature conversion
- ✅ 7-segment temperature display
- ✅ Proteus analog sensor simulation

---

## 🔗 11. Practical Applications

Digital thermometers | Fire detection systems | Industrial monitoring | Automotive engine warning | Smart home climate control | Refrigeration systems


## ⚖️ 14. License

📚 This project is for **educational purposes only**.
