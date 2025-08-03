# Bidirectional DC-DC Converter for EVs Battery Power Management

## Overview
This project focuses on designing and implementing a bidirectional DC-DC converter for electric vehicles (EVs) to manage power efficiently between the battery and the motor. The converter supports both buck (step-down) and boost (step-up) operations, enabling energy flow during motoring and regenerative braking. Using a cascade buck-boost topology, the system was developed with a 24V battery (two 12V 7Ah lead-acid batteries in series) and a 12V 100W brushed DC motor, demonstrating a practical solution for EV power management.

## Team Members
- Rohhit Pratap Singh (1022040365)
- Vishhayjeet Singh Bains (1022040455)
- Dinesh (1022040485)
- Ankit Besara (1022040505)

## Mentors
- Dr. Yogesh Tatte
- Dr. Shreedhar Joshi

## Problem Statement
Traditional DC-DC converters in EVs face several challenges:
- **Voltage Fluctuations:** Unstable battery voltage and varying load demands cause inconsistent motor power supply, affecting performance.
- **Inefficient Regenerative Braking:** Conventional converters fail to optimize energy recovery, leading to energy waste as heat.
- **Power Losses:** Switching, conduction, and thermal losses reduce efficiency, shortening battery life and driving range.

## Objectives
- Design a compact bidirectional DC-DC converter using a cascade buck-boost configuration.
- Demonstrate buck mode (24V to 12V) for motor powering and boost mode (10V to 24V) for regenerative braking.
- Implement control algorithms using an Arduino Uno for optimal power transfer.
- Monitor system parameters with sensors for protection and performance.
- Analyze efficiency and voltage regulation through simulation and testing.

## Methodology
![alt text](image.png)
The project followed a structured development process:
1. **Literature Survey:** Reviewed bidirectional converter topologies and control strategies (e.g., IEEE VPPC 2008).
2. **Topology Selection:** Adopted a cascade buck-boost configuration for efficient bidirectional power flow.
3. **Component Selection:** Chose cost-effective components like MOSFETs, inductors, and sensors based on system needs.
4. **Passive Element Calculations:** Determined inductor and capacitor values to minimize ripple and ensure stability.
5. **Simulation:** Validated design in MATLAB/Simulink with duty cycles of 50% (buck) and 58.3% (boost).
6. **Control Implementation:** Programmed Arduino Uno to generate 20 kHz PWM signals for mode switching.
7. **Hardware Prototype:** Assembled the converter on a breadboard with real-time sensor feedback.
8. **Testing:** Measured output voltage, current, and efficiency, comparing results to theoretical predictions.

## Converter Topology
![alt text](image-1.png)
The cascade buck-boost topology uses two bidirectional switches (MOSFETs with body diodes), coupled inductors (100 µH), and capacitors (470 µF) to enable seamless buck and boost operations. A series Rd-Cd network damps resonance, enhancing stability.

## Components
- **MOSFETs:** IRF244N
- **Drivers:** TC4420
- **Diodes:** MBR2010CT (Schottky)
- **Inductor:** 100 µH, 10A rating
- **Capacitors:** 470 µF, 35V rating
- **Microcontroller:** Arduino Uno
- **Sensors:** INA219 for current and voltage monitoring

## Simulation Results
- **Boost Mode:** Input 15V, Output 22.6V
![alt text](image-2.png)
![alt text](image-3.png)
- **Buck Mode:** Input 24V, Output 12V  
![alt text](image-4.png)
![alt text](image-5.png)
Simulations confirmed stable voltage regulation and efficient power transfer.

## Project Outcomes
- **Efficient Power Transfer:** Reduced losses, maximizing energy utilization.
- **Voltage Regulation:** Stable output under dynamic loads, enhancing reliability.
- **Regenerative Braking:** Effective energy recovery, improving EV sustainability.
- **Scalability:** Adaptable design for various EV models.

## Deliverables
- Functional hardware prototype.
- Circuit schematics and PCB layout.
- Arduino-based control algorithm.
- Test results and documentation.
- Simulation models with performance analysis.

## Challenges and Solutions
- **Challenge:** Voltage instability during mode transitions.  
  **Solution:** Implemented real-time feedback control with INA219 sensors.
- **Challenge:** Power losses in components.  
  **Solution:** Used low RDS(on) MOSFETs and optimized switching frequency.

## Skills Gained
- Power electronics design and component selection.
- Microcontroller programming (Arduino).
- Simulation and modeling (MATLAB/Simulink).
- Hardware prototyping and performance testing.

## Conclusion
This project successfully developed a bidirectional DC-DC converter that enhances EV power management by addressing voltage stability, energy efficiency, and regenerative braking. It demonstrates practical skills in power electronics and system integration, contributing to sustainable electric mobility.