# EasyDAB Assembly Options

With the EasyDAB v2 you have a couple of assembly options, most hobbyists looking to dabble into DAB will probably want to start off with the options installing the Mini360 modules, the RBP-204+ band pass filter and electing to -not- install the SFN components.

# 1. The Mini360 Modules

The Mini360 Modules are a convenient way of obtaining required voltages for the EasyDAB v2 board to work. However, one may desire to forgo the Mini360's to instead directly solder on the required circuitry directly on the board to acheive the required voltages. If you utilize the BoM from the Eagle Project, you will have components included on that BoM that are only needed if you are going the route to directly solder the DC-DC components to the board.

Each EasyDAB board requires two Mini360 DC-DC step-down buck converter modules. The Mini360 takes an input voltage of 4.75v-23v and can output between 1.0v-17v. The output is both determined by the input voltage and the configuration of the potentiometer located on the board.
The EasyDAB will supply both boards with 5v, but each needs to be configured for different output voltages. 

The Mini-360 Module closest to the DC Barrel Jack with IC11 labelled on the PCB must output 3.3v (Potentiometer configured for 21.5kOhm), while the Mini-360 module closest to the RF_OUT with IC10 labelled on the PCB must be configured for 1.8v output (Potentiometer configured for 7.87kOhm). It is advisable to run in 5v with a dummy load on the module's output and ensure that the potentiometers are configured for the correct output voltages BEFORE installing on the module. 

**Direct Solder Pads**
For reference the Mini360 direct-solder pads are labelled as follows, if you plan to use the Mini360 modules rather than direct solder you can exclude the below components from your bill of materials:


_DC Side (5v Input - 3.3v Output)_

C31 0.1uF

C32 4.7uF

C70 10uF

C71 10nF

C72 100nF

C73 22uF

R27 6.8K

R28 6.8K

R29 8K2

R30 21.5K

R31 (Potentiometer) 10-100K

L8 10uH

IC11 MP2307

_RF Side (5v Input - 1.8v Output)_

C68 22uF

C67 100nF

C65 10uF

C66 10nF

C64 3.9nF

R24 6.8K

R25 8K2

R26 7.87K

R27 (Potentiometer) 10-100K

L7 10uH Inductor

IC10 MP2307 DC>DC


# 2. Band Pass Filter / Low Pass Filter

The band pass filter is perhaps the easier option for acheiving RF filtering of the outputted signal. RF filtering is essential if you are using the EasyDAB board outside of a RF shielded box. This is because an unfiltered signal will spread RF harmonics all over the spectrum potentially interfering with licensed services and other lawful users of the RF spectrum. You could get in significant trouble with the associated regulatory bodies in your country if you do not filter your signal! However, there are three options to acheive RF filtering. You can either use the RBP-204+, the RBP-220+ or a set of passive componenets. The below covers the advantages and disadvantages of these options.

**RBP-204+**

_Advantages:_

Covers RF filtering for the entirety of the DAB Band III spectrum of 174Mhz-240Mhz. 

Probably acheives the cleanest signal possible.

Easier than using the series of passive components.


_Disadvantages:_

Expensive Component

Out-of-stock at some suppliers

Needs to be swapped for a different RF filtering option if you decided to change the board to be used for FM or DRM usage.


**RBP-220+**

_Advantages:_

Possibly easier to source than RBP-204+

Easier than using series of passive components.


_Disadvantages_

Does not cover entirety of DAB Band III, only covers to 212Mhz-240Mhz

Needs to be swapped for a different RF filtering option if you decided to change the board to be used for FM or DRM usage.


**Inductors and Capacitors / Low Pass Filter**

One can forgo the RBP-204+/RBP-220+ and instead install a series of capacitors and inductors at the locations of L1, L5 and L6, and C63, C62, C61 and C60. 

This may(?) acheive a lesser quality of filtering, however has the advantage of utilizing cheaper components. Additionally, if one wishes to use the EasyFM firmware, this should work for that too. (This I have not been able to test, Sergiy's site only mentions the usage of low pass filtering instead of band pass filtering for EasyFM - I ASSUME that references the circit diagram of using the inductors/capacitors)

_Advantages:_

Easiest and cheapest components to source

Works for EasyFM(tbc)


_Disadvantages_

Possibly lesser quality of filtering

More soldering and quantity of components to source


# 3. Single Frequency Network (SFN)
The EasyDAB v2 board allows you to use multiple boards to create a single frequency network of transmitters. That is you can extend your range by broadcasting the same multiplex on the same frequency over a distributed area. However, for this to work, all the ones and zeros must be sent out of all the transmitter in perfect synchronization. To acheive this, a GPS module is used to timestamp frames allowing the transmitters to broadcast said frames at the same time. 

Most folks who are looking to build microtransmitters within their own home or properties will most likely not need this. You will probably have an easier time boosting the power of your signal to acheive the desired range rather than needing to go down the SFN tunnel. However, if you are restricted by power limitations on restricted license/no-license regulations from your jurisdiction, you may find SFN useful as the regulations may be silent on the -quantity- of transmitters on the same frequency as such regulations usually only stipulate power of individual broadcasts. 

Using the design of Sergiy's board, you can initially build for non-SFN usage and later upgrade to the components needed for SFN at a later date if desired. 
