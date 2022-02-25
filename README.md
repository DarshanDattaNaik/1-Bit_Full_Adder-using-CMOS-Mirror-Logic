# 1-Bit_Full_Adder-using-CMOS-Mirror-Logic
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
