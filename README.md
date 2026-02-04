# Complete AMBA APB Protocol Verification using SystemVerilog & UVM

This repository presents a complete verification solution for the AMBA APB (Advanced Peripheral Bus) protocol using SystemVerilog and UVM. The project focuses on verifying APB read and write transactions, protocol timing, and handshaking behavior using a structured, coverage-driven verification methodology.

---

## APB Protocol Overview

The AMBA APB protocol is a low-power, low-complexity bus designed for connecting peripheral devices in SoC architectures. APB operates using a non-pipelined transfer mechanism and follows a simple finite state machine consisting of **IDLE**, **SETUP**, and **ACCESS** states. Each transaction requires a minimum of two clock cycles, with optional wait states supported through the PREADY signal.

---

## UVM-Based Verification and Functional Coverage

A complete UVM-based verification environment is developed to validate APB protocol compliance. The environment includes a UVM agent composed of a sequencer, driver, monitor, and scoreboard. Constrained random sequences are used to generate APB read and write transactions, while SystemVerilog Assertions (SVA) check protocol rules such as signal stability, handshaking, and state transitions. Functional coverage is implemented to measure verification completeness across address, data, and control signals.

---

## Verification Features

- UVM agent with sequencer, driver, monitor, and scoreboard  
- Constrained random APB read and write transactions  
- SystemVerilog Assertions (SVA) for protocol compliance  
- Functional coverage for protocol signals and scenarios  
- Verification of transfers with and without wait states  
- Waveform-based debugging for verification closure  

---

## APB Transaction Modeling

The verification environment models APB transactions based on the protocol specification:
- **Write transfers** with and without wait states  
- **Read transfers** with and without wait states  
- Validation of PSEL, PENABLE, PREADY, PWRITE, PADDR, PWDATA, and PRDATA behavior  
- FSM-based sequencing of IDLE, SETUP, and ACCESS phases  

---

## Tools and Methodology

- **Language:** SystemVerilog  
- **Methodology:** UVM (Universal Verification Methodology)  
- **Verification Techniques:**  
  - Constrained random testing  
  - Assertion-based verification  
  - Coverage-driven verification  

---

## Learning Outcomes

- Strong understanding of AMBA APB protocol operation  
- Hands-on experience with UVM verification architecture  
- Practical use of SystemVerilog Assertions and functional coverage  
- Experience in transaction-based and coverage-driven verification  

---

## Reference

The APB protocol behavior and transaction flow are based on standard AMBA APB specifications and academic reference implementations :contentReference[oaicite:1]{index=1}
