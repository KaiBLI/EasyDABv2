# EasyDAB Assembly Options

With the EasyDAB v2 you have a couple of assembly options, most hobbyists looking to dabble into DAB will probably want to start off with the 1st Option

# 1. The Mini360 Modules

The Mini360 Modules are a convenient way of obtaining required voltages for the EasyDAB v2 board to work. However, one may desire to forgo the Mini360's to instead directly solder on the required circuitry directly on the board to acheive the required voltages. If you utilize the BoM from the Eagle Project, you will have components included on that BoM that are only needed if you are going the route to directly solder the DC-DC components to the board.

Each EasyDAB board requires two Mini360 DC-DC step-down buck converter modules. The Mini360 takes an input voltage of 4.75v-23v and can output between 1.0v-17v. The output is both determined by the input voltage and the configuration of the potentiometer located on the board.
The EasyDAB will supply both boards with 5v, but each needs to be configured for different output voltages. 

The Mini-360 Module closest to the DC Barrel Jack with IC11 labelled on the PCB must output 3.3v (Potentiometer configured for 21.5kOhm), while the Mini-360 module closest to the RF_OUT with IC10 labelled on the PCB must be configured for 1.8v output (Potentiometer configured for 7.87kOhm). It is advisable to run in 5v with a dummy load on the board's output and ensure that the potentiometers are configured for the correct output voltages BEFORE installing on the board. 

#2. The Band Pass Filter
The band pass filter is perhaps the easier option for acheiving RF filtering of the outputted signal. RF filtering is essential if you are using the EasyDAB board outside of a RF shielded box. This is because an unfiltered signal will spread RF harmonics all over the spectrum potentially interfering with licensed services and other lawful users of the RF spectrum. You could get in significant trouble with the associated regulatory bodies in your country if you do not filter your signal! However, there are three options to acheive RF filtering. You can either use the RBP-204+, the RBP-220+ or a set of passive componenets. The below covers the advantages and disadvantages of these options.

RBP-204+
Advantages:
Covers RF filtering for the entirety of the DAB Band III spectrum of 174Mhz-240Mhz. 
Probably acheives the cleanest signal possible.
Easier than using the series of passive components.

Disadvantages
Expensive Component
Out-of-stock at some suppliers
Needs to be swapped for a different RF filtering option if you decided to change the board to be used for FM or DRM usage.

RBP-220+
Advantages:
Possibly easier to source than RBP-204+
Easier than using series of passive components.

Disadvantages
Does not cover entirety of DAB Band III, only covers to 212Mhz-240Mhz
Needs to be swapped for a different RF filtering option if you decided to change the board to be used for FM or DRM usage.
