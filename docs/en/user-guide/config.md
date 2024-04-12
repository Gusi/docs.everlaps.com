# :fontawesome-solid-gears: Config

Allows configuring general application parameters.

## Configuration options

--- 

#### :fontawesome-solid-microphone: Voices

Everlaps needs a voice synthesizer system *TTS (Text To Speech)* to be able to work. Two of the most well known are *Ivona* and *Loquendo*, although Everlaps can work with any *TTS* system that is SAPI5 compatible.

- **Primary/Secondary**: Allows selecting the desired voice among those available in the system. For a better experience a female voice is recommended as primary, and a male voice as secondary (Amy and Brian with Ivona, or Kate and Simon with Loquendo).

- **Speed**: Controls the speed of diction of the individual voices. Adjust at will according to chosen voices behavior.

- **Volume**: Controls the voices volume individually.

- **Test**: Allows the introduction of any text for the voice to pronounce when enter key is pressed. *very useful for making personal announcements on the track speakers*.

- **Voice compatibility mode**: enable  ***only*** if the voices stay silent. *See note further down*.

	!!! warning "Compatibility of voices: Loquendo 6.5"
		If an old version of Loquendo (6.5 o earlier) there is a bug in the voices that block the announcements due to an advanced use that Everlaps makes of voice control. Only in this case should *Voice compatibility mode* be selected. 
	
		This bug can be tested by selecting the corresponding Loquendo voice and writing the following in the test box:
	
			One <silence msec="1000"/> Two
	
		If you here *One Two* with a 1 second pause in between, the bug is not present and selecting compatibility mode will not be necessary: if only *One* is heard then it will be necessary to select it.

---

#### :fontawesome-regular-bell: Sounds

It is possible to adjust the volume individually for each systems sound according to the needs of the track.

- **Crossing**: Sounds when a valid crossing is detected across the finishing line (except if it is the vehicle with the most amount of laps, or if the heat has finalised)

- **Race leader**: When the vehicle with the most amount of laps crosses the finishing line, a sharper sound is received, which can help the race director and the public identify who is the driver with the most laps. 

	!!! note
		In a *final*, the race leader sound is equivalent to the first place driver.
	
		In a *qualifying heat*, Since each driver carries their own chrono, it does not imply that the driver is in the lead, only who is across the finishing line first.

- **Heat start/Heat finish**: Indicates start and finish of a heat.

	!!! note
		In a *final*, The heat start sound generally implies the start of the chrono. The heat finish sound implies that all the vehicles finish on their next crossing of the finish line.
	
		In a *qualifying heat*, The heat start sound indicates that the track is open, but the chrono will start when the first driver crosses first across the finishing line after the sound. The heat finish sound doesn't imply that all vehicles finish on their next crossing of the finishing line: the announcements will announce which vehicles have finished according to their individual chrono.

- **Invalid transponder**: Sounds when a crossing is made by a transponder that does not belong to a driver in the active heat.

---

#### :fontawesome-solid-bolt: Transponders

The system supports the connection to different lap counting systems.

- **Decoder/Parameters**: Allows selecting the decoder and or its connection. The available options are:

	- **IPDecoder**: Connection to AMB/MyLaps devices using a IP protocol connection (Connection via Ethernet cable). In the field **Parameters** It is necessary to indicate the decoders IP address (for example, 192.168.0.10)

	- **SerialDecoder**: Connection to AMB/MyLaps devices using serial port. In the field **Parameters** It is necessary to indicate which serial port the decoder is connected to (COM1, COM2, etc...)
	
	- **SimulatorDecoder**: Crossings simulator that allows testing the program by generating drivers crossings by clicking on the corresponding transponder buttons or by configuring it in automatic with a corresponding gap of time between crossings.
	
	- **NullDecoder**: No decoder connection is established.
	
- **Filter if hits/signal lower than...**: For connections to AMB/MyLaps devices, ignores crossings with hit/signal values lower than indicated.

- **Permits invalid transponders to start heat**: By defect only valid transponders are allowed to start heats that wait for the first crossing to start the chrono (generally qualifying is started with a rolling start). If this option is enabled, it will permit an invalid transponder to start the chrono. 

	!!! note
		Permits an invalid transponder to start the chrono, the invalid transponder can be assigned to a driver afterwards and all the laps (including the first crossing) can be recovered automatically: otherwise, the first crossing will not be registered (since the heat has not started yet) and could not be recovered.

- **Permit manual counting**: Enables the program's manual counting option, for counting crossings of drivers without transponders manually.

	- **Detect short cuts when manual counting**: If enabled short cuts will be detected in crossings when manual counting and these will not be counted as valid laps.

	- **Permit hot keys**: Allows the use of hot keys **F1 to F12** (drivers 1 to 12) and **Ctrl+1, Ctrl+2 to Ctrl+0** (drivers from 11 to 20) to generate manual counting without using the mouse in the lap screen of the active heat.

		!!! note "Hot Keys when manual counting"
			The keys F1 to F12 and all the combinations of Ctrl+NUM function including when Everlaps is not in the foreground.

