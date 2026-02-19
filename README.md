# EasyDABv2
Repository of Plain-English Information for Sergiy's EasyDABv2 DAB Exciter Board. This is not to be confused with the EasyDABv1 which is a USB-based DAB exciter board. The USB DAB Board requires a computer to handle modulation while the v2 board utilizes a FPGA for independent operation.

# Introducton
First off, much of this is not my original work, credit goes to Sergiy for the design and release of the EasyDAB board. His site can be found here: https://tipok.org.ua/node/46

Secondly, this is a repository of the information I've learned through trying to manufacture one of these boards myself in order that folks in the future have an easier time with it than me.
There are a couple of issues with the original release of this board, firstly, I have not been able to find a license or any information regarding copyright of this board. Given that this was done in collaboration with the OpenDigitalRadio group, it is assumed that the board was released under similar licensing to the other projects under OpenDigitalRadio, that is permitting deriative work which is also licensed under the GPL and with credit to the original creator. 

If the above is not correct and the board was released under a more restrictive license, please get in touch at hoosk@retrohoosk.tv and this repository will be updated as such. That being said, under no circumstances will documentation of my own making be removed that was created based on information that is publicly available. 

# Aims
As mentioned in the introduction, the information is somewhat sparse on how to go about creating one of these boards. The original release was an Eagle PCB project coupled with a release of the firmware for flashing the board. The rest is left up to the individual to 'figure it out' (tm). 

As I'm a believer in easy, accessible and transparent documentation railing against those that insist on spoon-feeding being a bad thing, I have determined to document my findings and provide as much information as possible regarding the manufacture and configuration of these boards. 

So the aims of this project encompass the following:
1. Documentation


I will proceed to create an 'info dump' of all of my findings that I've learned through building this projects.

2. Photos


I will proceed to create high-resolution and detailed photos of both empty boards and fully assembled units so that others can see what these look like once assembled.

4. A fresh bill of materials.


The existing bill of materials leave too much up to assumption, therefore I will create a digikey cart and an Excel sheet of components required including example part numbers. It is assumed that components over time will be obsoleted and substitutes will be required, hence specification of components will be detailed as possible.

5. Board redesign.


The existing board requires redesign, solder pads overlay over existing component lables, requiring continuous reference to the PCB layout in CAD during assembly. This leaves opportunity to mistake and damage of expensive components (I'm looking at that Analog Devices Digital Synthesiser!). The board also allows different options depending on whether you wish to use a Single Frequency Network, FM or Digital Radio Mondiale usage, whether to use the mini360 modules and whether to use the band-pass filter. Given that there is little need for this board to be compact, outside of manufactoring costs, additional space can be used to make component locations clearer to the average hobbyist.

# Contact
Questions and Comments can be directed to hoosk@retrohoosk.tv , I'd love to hear your experience with assembling one of these boards and other ideas for this repo. 
