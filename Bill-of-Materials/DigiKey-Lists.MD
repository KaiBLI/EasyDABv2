# DigiKey Parts Lists

# DAB Board Main

The ICs have been separated from the passives as you may wish to source the ICs from a cheaper source than DigiKey, FPGAs and DACs can be found on eBay for a significant discounts, but come with the added risk of being non-genuine parts. 

Essential ICs (FPGA/DAC/Main SRAM/Ethernet Controller): https://www.digikey.com/en/mylists/list/T6NBFB3ZXT

Essential Components: https://www.digikey.com/en/mylists/list/4SKKTAJE6A

Essential RJ-45 Jack: The HR911105A RJ-45 Jack does not appear to be available on DigiKey, you will need to source it elsewhere. Here's an example listing: https://www.lcsc.com/product-detail/C12074.html

Essential DC-DC Converters - The Mini360 DC-DC Buck Converter required for 3.3v and 1.8v on the board does not appear to be available at DigiKey, but it can be found at many other suppliers such as Amazon, eBay and AliExpress, here's an example listing from RobotShop https://www.robotshop.com/products/mini-360-dc-dc-buck-converter .

# SRAM Option (Strongly Recommended)
23LC1024 SRAM: https://www.digikey.com/en/mylists/list/1WGT9OCI7E

# DAC Oscillator Options (One of Two of the Below is Required)

TC Oscillator (Strongly Recommended): https://www.digikey.com/en/mylists/list/RGXW9F6W7X

Quartz Oscillator: https://www.digikey.com/en/mylists/list/ATKNHPW9MJ

# Filtering Options (One of Two of the Below is Required)

Low Pass Filter (Needed for EasyFM/EasyDRM - Harder to Install): https://www.digikey.com/en/mylists/list/UZGJUMNWCD

Band Pass Fiter (Only Supports DAB Band III Frequencies - Easier to Install): https://www.digikey.com/en/mylists/list/YETD7D4YD4

# GPSDO Option (Only needed for SFN)

IF you wish to use SFN, you will need at least two EasyDAB boards configured with a TC Oscillator, additional SRAMs and the GPSDO module. 
GPSDO: https://www.digikey.com/en/mylists/list/PNWZ96SRTK

