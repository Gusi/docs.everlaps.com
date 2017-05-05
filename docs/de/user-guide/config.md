## &fa-gears; Konfiguration

Allows configuring general application parameters.

## Optionen der Konfiguration

--- 

#### &fa-microphone; Stimmen

Everlaps benötigt für vollen Funktionsumfang die Installation synthetische Stimmen *TTS (Text To Speech)*. Zwei der bekanntesten Anbieter sind *Ivona* und *Loquendo*, darüberhinaus kann Everlaps mit jedem *TTS* SAPI5 kompatiblen System zusammenarbeiten.

- **Erststimme/Zweitstimme**: Allows selecting the desired voice among those available in the system. For a better experience a female voice is recommended as primary, and a male voice as secondary (Marianne und Hans mit Ivona, oder Kate and Simon mit Loquendo).

- **Geschwindigkeit**: der Schieberegler steuert die Geschwindigkeit der einzelnen Stimmen. Je nach Stimmbild sollte durch justieren und Testen das Stimmenverhalten angepasst werden.

- **Lautstärke**: der Schieberegler steuert die individuelle Stimmlautstärke der Ansagen.

- **Test**: jeder hier eingegebene Text wird nach drücken der ENTER Taste automatisch ausgegeben. *diese Funktion ist nicht nur zum Testen wichtig sondern auch sehr nützlich für Ansagen über die Streckenlautsprecher*.

- **Stimm-Kompatibilitätsmodus**: aktiv  ***nur*** wenn anderweitig keine Stimme zu hören ist. *siehe weiter unten*.

	!!! Achtung !!! "Stimmkompatibilität: Loquendo 6.5"
		bei älteren Versionen von Loquendo (6.5 oder früher) gibt es einen Fehler bei der Sprachkontrolle durch Drittprogramme wie Everlaps. Nur in diesem Fall sollte der *Stimm-Kompatibilitätsmodus* aktiviert werden. 
	
		Dieser Fehler kann getestet werden, indem man die entsprechende Loquendo-Stimme auswählt und in der Testbox folgendes schreibt:
	
			Eins <Stille msec="1000"/> Zwei
	
		Wenn Sie hier *Eins Zwei* mit einer 1 Sekunde Pause dazwischen hören, ist der Fehler nicht vorhanden und die Auswahl des Kompatibilitätsmodus ist nicht notwendig; Wenn nur *Eins* gehört wird, dann ist es notwendig, den *Stimm-Kompatibilitätsmodus* zu aktivieren.
---

#### &fa-bell-o; Töne

Jeder Systemklang kann durch diesen Regler einzeln entsprechend den Bedürfnissen eingestellt werden.

- **Überfahrt**: erklingt bei einer gültigen Überfahrt über die Meßschleife (außer wenn es das Fahrzeug das des Führenden ist oder wenn der Lauf beendet ist)

- **Führender**: Wenn das Fahrzeug mit den meisten Runden die Ziellinie kreuzt, wird ein intensiverer Klang ausgegeben, der dem Rennleiter und dem Publikum helfen kann, zu erkennen wer der Fahrer mit den meisten Runden ist. 

	!!! note ""
		In einem * Finale * ist der Sound vom Führenden gleichbedeutend mit dem des schnellsten Fahrers.
	
		In a *qualifying heat*, Since each driver carries their own chrono, it does not imply that the driver is in the lead, only who is across the finishing line first.

- **Lauf Start/Lauf Ende**: signalisiert den Start bzw. das Ende des Laufes.

	!!! beachte ""
		In einem * Finale * bedeutet der Laufstart-Sound im Allgemeinen den Beginn der Zeitmessung. Der Klang für das Laufende signalisiert jedoch, dass für alle Fahrzeuge nach ihrer DARAUFFOLGENDEN Überfahrt der Mess-Schleife der Lauf endet.
	
		In eine * Vorlauf * signalisiert der Laufstart-Sound dass die Strecke offen ist - aber die Zeitmessung erfolgt erst wenn der erste Fahrer die Mess-Schleife überfährt. Der Klang für das Laufende signalisiert NICHT das allgemeine Laufende sondern die Phase des individuellen Laufendes. Das Rennen wird fortgesetzt bis jeder Fahrer entsprechend seiner Rennzeit eine persönliche Ankündigung des Laufendes gesagt bekommt. (Bsp: Max fertig...) 

- **ungültige Trasponder**: wird ausgegeben wenn eine Überfahrtmit einem Transponder erkatt wird der zu keinem Fahrer im aktiven Rennen zugeordnet werden kann.

---

#### &fa-bolt; Transponder

Das System unterstützt verschiedene Transponder und ihre Decoder-Systeme

