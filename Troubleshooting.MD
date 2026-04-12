Troubleshooting
=====

# Stuttering Audio / Corrupted DAB Stream

Check that the Main SRAM is properly soldered, poor solder joints will cause stuttering and cutting out audio. This is especially the case if you find that it improves/gets worse if you move the board. This will also manifest as Frame errors in the DAB stream when using Welle.io.

# No PLL Lock LED / Status in Config Page shows Unknown 00

Ensure that the 0Ohm Resistor at R20 is populated. This provides 3v3 to the DAC via IC5 and is required for the DAC to operate. 
Ensure that Oscillator is correctly installed and configured. If using the VCTCXO oscillator must be set to 19.4Mhz in the EasyDAB configuration, if using the non-VCTC Oscillator, then it must be configured for 24.576Mhz. The VCTCXO is polarized, ensure it is correctly orientated, if it is hot to touch, it has been installed the wrong way around. 
The OOhm Solder Pads R32/R33 are jumpers to specify which oscillator to use, if using the VCTCXO bridge R33, if using non-VCTCXO bridge R32. 

# No RF Output

Verify that IC7 has a voltage, and is correctly soldered. If using the Band Pass Filter, verify solder connections as they can easily be missed due to the solder pads for the component largely being on the bottom of the filter.
Check and replace the Low-Noise Amplifier IC7. 

# Booting LED stays on

If the Booting LED stays lit, the FPGA has not picked up the EasyDAB core. Verify your SPI flash is correctly programmed and replace if needed. 

# ETI Wait Light ocassionally flashes solid/bright and RF drops

The buffer for the EasyDAB is not sufficient to maintain a stable output. Install additional SRAMs for the extra buffer. 

# ETI Wait Light Dimly Flickers
This is normal operation and indicating that the EasyDAB is processing an active ETI/ZMQ Stream. This is expected behavior on the 2017 firmware, but is not present on earlier firmwares.

# SFN and ODR-DabMux 

ODR-DabMux does not support EasyDAB's SFN after version 2.3.1, however later versions work fine if you are NOT using SFN. As far as I know this is due to ODR-DabMux changing how it handles creating timestamps of data allowing multiple EasyDABs to stay in sync. 

# FIR Clipped Indicator/ iFFT Overflow Happened

I have no idea what this is warning about, but it does not appear to impact operation. 
