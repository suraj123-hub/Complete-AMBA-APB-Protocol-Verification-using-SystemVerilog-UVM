# AMBA APB Protocol Verification using SystemVerilog & UVM

This repository presents a SystemVerilog and UVM-based verification project for the AMBA APB (Advanced Peripheral Bus) protocol. The goal of this work is to verify correct protocol behavior, transaction timing, and data integrity for APB read and write operations using a reusable and coverage-driven verification environment.

---

## Project Overview

AMBA APB is a low-power, low-complexity bus protocol commonly used in System-on-Chip (SoC) designs to interface low-bandwidth peripheral devices. Unlike high-performance buses, APB follows a non-pipelined transfer mechanism and operates using a simple and well-defined transaction flow.

In this project, the APB protocol is verified using a UVM-based testbench written in SystemVerilog. The verification environment focuses on protocol compliance, functional correctness, and robust handling of different transaction scenarios.

---

## APB Protocol Operation

The APB protocol follows a master–slave architecture where the APB master (bridge) initiates transactions and the APB slave responds accordingly. Each APB transfer is performed using three logical states:

- **IDLE** – Default state with no active transfer  
- **SETUP** – Address and control signals are asserted  
- **ACCESS** – Data transfer occurs and the transaction completes  

Each transfer requires a minimum of two clock cycles, and optional wait states are supported through the PREADY signal to accommodate slower peripherals.

---<img width="403" height="314" alt="image" src="https://github.com/user-attachments/assets/d76d755a-c52a-4c7e-8bca-22350c6c4c89" />


## UVM-Based Verification and Functional Coverage

A complete UVM verification environment is developed to validate APB protocol functionality. The environment includes a UVM agent composed of a sequencer, driver, monitor, and scoreboard. Constrained random sequences are used to generate APB read and write transactions that adhere to protocol timing requirements.

SystemVerilog Assertions (SVA) are implemented to check critical protocol properties such as handshaking correctness, signal stability, and valid state transitions. Functional coverage is collected on address, data, and control signals to measure verification completeness and achieve coverage closure.

---

## Verification Strategy

- The APB slave is modeled as a memory-based DUT  
- Randomized read and write transactions are generated using UVM sequences  
- A scoreboard maintains a reference memory model  
- Write operations update both DUT and scoreboard memory  
- Read data from the DUT is compared against the reference model  
- Assertions and coverage ensure protocol compliance and correctness  

---

## Simulation and Results

Simulation results demonstrate correct APB protocol behavior for:
- Read and write transactions  
- Transfers with and without wait states  
- Proper sequencing of IDLE, SETUP, and ACCESS phases  

UVM reports confirm successful verification with no protocol violations or data mismatches, indicating reliable and correct APB protocol operation.

---# AMBA APB Protocol Verification using SystemVerilog & UVM

This repository presents a SystemVerilog and UVM-based verification project for the AMBA APB (Advanced Peripheral Bus) protocol. The goal of this work is to verify correct protocol behavior, transaction timing, and data integrity for APB read and write operations using a reusable and coverage-driven verification environment.

---<img width="517" height="254" alt="image" src="https://github.com/user-attachments/assets/489d7f03-5b55-4f33-bfab-575500758430" />
<img width="408" height="210" alt="image" src="https://github.com/user-attachments/assets/caf3f3dd-bd4d-424f-babd-b2e64dc8f9c2" />
<img width="471" height="250" alt="image" src="https://github.com/user-attachments/assets/fa3bffb0-2b1f-4de8-b49b-bd8864ba5785" />
<img width="524" height="249" alt="image" src="https://github.com/user-attachments/assets/f225024a-cd4b-431b-b456-c0725074f5a0" />
<img width="452" height="285" alt="image" src="https://github.com/user-attachments/assets/40fb41d4-584f-461c-9a93-7a4528beb7ec" />






---
## Tools and Methodology

- **Language:** SystemVerilog  
- **Verification Methodology:** UVM (Universal Verification Methodology)  
- **Verification Techniques:**  
  - Constrained random verification  
  - Assertion-based verification (SVA)  
  - Functional coverage-driven verification  

## Learning Outcomes

- Strong understanding of AMBA APB protocol fundamentals  
- Hands-on experience with UVM-based verification environments  
- Practical use of SystemVerilog assertions and functional coverage  
- Exposure to transaction-based and coverage-driven verification methodologies  


## Reference

This project is conceptually based on standard AMBA APB specifications and SystemVerilog/UVM verification methodologies described in academic literature.
