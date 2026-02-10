# EasyDAB Assembly Options

With the EasyDAB v2 you have a couple of assembly options, most hobbyists looking to dabble into DAB will probably want to start off with the 1st Option

# 1. EasyDAB v2 with RBP Band Pass Filter using Mini360 Modules without Single Frequency Network support.

This is perhaps the most straightforward option for assembly. A dedicated Bill of Materials will be provided for this option.

Each EasyDAB board requires two Mini360 DC-DC step-down buck converter modules. The Mini360 takes an input voltage of 4.75v-23v and can output between 1.0v-17v. The output is both determined by the input voltage and the configuration of the potentiometer located on the board.
The EasyDAB will supply both boards with 5v, but each needs to be configured for different output voltages. 

The Mini-360 Module closest to the DC Barrel Jack with IC11 labelled on the PCB must output 3.3v (Potentiometer configured for 21.5kOhm), while the Mini-360 module closest to the RF_OUT with IC10 labelled on the PCB must be configured for 1.8v output (Potentiometer configured for 7.87kOhm). It is advisable to run in 5v with a dummy load on the board's output and ensure that the potentiometers are configured for the correct output voltages BEFORE installing on the board. 
