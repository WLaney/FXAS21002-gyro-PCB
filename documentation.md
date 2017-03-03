# FXAS21002 Breakout

This board was designed by William Laney as part of the College of William and Mary's physics undergraduate research, 2016. 
Questions or concerns can be directed to William Laney at welaney@email.wm.edu

This is a breakout board for the FXAS21002 IC. The FXAS21002 is 3-axis digital gyroscope. The chip can use the I2C or SPI communcication proticals, however only I2C has been broken out, SPI has been disabled. The I2C address for this chips is 0x20 in hex (100000 in binary).

The board is designed to be stackable with the Sparkfun MMA8452 breakout board. To allow for this functionality, two unused header pin holes have been added between the SCL and ground pins.

Printed on the board's silk screen are labeled arrows corresponding to the positive direction of rotation for each axis. These arrows show the direction towards which the board must rotate to register a positive rotation on a given axis.

One interupt line has been broken out form the chip, it corrospons to Interupt 2 on the data sheet.

The reset input, RST_B is unused and has been connected to voltage with a pull up reistor. This resistor is optional, but was inclued in this desgine.

The large white dot on the silkscreen in the area for the chip corresponds to a dot on the same location on the physical chip package, and assures that the chip is attached to the board with the proper orientation.

 Both the bottom and top layers of this board contain ground pours to insure proper grounding and to mimize noise and interfence between signal traces.

All traces on this board are 0.01" and the vias have 0.02" drill holes. This is more than sufficient to handle the current through the traces. Right angles in the trace are avoid to help ensure data integrity.

Decoupling capacitors were added as near to the chips as possible to minimize noise to the chips. This is detailed in the relevant data sheets.

10k pull up resistors were used on the I2C data lines. This value is larger then recomended in the data sheet. These larger values were choosen both to help lower the current of the device and maintain compatablity with the other I2C devices used in the sharkduino system. These data lines need to be examned after the board is produced to insure that they are getting enough current to be properly pulled high.

0805 package size is used for all passive components. This size was selected because I believe it to be a good compromise between size and ease of placement.

On October 28, 2016 three boards were ordered from OSHpark for \$1.85. This corresponds to \$0.62 per board.

## Assembily Information

Assemblie steps:
(please note that these steps represent what I beilive to be the optimal order of operations. They may not be. Addionaly not all boards were assembled in this way as I expermented with the order)

1. Applie solder paste for FXAS21002C
2. Applie solder past for passive components
3. Place FXAS21002C
4. Place passive components
5. Place full board into solder reflow oven
6. Wipe down with isopropal alchohal 
7. Check if board is shorted between GND and VCC

## Notes/Feature Requests

*this information is subject to change with as more boards are assembled*

I2C adress read as 0x21 not 0x20 as expected on one board, the reason for this is currently unkown. Chances are there was some bad soldering.

10k pull up resisotrs appear to not be a problem.

