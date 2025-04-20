# 🧮 Minimal ALU Hardware with TTL Logic & Arduino Control

A minimal Arithmetic and Logic Unit (ALU) built using 74-series TTL ICs and controlled via an Arduino interface. This project demonstrates how core processor logic can be replicated with basic hardware components and interfaced with software over UART.

---

## 🧠 Overview

This project replicates the arithmetic core of a processor — the ALU — using physical hardware logic gates. The ALU is implemented with **TTL chips**, while the **Control Unit** and **Registers** are emulated using an **Arduino**, which interfaces with a **C#-based desktop GUI** via UART.

---

## ⚙️ Features

- 🟢 **Minimal Instruction Set Architecture (ISA)**:
  - `NOT`
  - `AND`
  - `OR`
  - `ADD`
- 🔌 **Built using TTL Logic Chips**: 7400, 7408, 7432, 7486
- 💡 **LED Output**: ALU output is visualized using LEDs
- 🧭 **Arduino as Control Unit**: Decodes instructions and manages data flow
- 🖥️ **Desktop GUI**: C# Windows Forms application to control the ALU and display results

---

## 🧰 Hardware Used

| Component      | Description                         |
|----------------|-------------------------------------|
| 7400           | Quad 2-input NAND gate              |
| 7408           | Quad 2-input AND gate               |
| 7432           | Quad 2-input OR gate                |
| 7486           | Quad 2-input XOR gate               |
| Arduino (Uno)  | Acts as control unit + UART bridge  |
| LEDs & Resistors | For output display and input indication |
| Breadboards & Wires | For circuit prototyping         |

---

## 🖼️ Images

### 1️⃣ Minimal Instruction Set
![Instruction Set](https://github.com/user-attachments/assets/30264b42-4ffd-4fc0-b607-d5e48066730b)

### 2️⃣ Hand-drawn Circuit Diagram
![ALU Circuit](https://github.com/user-attachments/assets/6a4d40f9-0a80-4618-af21-c17840d1e7a0)

### 3️⃣ GUI Interface
![Desktop GUI](https://github.com/user-attachments/assets/3701da78-bb6f-4675-9a99-4252183646cc)

---

## 🔗 Communication

- **UART Serial Protocol** is used between the desktop GUI and the Arduino
- **Control Signals** are decoded by the Arduino and applied to the ALU circuit
- **Result Data** is captured from ALU output pins and sent back for GUI display

---

## 🚀 Future Improvements

- Replace Arduino-based control with **Hardwired Control Logic** using MUX ICs
- Transition from hand-drawn circuit to **schematic/PCB layout tools**
- Expand the instruction set to include **SUB**, **XOR**, and **Shift** operations
- Add support for multiple bit-width operations (e.g., 4-bit ALU)

---

## 🛠️ Getting Started

### Prerequisites

- **Arduino IDE**: To upload the Arduino code that interfaces with the ALU
- **C#/.NET Framework 4.7**: To run the GUI built with Windows Forms
- **TTL ICs**: Required for building the ALU hardware on a breadboard
- **UART Interface**: For communication between the Arduino and the GUI

### Running the System

1. Connect the ALU circuit to Arduino as per the circuit diagram.
2. Upload the Arduino sketch (`control_unit.ino`) to the Arduino.
3. Launch the **C# GUI** application built in Windows Forms.
4. Select the operation, input values, and send the instruction from the GUI.
5. View the ALU's output on the LEDs and the GUI interface.

---

## 📂 Repository Structure

```text
Minimalistic-ALU/
│
├── Arduino/                # Arduino code to control the ALU hardware
│   └── Minimalistic-ALU/
│       └── ALU_revision_2  # Arduino code for ALU hardware control
│
├── ISA/                    # Instruction set and encodings
│   └── minimal_isa.pdf     # PDF with the minimal instruction set
|
|── All other files are for the GUI made in C# and WindowsForms


```

---

## 📜 License

This project is open-source under the MIT License.

---

## 🙌 Acknowledgments

- TTL datasheets and logic gate theory from standard digital electronics references
- Arduino community for serial communication tools
- Inspiration from basic computer architecture tutorials and textbooks
