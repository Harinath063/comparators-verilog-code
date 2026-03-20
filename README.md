# Verilog 2-Bit and 4-Bit Comparator Simulation

## Project Overview

This project implements and verifies **2-bit and 4-bit digital comparators** using **Verilog HDL**.
The design compares two binary numbers **A** and **B** and produces three outputs:

* **A_gt_B** → A greater than B
* **A_lt_B** → A less than B
* **A_eq_B** → A equal to B

The project is simulated using **Icarus Verilog** and visualized using **GTKWave**.

---

# Tools Used

* Icarus Verilog – Verilog simulation
* GTKWave – waveform viewer
* GitHub – project hosting

---

# Project Structure

```
Comparator_Project
│
├── comparator.v        # Verilog design (2-bit and 4-bit comparator)
├── comparator_tb.v     # Testbench for simulation
├── comparator.vcd      # Generated waveform file
└── README.md           # Project documentation
```

---

# Comparator Logic

The comparator generates three outputs:

| Condition | Output     |
| --------- | ---------- |
| A > B     | A_gt_B = 1 |
| A < B     | A_lt_B = 1 |
| A = B     | A_eq_B = 1 |

Only **one output is high at a time**.

---

# 2-Bit Comparator Truth Table

| A  | B  | A>B | A<B | A=B |
| -- | -- | --- | --- | --- |
| 00 | 00 | 0   | 0   | 1   |
| 00 | 01 | 0   | 1   | 0   |
| 00 | 10 | 0   | 1   | 0   |
| 00 | 11 | 0   | 1   | 0   |
| 01 | 00 | 1   | 0   | 0   |
| 01 | 01 | 0   | 0   | 1   |
| 01 | 10 | 0   | 1   | 0   |
| 01 | 11 | 0   | 1   | 0   |
| 10 | 00 | 1   | 0   | 0   |
| 10 | 01 | 1   | 0   | 0   |
| 10 | 10 | 0   | 0   | 1   |
| 10 | 11 | 0   | 1   | 0   |
| 11 | 00 | 1   | 0   | 0   |
| 11 | 01 | 1   | 0   | 0   |
| 11 | 10 | 1   | 0   | 0   |
| 11 | 11 | 0   | 0   | 1   |

---

# How to Run the Simulation

### 1. Compile the design

```
iverilog -o comparator comparator.v comparator_tb.v
```

### 2. Run simulation

```
vvp comparator
```

This generates the waveform file:

```
comparator.vcd
```

### 3. Open waveform viewer

```
gtkwave comparator.vcd
```

---

# Waveform Output

The waveform shows the behavior of:

* A2[1:0]
* B2[1:0]
* A4[3:0]
* B4[3:0]
* gt2
* lt2
* eq2
* gt4
* lt4
* eq4

These signals verify the correct operation of both comparators.

---

# Simulation Screenshot

Example waveform from GTKWave:

(Add your waveform screenshot here)

---

# Learning Outcomes

This project demonstrates:

* Verilog module design
* Testbench creation
* Digital comparator logic
* Simulation using Icarus Verilog
* Waveform analysis using GTKWave
* Basic GitHub project documentation

---

# Author
V.Venkata Harinath
Diploma ECE SVGP TIRUPATI

Electronics Engineering Student
Digital Design Practice Project
