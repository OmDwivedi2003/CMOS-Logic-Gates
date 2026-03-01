# CMOS Inverter and NAND Gate Design & Analysis (Cadence Virtuoso)

## 📌 Overview

This project involves the transistor-level design, analysis, and layout implementation of basic CMOS logic gates using Cadence Virtuoso.

Designed Circuits:
- CMOS Inverter
- 2-input CMOS NAND Gate

The objective was to understand:
- CMOS switching behavior
- Voltage Transfer Characteristics (VTC)
- Noise margin calculation
- Propagation delay analysis
- Layout design and physical verification (DRC & LVS)

---

## 🧠 CMOS Inverter

### 🔹 Circuit Description

The CMOS inverter consists of:
- PMOS transistor connected to VDD
- NMOS transistor connected to GND
- Common gate input
- Common drain output

When input is LOW:
- PMOS ON, NMOS OFF → Output HIGH

When input is HIGH:
- PMOS OFF, NMOS ON → Output LOW

---

### 🔹 DC Analysis (VTC)

Performed DC sweep of input voltage to obtain:
- Voltage Transfer Curve
- Switching threshold (VM)
- Noise Margins (NMH & NML)

Observed:
- Sharp transition near threshold voltage
- Proper rail-to-rail output swing

---

### 🔹 Transient Analysis

Applied pulse input and measured:
- Rise time
- Fall time
- Propagation delay (tpHL and tpLH)

Delay variation observed with transistor sizing ratio.

---

### 🔹 Layout Design

- Designed layout using Cadence Virtuoso
- Ensured proper PMOS (in N-well) and NMOS placement
- Used Metal1 and Metal2 routing
- Maintained design rule compliance

Performed:
- DRC (Design Rule Check)
- LVS (Layout vs Schematic)

Both checks passed successfully.

---

## 🧠 2-Input CMOS NAND Gate

### 🔹 Circuit Description

The NAND gate consists of:

Pull-Up Network (PUN):
- Two PMOS transistors in parallel

Pull-Down Network (PDN):
- Two NMOS transistors in series

Operation:
- Output LOW only when both inputs HIGH
- Otherwise output HIGH

---

### 🔹 Analysis Performed

- DC transfer characteristics
- Transient switching behavior
- Delay measurement
- Comparison with inverter performance

Observed:
- Increased delay due to series NMOS resistance
- Asymmetric rise/fall behavior depending on input combination

---

## 📊 Key Observations

- Propagation delay depends on transistor sizing
- NAND gate has higher delay than inverter
- Series transistors increase effective resistance
- Noise margin influenced by threshold voltage
- Layout parasitics affect delay

---

## 🛠 Tools Used

- Cadence Virtuoso (Schematic & Layout)
- Spectre Simulator
- DRC and LVS Verification

---

## 📚 Learning Outcomes

This project strengthened understanding of:

- CMOS switching fundamentals
- Pull-up and pull-down network design
- Noise margin and switching threshold
- Propagation delay calculation
- Physical layout constraints
- DRC/LVS verification process

---

## 🚀 Possible Improvements

- Optimize transistor sizing for symmetric rise/fall delay
- Perform corner analysis
- Extract parasitics (PEX) and re-simulate
- Perform power analysis
- Compare with NOR gate implementation

---

## 👨‍💻 Author

Om Dwivedi  
M.Tech VLSI Design  
NIT Kurukshetra