---

#### :fontawesome-solid-print: Printing

- **Print total race time in lap results**: In heat reports, total race time is included next to the lap time in the chronological information for each driver.

- **Print graph with heat results**: In the heat reports, a graph will show the evolution of laps and standings for each driver over time.

- **Print automatically at the end of each heat**: When each heat ends, the heat results will be printed automatically, as well as the round results (in the case that the recently completed heat has finalised the round) and also the session results (if there are 2 or more rounds completed).

- **Use PDF viewer prior to printing**: When printing a report, it is opened with the default operating system PDF viewer ([Foxit Reader](http://www.foxitsoftware.com/Secure_PDF_Reader), [Adobe Reader](http://get.adobe.com/es/reader), etc...) instead of the printer.

- **Printer**: Selects the system printer which the reports are sent to, as long as the *Use PDF viewer prior to printing* is not enabled.

---

#### :fontawesome-solid-gear: Default options

- **Prologue/minimum lap/last lap/Delayed chrono time/Delayed launched start**: The values introduced in these fields are automatically assigned to new races that are generated by the program. Each field corresponds to a similar one in [Race configuration](../race-formats/qualify-finals.md#comun)

- **Invert numbering of practice and qualifying series**: By default the series where each diver has an individual chrono are numbered from 1 on-wards, 1 being the series which contains the drivers of higher ranking and is scheduled to run last in the round. If this option is enabled, The qualifying series are numbered reverse order (series 1 will contain the drivers of least ranking and will be scheduled to run in first).

	!!! note
		The order of the heats execution in Everlaps does not need to be strictly followed and the time keeper can choose which heat from the current round to launch in each moment.

---

#### :fontawesome-solid-signal: Network

- **Publish results automatically in  everlaps.com**: When each heat finishes, the results are updated in [Everlaps](http://everlaps.com) as long as the *Web code* has been introduced that corresponds to that in the race configuration.

	!!! note
		Once the heat has finished and corrections or penalties are applied to the race, it will be necessary to re-publish the race results manually (List of races > Right click > Publish results in everlaps.com)

---

#### :fontawesome-solid-rss: Live Timing 

Everlaps can transmit the heat results in *Real time* via a web server, which enables the possibility to visualise the course of the race on any device with a modern web browser, like smart-phones, tablets and computers.

That way drivers in the pits and the public around the track or at home can follow the race, the *Live Timing* system is specially useful in the hands of the race director, since it allows a direct view of the races state, including being able to start and stop the heat in course.

- **Publish a local server**: Enables sending the race data to a local server which is executed in the same computer where Everlaps is installed. *This is the only option available when executing the program in freeware mode*.

	!!! note "Local server"
		The local server is an independent program that needs to be running so that mobile devices can connect to Live Timing on the track WiFi. It can be found in the Everlaps folder, inside windows Program Files, as on the desktop, and is identified by a green icon labeled *Everlaps Live Timing*.
 
- **Publish to everlaps.com**: Enables the sending of data to [Everlaps Live Timing](http://live.everlaps.com) web site, beneath the title that is published on the main page of [Everlaps](http://everlaps.com) during the dates of the race.

- **Personal servers**: Allow sending to a different IP addresses or servers indicated in this box (separated by spaces).

- **Show refueling clocks**: Shows in [Live Timing](http://live.everlaps.com) (remotely and locally) a list of different refueling strategies and time remaining for each pit-stop.

	- **Minimum/maximum between refueling**: According to the duration of the race and the values introduced, corresponding to the time a that a vehicle can go without refueling, it generates the different refueling strategies.

- **Permits remote control**: Permits remote control of heats from a mobile device connected to the track local network. *This option is currently disabled in this version*.

	- **User/Password**: Fields that must be introduced in the *Live Timing* client to give permission for remote control to a user.

---

#### :fontawesome-solid-database: Files

- **Database**: Shows the path to the application file where all the driver and races are stored. This file can be moved between machines, for example to configure a race on another computer (including on the freeware version), to copy the database to the track computer to start the race immediately.

- **Logotype**: Allows showing a personalised logotype at the top of the reports.

---

#### :fontawesome-solid-globe: Language

Allows changing the interface language and announcements of Everlaps

!!! note
	The voices will need to be configured in the same language as that is established for the program.

---

#### :fontawesome-solid-bug: Debugging

- **Show Console**: Shows the programs logs (voice announcements, actions, errors...). In case of problems, it can be useful to try and understand what has happened following the programs back-trace.


## Classes and tags 

![Classes and tags](../img/classes-tags.png)

#### :fontawesome-solid-list: Classes

Allows adding, deleting and modifying classes. By default a list of the most common classes is created, These can be modified at will, the only restriction being that the default class cannot be removed.

#### :fontawesome-solid-list: Tags

Allows adding, deleting and modifying tags, assigning an identifying colour as well as a description.

The use of tags is explained in detail in the [Tags](../common-tasks/tags.md) section.
