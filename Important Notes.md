# Noise on EasyDABv2 Cold Start
The current schematics have an issue which causes a lot of noise on cold-start which require a 2K Ohm resistor bodge. Please see here for more info: https://tipok.org.ua/node/56 - It is warned that you will burn out your output amplifier if you do not address this.


# Units are not provided for the below caps on the schematic, the correct units are Pico Farad, NOT Micro Farad. 

Thank you to PancakePuppy for confirming values.

C42 C43 - 27pF

C46 C47 - 100pF

These caps above are only required if you're using the Quartz oscillator. You do not need to install them if you are using the VCTCXO. 

# CY7C1019DV33 SRAM Chip


The main SRAM chip is designed in a socketed package, but it is generally surface mounted on this board, this can cause bad solder joints. 

If you are getting partial/no audio and evidence of corrupt DAB frames, validate the solder joints on the main SRAM, this will likely be your problem. The FPGA can appear to be fully functional with this problem happening and the only problem be the lack of audio, trust me, check the main SRAM! 

This part is End-of-Life, so it may become difficult to acquire in the future. 

# C76 Charge Pump Capacitor

If you have elected to use the VCTCXO instead of a standard Quartz Oscillator, contrary to popular belief the relatively expensive charge pump capacitor is not required for the board to operate correctly if you are not using SFN. It has not been tested without being present when configured for SFN. Please report in if you have had success without the charge-pump cap with SFN. 
