## Quick start

Here are described the basic steps to install and start a race in Everlaps. For more Detailed information see the rest of the documentation.

---

### Basic actions

1.  Input the driver data in [&fa-users; **Drivers**](./user-guide/drivers/index.html)

2.  Create a new race in [&fa-road; **Races**](./user-guide/races/index.html), configure general and [&fa-flag; **Session**](./race-formats/qualify-finals/index.html) options

3.  Register participating drivers in [&fa-user; **Registrations**](./user-guide/races/index.html#inscripciones)

4.  &fa-check-circle; **Generate** and &fa-print; **Print** driver series in [&fa-th; **Series**](./user-guide/races/index.html#series)

	*Returns here at the end of each session to generate the series for the next. For example, to generate finals series after completing qualifying*

5.  &fa-check-circle-o; **Confirm** The drivers series in [&fa-th; **Series**](./user-guide/races/index.html#series)

	*The race Heats are generated*

6.  [&fa-upload; **Activate**](./user-guide/heats/index.html#mangas_1) and start ([&fa-check-circle; **Start**](./user-guide/heats/index.html#control-de-la-manga-activa)) The heats one after another in [&fa-clock-o; **Heats
**](./user-guide/heats/index.html)

7.  Penalise and correct if necessary, and &fa-print; **Print** the results

---

### Installation of program

System requirements

- Windows Vista / 7 / 8 / 10

- Microsoft .NET Framework 4.5 or above

- Text to speech compatible with SAPI 5 (Ivona, Loquendo, ...)

- Decoder compatible with AMB/MyLaps with Serial or Ethernet connection

- Recommended: PDF file reader ([Foxit Reader](http://www.foxitsoftware.com/Secure_PDF_Reader/), [Adobe Reader](http://get.adobe.com/reader/), ...)

!!! Warning "Windows energy saving options"
	During timing it is important that all the computers energy saving options are turned off (suspend, hard disk drive idle, etc...), as these can interrupt the proper working during periods of inactivity.  

---

### Installing the voices

Requires the installation of a text to speech module (The cost is not included in the Everlaps license). The recommended is [Ivona](http://www.ivona.com).

Once the voices are installed they can be selected in [&fa-gear; **Configuration options**](./user-guide/config/index.html)

---

### Connecting the decoder

Connect the amb/MyLaps decoder to the computer following the instructions provided by the manufacturer. 

Depending on the type of connection, the correct values will need to be configured in [&fa-gear; **Configuration options**](./user-guide/config/index.html)

- Serial connection: input the computers serial port that the decoder is connected to (COM1, COM2, ...)

- Ethernet connection: input the decoders IP address (example: 192.168.1.2)


!!! warning "(Ethernet) cable connection"
	
	- If you connect the decoder directly to a computer, it is possible that you will need a [crossover cable](https://en.wikipedia.org/wiki/Ethernet_crossover_cable). If there is a switch or router in the middle it will not be necessary.
	
	- The decoder and the computer must be on the **same subnet** (for example if the computer is 192.168.0.1 and the decoder is 192.168.0.2). If you cannot get the connection to work you may need to disable automatic DHCP on the decoder and input a static IP manually on the LCD screen of the decoder.
	
	
	
