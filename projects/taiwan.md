**[← Back to Home](../README.md)**

# Taiwan Research Project: PCB Test Platform

## Project Overview
The research project I was apart of was to design and produc a PCB to be used with an MCU for the purpose of testing onboard components. 
The overall purpose is that this board makes the programming, testing, and measuring process more convenient.
Acting as the Device Under Test, our PCB can be placed in a wide range of conditions and its various components (ADC, DAC, Temperature Sensor, and Clock Generator) can be measured externally through an attached microcontroller that is programmed through a computer. During this project, we were able to practice multiple skills and softwares, like soldering, circuit design, PCB design, and C coding.


![PCB Layout](../images/PCBDesign.png)

---

## Design Process

1. **Research** – Started with a reference design and evaluated which components were available and compatible with our requirements. Compared datasheets, checked footprints, and validated pinouts to ensure smooth integration.  
2. **System Design** – Created and updated schematic circuits for the ADC, DAC, clock generator, and temperature sensor. Defined how each peripheral would interface with the MCU via SPI or I²C, and planned for debugging headers and test points.  
3. **PCB Design** – Iterated through multiple board designs, debating between a 4-layer stack (better signal integrity, easier routing) versus a simpler 2-layer board (cheaper, faster to fabricate). Finalized on a 4-layer layout due to the component pads being more suitable on a 4-layer board
4. **Initial Coding** – Before the final board was ready, tested core functionality with through-hole breakout boards (DAC and clock generator). Wrote simple SPI and I²C drivers in C to validate communication and build confidence before committing to soldering the real board.  
5. **Soldering and Testing** – Our first time working with fine-pitch SMD components. Learned reflow and hot-air soldering techniques, practiced cleaning bridges, and confirmed connections with a multimeter. This stage was as much about learning proper hardware assembly as it was about debugging.  
6. **Main Programming** – Developed and refined drivers for all peripherals: DAC (SPI), ADC (SPI), clock generator (I²C), and temperature sensor (I²C). Integrated them into a single firmware project on the LPCXpresso51U68. Debugged timing conflicts, verified voltage outputs, and implemented a button-controlled toggle to demonstrate system-level functionality.  


---

## Components
- **MCU**: LPC51U68 with the LPCXpresso51U68 Devboard
- **ADC**: MCP3424-E/SL (I2c) 
- **DAC**: MCP4822 (SPI)  
- **Clock Generator**: Si5351A (I²C)  
- **Temperature Sensor**: MCP9700AT-E/TT (I2C) 
- **LDO Regulator**: MCP9700AT-E/TT
- **Power Switch**: AP2171DWG-7

---

## Key Learnings
- End-to-end workflow from schematic to tested hardware  
- Debugging soldering and PCB-level issues in real hardware  
- Writing and testing embedded drivers for SPI and I²C  
- Integrating multiple ICs on a single test platform
