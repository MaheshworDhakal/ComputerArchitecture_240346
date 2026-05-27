# Lab 2: VHDL Code for Realizing Logic Gates

## Objective
- To write VHDL code for basic logic gates:
  - AND
  - OR
  - NOT
  - NAND
  - NOR
  - XOR
  - XNOR
- To simulate each gate and verify the truth table using GTKWave.

---

## Theory

Logic gates are the fundamental building blocks of digital circuits. Each gate performs a Boolean operation on one or more binary inputs and produces a single binary output.

| Gate | VHDL Operator | Boolean Expression |
|------|----------------|-------------------|
| AND | and | Y = A · B |
| OR | or | Y = A + B |
| NOT | not | Y = A̅ |
| NAND | nand | Y = (A · B)̅ |
| NOR | nor | Y = (A + B)̅ |
| XOR | xor | Y = A ⊕ B |
| XNOR | xnor | Y = (A ⊕ B)̅ |

---

## Files Used

- and_gate.vhd  
- or_gate.vhd  
- not_gate.vhd  
- nand_gate.vhd  
- nor_gate.vhd  
- xor_gate.vhd  
- xnor_gate.vhd  
- gates_tb.vhd  

---

## Simulation Commands

### Analyze VHDL files
ghdl -a and_gate.vhd or_gate.vhd not_gate.vhd nand_gate.vhd nor_gate.vhd xor_gate.vhd xnor_gate.vhd gates_tb.vhd

### Elaborate testbench
ghdl -e GATES_TB

### Run simulation
ghdl -r GATES_TB --vcd=simulation.vcd

### Open waveform in GTKWave
gtkwave simulation.vcd

---

## Expected Truth Table

| A | B | AND | OR | NOT A | NAND | NOR | XOR | XNOR |
|---|---|-----|----|-------|------|-----|-----|------|
| 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 |

---

## Simulation Output

### GTKWave Output
![Simulation Output](image.png)

---

## Conclusion

The VHDL implementation of basic logic gates was successfully completed.  
The simulation results matched the expected truth table, confirming correct functionality of all logic gates.