- **Decoder/Parametes**: Ermöglicht die Auswahl des Decoders und seiner Verbindung. Die verfügbaren Optionen sind:

	- **IPDecoder**: Anschluss von AMB/MyLaps oder alternativen Decodern über das Netzwerk via IP-Protokoll. Im Feld ** Einstellungen ** istes erforderlich, die Decoder-IP-Adresse anzugeben (zB 192.168.0.10)

	- **seriellerDecoder**: Anschluss von AMB/MyLaps oder alternativen Decodern über die serielle Schnittstelle. Im Feld ** Parameter ** ist es erforderlich, anzugeben an welchem seriellen Port der Decoder angeschlossen ist (COM1, COM2, etc ...)
	
	- **SimulatorDecoder**: startet nach Auswahl und Programmneustart einen Überfahrts-Simulator im Zusatzfenster. Mit diesem Tool kann man testweise Fahrerüberfahrten erzeugen, indem man die entsprechenden Transpondernummern aktiviert und die Zeitspanne zwischen den Überfahrten konfiguriert. (beachte: auf die passende minimale Rundenzeit in den Einstellungen des Testlaufes achten) 
	
	- **NullDecoder**: wenn keine Decoderverbindung eingerichtet ist, wird mit dieser Einstellung keine Schnittstelle abgefragt.
	
- **Filter if hits/signal lower than...**: For connections to AMB/MyLaps devices, ignores crossings with hit/signal values lower than indicated.

- **Permits invalid transponders to start heat**: By defect only valid transponders are allowed to start heats that wait for the first crossing to start the chrono (generally qualifying is started with a rolling start). If this option is enabled, it will permit an invalid transponder to start the chrono. 

	!!! note ""
		Permits an invalid transponder to start the chrono, the invalid transponder can be assigned to a driver afterwards and all the laps (including the first crossing) can be recovered automatically; otherwise, the first crossing will not be registered (since the heat has not started yet) and could not be recovered.

- **Permit manual counting**: Enables the program's manual counting option, for counting crossings of drivers without transponders manually.

	- **Detect short cuts when manual counting**: If enabled short cuts will be detected in crossings when manual counting and these will not be counted as valid laps.

	- **Permit hot keys**: Allows the use of hot keys **F1 to F12** (drivers 1 to 12) and **Ctrl+1, Ctrl+2 to Ctrl+0** (drivers from 11 to 20) to generate manual counting without using the mouse in the lap screen of the active heat.

		!!! note "Hot Keys when manual counting"
			The keys F1 to F12 and all the combinations of Ctrl+NUM function including when Everlaps is not in the foreground.

---

#### &fa-print; Printing

- **Print total race time in lap results**: In heat reports, total race time is included next to the lap time in the chronological information for each driver.

- **Print graph with heat results**: In the heat reports, a graph will show the evolution of laps and standings for each driver over time.

- **Print automatically at the end of each heat**: When each heat ends, the heat results will be printed automatically, as well as the round results (in the case that the recently completed heat has finalised the round) and also the session results (if there are 2 or more rounds completed).

- **Use PDF viewer prior to printing**: When printing a report, it is opened with the default operating system PDF viewer ([Foxit Reader](http://www.foxitsoftware.com/Secure_PDF_Reader), [Adobe Reader](http://get.adobe.com/es/reader), etc...) instead of the printer.

- **Printer**: Selects the system printer which the reports are sent to, as long as the *Use PDF viewer prior to printing* is not enabled.

---

#### &fa-gear; Default options

- **Prologue/minimum lap/last lap/Delayed chrono time/Delayed launched start**: The values introduced in these fields are automatically assigned to new races that are generated by the program. Each field corresponds to a similar one in [Race configuration](../race-formats/qualify-finals/index.html#comun)

- **Invert numbering of practice and qualifying series**: By default the series where each diver has an individual chrono are numbered from 1 on-wards, 1 being the series which contains the drivers of higher ranking and is scheduled to run last in the round. If this option is enabled, The qualifying series are numbered reverse order (series 1 will contain the drivers of least ranking and will be scheduled to run in first).

	!!! note ""
		The order of the heats execution in Everlaps does not need to be strictly followed and the time keeper can choose which heat from the current round to launch in each moment.

---

#### &fa-signal; Network

- **Publish results automatically in  everlaps.com**: When each heat finishes, the results are updated in [Everlaps](http://everlaps.com) as long as the *Web code* has been introduced that corresponds to that in the race configuration.

	!!! note ""
		Once the heat has finished and corrections or penalties are applied to the race, it will be necessary to re-publish the race results manually (List of races > Right click > Publish results in everlaps.com)

---

#### &fa-rss; Live Timing 

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

#### &fa-database; Files

- **Database**: Shows the path to the application file where all the driver and races are stored. This file can be moved between machines, for example to configure a race on another computer (including on the freeware version), to copy the database to the track computer to start the race immediately.

- **Logotype**: Allows showing a personalised logotype at the top of the reports.

---

#### &fa-globe; Language

Allows changing the interface language and announcements of Everlaps

!!! note ""
	The voices will need to be configured in the same language as that is established for the program.

---

#### &fa-bug; Debugging

- **Show Console**: Shows the programs logs (voice announcements, actions, errors...). In case of problems, it can be useful to try and understand what has happened following the programs back-trace.


## Classes and tags 

![Classes and tags](../img/classes-tags.png)

#### &fa-list; Classes

Allows adding, deleting and modifying classes. By default a list of the most common classes is created, These can be modified at will, the only restriction being that the default class cannot be removed.

#### &fa-list; Tags

Allows adding, deleting and modifying tags, assigning an identifying colour as well as a description.

The use of tags is explained in detail in the [Tags](../common-tasks/tags/index.html) section.
