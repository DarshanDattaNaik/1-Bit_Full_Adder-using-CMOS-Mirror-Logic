# 1-Bit_Full_Adder-using-CMOS-Mirror-Logic
[Abstract](# Abstract)

























# Abstract
Adders are one of the main components of majority of circuits and find their application in ALU’s, microprocessors, DSP processors.1-Bit Full adder can be used to implement other circuits such as Ripple Carry Adder, Multipliers. A 1-bit full adder using CMOS mirror logic is designed and implemented in this repository. The implementation will be done in 28nm technology node using Synopsys tools. The reference waveforms will be verified with actual waveforms obtained from simulation.
# Reference Circuit Details
A one bit full adder has two circuit blocks, with three inputs and two outputs, one block generates the sum output and the other generates the carry output.
It contains 28 Transistors.
The carry output is generated using the expression 
                                                          Cout = A.B + Cin.(A+B).
The pull-down network of carry block with three inputs consisting of only NMOS is designed based on CMOS logic and the pull-up network consisting of only PMOS will be exact mirror image of the pull-down network. The output obtained will be in inverted form (Cout)’ which will be fed to CMOS inverter to obtain the Cout.
The sum output is generated using the expression
                                                      Sum = A.B.Cin + (Cout)’.(A+B+Cin).
The sum output can be obtained using the inverted Cout obtained from previous carry block which reduces the number of transistors in the circuit. The pull-down network of sum block with four inputs consisting of only NMOS is designed based on CMOS logic with (Cout)’ as fourth input and the pull-up network consisting of only PMOS will be exact mirror image of the pull-down network. The output obtained will be in inverted form (Sum)’ which will be fed to CMOS inverter to obtain the Sum.
Note:The inverters shown in the block diagram beloware directly included in the respective Sum block and the Carry block.
# Block Diagram
![image](https://user-images.githubusercontent.com/100398507/155660871-aa7117ce-e985-414c-a283-6d025d51edcf.png)
# Reference Circuit Diagram
![image](https://user-images.githubusercontent.com/100398507/155661075-bff4d68a-5d98-4c95-b5b5-e51609a39a95.png)
# Reference Circuit Waveforms
![image](https://user-images.githubusercontent.com/100398507/155661181-18493962-3752-4a6e-bb0b-422d8619e7ea.png)
# Tools used
1) Synopsys Custom Compiler: Custom Compiler™ is a fresh, modern solution for full-custom analog, custom digital,
and mixed-signal integrated circuit (IC) design.Custom Compiler provides a highly productive environment for design entry
and simulation, with strong features for mixed-signal design, debug, simulation
management, analysis, and reporting.All the schematics and blocks used in this circuit are designed using this tool
2) Synopsys PrimeWave: PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. All the simulations of this project is done using this tool.
3) Synopsys 28nm PDK: All the components used in the circuit design is utilised from this PDK
# Simulation in Synopsys
# Carry Block
![Carryschematic](https://user-images.githubusercontent.com/100398507/155667781-fd7fb72b-598e-4b7c-a8f6-73b1d528c257.png)
Fig.1: Carry Block Schematic

![Carrysymbol](https://user-images.githubusercontent.com/100398507/155667815-d5b2f597-e07a-4115-b6d1-1e104499a803.png)
Fig.2: Carry Block Symbol
# Sum Block
![Sumschematic](https://user-images.githubusercontent.com/100398507/155668311-e8b91060-e7ea-4a4d-8631-9db793151c4e.png)
Fig.3: Sum Block Schematic

![sumsymbol](https://user-images.githubusercontent.com/100398507/155668370-a78a676a-e58d-4e42-a403-5d0f282a7f95.png)
Fig.4: Sum Block Symbol
# Full Adder Implementation
![fulladderschematic](https://user-images.githubusercontent.com/100398507/155669418-3cdd61e0-e87f-426b-bc50-53ff8a11e6a1.png)
# Parameters set for Voltage Input A
![inpA](https://user-images.githubusercontent.com/100398507/155671972-50584ba5-239b-4400-870c-c0c427e379d4.png)

# Parameters set for Voltage Input B
![INPB](https://user-images.githubusercontent.com/100398507/155672013-577dfc85-4c2d-4849-ae77-cb46e8d94806.png)

# Parameters set for Voltage Input C
![INPC](https://user-images.githubusercontent.com/100398507/155672032-913849d1-3c10-48e5-8ea0-1b827af05cbd.png)

# Parameters set for Voltage Vdd
![INPVDD](https://user-images.githubusercontent.com/100398507/155672055-4aa3ad3c-9059-4cbd-9c59-78a4d391440a.png)

# Transient Settings
![TRANSANALYSIS](https://user-images.githubusercontent.com/100398507/155672668-9069fb8b-33be-487a-9dbc-98dca203d154.png)

# Output Waveform
![outputwaveform](https://user-images.githubusercontent.com/100398507/155673142-be600d37-ff06-487c-8ddf-9e7de8e2b689.png)

# Netlist
![Screenshot (217)](https://user-images.githubusercontent.com/100398507/155674267-6ec34aa0-d175-4dbb-b07c-68a8070508ae.png)
![Screenshot (218)](https://user-images.githubusercontent.com/100398507/155674286-b06ba779-3f2e-4de2-a9ee-7c2ebc4e1bbc.png)

# Conclusion
The Reference circuit of 1-Bit Full Adder using CMOS mirror logic is successfully implemented using Synopsys tools and simulation waveforms are obtained. The obtained waveforms match with the reference waveforms

# Author
Darshan Datta Naik, RV College of Engineering, Bengaluru

# Acknowledgement

# References
1)Suresh Kumar, Paramasivam, “Energy efficient low-power full-adder by 65 nmCMOS”, Concurrency Computat Pract Exper. 2018;e4741. DOI: 10.1002/cpe.4741
2)Eli Lyons, Vish Ganti, Rich Goldman, Vazgen Melikyan and Hamid Mahmoodi,”Full-Custom Design Project for Digital VLSI and IC Design Courses using Synopsys Generic 90nm CMOS Library” Conference Paper, DOI: 10.1109/MSE.2009.5270834 ,Source: IEEE Xplore, August 2009
