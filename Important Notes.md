# Units are not provided for the below caps on the schematic, the correct units are Pico Farad, NOT Micro Farad. 

Thank you to PancakePuppy for Saving my Ass.

C42 C43 - 27pF

C46 C47 - 100pF

These caps above are only required if you're using the Quartz oscillator. You do not need to install them if you are using the VCTCXO. 

# CY7C1019DV33 SRAM Chip


The main SRAM chip is designed in a socketed package, but it is generally surface mounted on this board, this can cause bad solder joints. 

If you are getting partial/no audio and evidence of corrupt DAB frames, validate the solder joints on the main SRAM, this will likely be your problem. The FPGA can appear to be fully functional with this problem happening and the only problem be the lack of audio, trust me, check the main SRAM! 
