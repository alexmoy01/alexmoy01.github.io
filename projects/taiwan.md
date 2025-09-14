**[← Back to Home](../README.md)**

# Taiwan Research Project: PCB Test Platform

## Project Overview
Design a PCB test platform for ADC, DAC, clock generator, and temperature sensor validation.  
This project was part of my research work in Taiwan, where I practiced the **full embedded systems workflow**: schematic capture, PCB layout, soldering, firmware development, and system debugging.

![PCB Layout](../images/taiwan-pcb.png)

---

## Design Process
1. **Schematic Capture** – Designed circuits for ADC, DAC, clock generator, and temperature sensor.  
2. **PCB Layout** – Created a 2-layer PCB in Altium, optimized trace routing, and managed ground/power planes.  
3. **Assembly** – Hand-soldered and reflowed components, then verified connectivity and signal integrity.  
4. **Firmware Development** – Wrote embedded C drivers for SPI and I²C communication on the LPCXpresso51U68 MCU.  
5. **Debugging** – Resolved soldering bridges, trace routing issues, and communication protocol errors.  

---

## Components
- **MCU**: NXP LPCXpresso51U68 (ARM Cortex-M0+)  
- **ADC**: 3-channel SPI-based ADC  
- **DAC**: MCP4822 (SPI)  
- **Clock Generator**: Si5351A (I²C)  
- **Temperature Sensor**: I²C-based digital sensor  
- **Misc**: Passive components, power regulation, headers for testing  

---

## Key Learnings
- End-to-end workflow from schematic to tested hardware  
- Debugging soldering and PCB-level issues in real hardware  
- Writing and testing embedded drivers for SPI and I²C  
- Integrating multiple ICs on a single test platform
