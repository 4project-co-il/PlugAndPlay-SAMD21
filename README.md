# PlugAndPlay-SAMD21
This is the repository with the files for Plug-n-Play SAMD21 Development Board.

The Plug-n-Play system is an arduino-based environment that allows easier connections between the parts
and intends to create a more "product-like" projects with permanent connections, compared to a breadboard.

Plug-n-Play parts do not require any soldering to connect. Just plug the cable to the connectors and you are ready to go.
In the worst case, you might need to tighten few screws on a terminal block.

All the parts in the Plug-n-Play system communicate via I2C protocol. 
The connectors between the parts have 6 lines: 2 lines to provide the power (VCC and GND), 2 lines for the I2C communication and additional 2 lines for the interrupts.
The interrupts are handled by the Event Based Framework ([EBF](https://github.com/4project-co-il/EBF)) in the background. No polling is needed in the software.
A button pressed? Even function will be called in your code to handle that change.

Using the interrupts allows creation of very low-power projects, as well as controllers with fast responding to changes.

No need to worry about the correct wires connection, accidental inversion I2C lines, or even worse, the VCC and GND.
No need to worry about the I2C addresses as well. Pull-up resistors if you connect few parts in serial, are those needed or not?
What port should I connect the part? Is is PWM complatible? No more wories like that.
Just plug the connectors and start playing with the code. As easy as that.

Communication is not the only thing handled by the PnP system. Power distribution is easily managed as well.
Need to have a 12V relay, 5V servo and 3.3V for the logic? No problem at all...
Plug the power cables between the parts, add needed regulator to the board and you're done.

The board is manufactured by the [4project.co.il](https://www.4project.co.il/).\
You will need the Event Based Framework ([EBF](https://github.com/4project-co-il/EBF)) to program the board.
