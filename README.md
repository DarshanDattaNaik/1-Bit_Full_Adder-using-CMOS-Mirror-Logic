# 1-Bit_Full_Adder-using-CMOS-Mirror-Logic
# Abstract
Adders are one of the main components of majority of circuits and find their application in ALU’s, microprocessors, DSP processors.1-Bit Full adder can be used to implement other circuits such as Ripple Carry Adder, Multipliers. A 1-bit full adder using CMOS mirror logic is designed and implemented in this repository. The implementation will be done in 28nm technology node using Synopsys tools. The reference waveforms will be verified with actual waveforms obtained from simulation.
# Reference Circuit Details
A one bit full adder has two circuit blocks, with three inputs and two outputs, one block generates the sum output and the other generates the carry output. 
The carry output is generated using the expression 
                                                          Cout = A.B + Cin.(A+B)
The pull-down network of carry block with three inputs consisting of only NMOS is designed based on CMOS logic and the pull-up network consisting of only PMOS will be exact mirror image of the pull-down network. The output obtained will be in inverted form (Cout)’ which will be fed to CMOS inverter to obtain the Cout.
The sum output is generated using the expression
                                                      Sum = A.B.Cin + (Cout)’.(A+B+Cin)
The sum output can be obtained using the inverted Cout obtained from previous carry block which reduces the number of transistors in the circuit. The pull-down network of sum block with four inputs consisting of only NMOS is designed based on CMOS logic with (Cout)’ as fourth input and the pull-up network consisting of only PMOS will be exact mirror image of the pull-down network. The output obtained will be in inverted form (Sum)’ which will be fed to CMOS inverter to obtain the Sum.
