## Vorläufe und Finale

![Vorläufe und Finale](../img/qualy-finals.png)

Das Rennformat * Vorläufe und Finale * definiert standardmäßig die Trainingssitzungen, Qualifikationen, Vorläufe und Finalsitzungen, die ersten beiden können entfernt werden, wenn sie nicht im Rennen eingesetzt werden.

---

##### allgemeines

- **Name**: Titel für das Rennen  der oben auf den Listen erscheint.

- **Beschreibung**: beschreibender Text der unten auf den Listen erscheint.

- **Typ**: beschreibt das Renn-Format, in diesem Fall *Vorläufe und Finale*.

- **Web Code**: notwendig um Livezeiten und Ergebnisse im [Everlaps-Portal](http://everlaps.com) zu veröffentlichen.

- **Klassen**: Identifiziert die Rennklasse damit der entsprechende Transponder bei einer manuellen Fahrerregistrierung gewählt werden kann.

---


##### Sprachansagen

- **Kurzname**: Kurzname, den der Ansager verwendet, um zu identifizieren, welches Rennen eine aktive Hitze gehört. Seine Verwendung wird nur empfohlen, wenn die Hitze von verschiedenen Rassen gemischt wird. (Zum Beispiel, wenn zwei Klassen am selben Tag laufen), so dass die Fahrer identifizieren können, welche der Klassen die aktive Wärme gehört.

- **Streckenposten**: Die Streckenposten können hier aufgerufen werden, sobald die Strecke für den Lauf geöffnet wurde und bevor er beginnt.
	
	- **kein Aufruf**: ruft die Streckenposten nicht auf.
	- **vorheriger Lauf**: ruft die Fahrer des vorangegangenen Rennens als Streckenosten auf

- **Fahrer aufrufen**: legt Fest wie die Fahrer angesagt werden bei den Positionen im Rennen, Endergebnissen...etc...
	
	- **Kurzname**: nutzt den Kurznamen des Fahrers zum Aufruf
	- **Startnummer**: nutzt die Starnummer des Fahrers zum Aufruf
	
- **Startnummern**: legt das Startnummernsystem für das aktuelle Rennen fest.

	- **jede Session neu nummerieren**: abhängig vom Sessionergebnis werden die Startnummern während des Rennens neu vergeben.
	- **feste Startnummern**: das Fahrzeug hat während des gesamten Rennens eine feste Startnummer ausgehend von der Nennung.

- **Fahrzeug**: legt den Typ des Fahrzeuges fest (Auto oder Moto)

---

##### gemeinsames

- **Warmup**: The time that passes from when the heat (Start) button is pressed and the heat launches.

- **minimale Rundenzeit**: Minimale Rundenzeit für die jeweilige Strecke. Schnellere Runden werden automatisch als Abkürzung betrachtet und nicht gezählt.
 
	!!! beachte ""
		Die minimale Rundenzeit sollte so eng wie möglich festgelegt werden, da sie neben der Abkürzungserkennung für die Sprachausgabe der Positionen während des Qualify herangezogen wird

- **Letzte Runde**: Zeit zum Beenden der letzten Runde nachdem die Laufzeit um ist (oder das Ende der Qualify-Zeit erreicht ist). Entsprechend einiger Regelwerke sollte sie 150% der rechnerischen Rundenzeit nicht übersteigen.

- **Finale Überfahrt Verzögerung**: legt die Zeit fest, in der nach Finalstart keine Überfahrten registriert werden - dies ist nützlich wenn die Maßschleife die Startaufstellung kreuzt

---

#### Sessions

##### mögliche Aktionen

- **hinzugfügen**: fügt ein neues Training, Qualify (sofern noch nicht vorhanden) oder benutzerdefiniertes Rennformat hinzu.
- **löschen**: löscht die gewählte Session.

---

##### Einstellungen

- **Fahrer/Gruppe**: maximale Anzahl an Fahrern jeder Gruppe in Sub-Finals oder Finale für die automatische *Generiere* Option im Tab [Gruppen](../user-guide/races/index.html#series). Im Gruppenmanagement kann die Fahrerverteilung aber auch per drag and drop total frei erfolgen...

- **Gruppenaufteilung**: gibt an wie die Fahrer unter Berücksichtigung des Wertes *Fahrer/Gruppe* in die Gruppen der einzelnen Läufe verteilt werden.

	- **komplett in Reihenfolge**: Füllt die Gruppen nacheinander mit dem Wert *Fahrer/Gruppe*. Dies wird normalerweise in den Finals verwendet um diese voll besetzt zu bekommen - nur die letzte Gruppe ist hier kleiner.
	 
		*Bei einem Rennen mit 26 Fahrern mit z.B. 10 Fahrer/Gruppe werden 3 Gruppen generiert: A B and C with 10, 10 und 6 Fahrern.*
 
	- **gleichmäßige Verteilung**: Distributes by trying to find a even distribution of drivers in all the series without exceeding the value *Drivers/series*. It can be used in qualifying to even out the number of drivers on the track.

		*For example, The same race with 26 drivers with 10 per qualifying series would generate 3 series 1, 2 and 3 with 7, 7 and 8 drivers respectively.* 

- **Durchgänge**: die absolute Anzahl an Läufen pro Serie.

- **Wertung**: die gewertete Anzahl an Läufen pro Serie.

- **Dauer**: Auer jedes Laufes.

---

##### Announcements

- **Type of narration**: Establishes the type of information the system announces during the race.

	- **Race situation**: Periodically the the race situation, drivers positions and distance between them are announced.
	
		!!! note ""
			In qualifying heats, as each driver has their own chrono, it is possible that there will be slight pauses between announcements for each driver. This is completely normal and depends on the distance between the start of each drivers chrono and the reliability of the minimum lap value established for the race. 
	
	- **Position when passing finishing line**: Each time a driver crosses the finishing line the drivers position is announced. This mode is only applied to finals, since all drivers have a common chrono.
	
	- **Mixed (position when passing finishing line + race situation)**: Uses the *position when passing finishing line* and, periodically *race situation* is announced.
	
	- **No narration**: No announcements are made regarding race situation or drivers positions.

- **First narration**: Time from the start of the heat until race situation announcements start being made (generally the announcements start once the race leader passes the finish line after the first narration time has elapsed, therefore there can be a slight delay beyond that of the set time). 

- **Narration Interval**: Time between announcements once the first has been made.

- **Race time interval**: Interval between race time announcements.

- **Race time mode**: Establishes the race time mode for the time used in *Race time Interval*.

	- **Elapsed**: Uses the time elapsed from beginning of heat.
	- **Remaining**: Uses the time remaining until the end of heat.

---

##### Format

- **Session format**: Defines the configuration parameters most used to chrono, and also allows personalised adjustment of each parameter.

	- **qualifying consecutive laps**: This is normally used for re-ordering heats. Each pilots starts their own chrono with the first passing of the finishing line, the sum of the 3 fastest consecutive laps are counted.These are established as *Laps result* value.

	- **Staggered qualifying (points or best result)**: The system calls each driver in turn according to session ranking, with a configured time interval, indicted in the field *Launched start delay*. The option for points or best result are established in the field *Session points type* for the session.

	- **flying start qualifying (points or best result)**: Similar to the previous, but each driver can find their own space on the track and starts their own chrono when they pass the finishing line for the first time.

	- **Finals**: Starting grid launch and in grid order, with the start of the chrono the instant the horn sounds.
	
	- **Practice (points or best result)**: Similar to flying start qualifying, but the chrono starts with the sound of the horn instead of waiting for the first passing of the finishing line.
	
!!! note ""
	The format can be modified even thou heats of the session have already been run. The system re-calculates the results according to the new parameters and the laps recorded.

##### Personalised Format

Allows configuring each of the parameters.

- **Start chrono**: Defines when the chrono starts.

	- **Start on horn**: The chrono start on the starting horn.
	- **start on first passing**: The chrono starts with the first passing of the finishing line by any of the drivers in the heat.
	
- **Chrono mode**: Defines individual chrono management

	- **Individual**: Each driver starts their own chrono (qualifying).
	- **shared**: The chrono start is common to all the drivers (finals).

- **Delayed chrono**: Defines when chrono starts for drivers that have not passed the finishing line for the first time.

	- **First lap completed**: The chrono starts when the first driver completes first lap.
	- **After time delay**: The chrono starts after the time delay defined in *Delayed chrono time* once the heat has started.

- **Delayed chrono time**: for the *After time delay* mode, Indicated the time delay before the chrono starts for drivers that have not passed the finishing line.

- **Start mode**: Defines the format in which drivers start the heat.

	- **Grid**: The system executes a count down, and after the count reaches 3 a random delay is executed followed by the heat start horn.
	- **Staggered**: The system launches the drivers one at a time.
	- **Flying**: A full countdown is executed so that each driver can find a space on the track.

- **Minimum count down time**: Only for *Grid* mode, minimum time delay after last number in the count down, before the start horn.

- **Random count down time**: Only for *Grid mode, random time delay after minimum count down time, before the start horn. *For example, a configured minimum count down time of 2 seconds, and a random count down time of 3 seconds, would mean that after the countdown from 10 to 3, the program will wait between 2 and 5 seconds to sound the start horn.*

- **Staggered start time delay**: For *Staggered* mode only, indicates the time delay between calls to drivers.

- **Staggered start order**: Defines if in each round the start order is recalculated depending on session results.

	- **Re-order each round**: Enables re-ordering. This is the default option for staggered start.
	- **Fixed order**: Maintains the same order in all the rounds.

- **Results type**: Defines the values which are used to calculate the session results:

	- **Laps / Time**: Total amount of laps and time are used to calculate.
	- **Consecutive Laps**: Least amount of time to complete N consecutive laps (Re-ordering).
	- **Fixed Laps**: Amount of time to complete a fixed number of laps (Formula 1 type).

- **Result laps**: Number of laps to count for *consecutive laps* and *fixed laps* modes.

- **Results scope**: Defines the group of drivers included in session results.

	- **Global**: All drivers are taken into account for general classification (qualifying).
	- **Per series**: Only drivers from the same series are used (Finals).

- **Points type**: Establishes the session points type

	- **Points**: A system of points is established for the session results. By default for electric vehicles position obtained in each round (0, 2, 3… for qualifying ; 1, 2, 3... for finals)
	- **Best result**: Best result is chosen laps/time position having no bearing.

- **Points system**: Establishes points system among those supported by the program.

- **Series with complete rounds**: Establishes how many heats count in each series. This is useful for, for example, finals permitting the A series to run 3 rounds of finals counting 2, leaving the series B onward to run a single final.

	- **All series**: All series score points with the same number of heats. There is no difference between series with respect to number of rounds and heats which score points.
	
	- **Premier series**: Only premier series score points in the heats established in the general configuration for the session, the rest the value established in *Lower series rounds*.
	
		- **Until series**: Defines Until what series (inclusive) all the heats are run. For example if only 3 rounds of finals are required for series A, this value should be 1.
		- **Lower series rounds**: Number of rounds that score points for the lower series. For example series below A only score points in 1 heat.

---

##### Tie breakers

Permits establishing how to solve tie breaks, in the case that various drivers obtain the same number of global points in the computable heats for a session.

- **Tie break format**
	- **Default**: Only valid heats are used, first position is used, then in case of tie results.
	- **Personalized**: Permits establishing all tie breaker properties.
	
##### Personalized tie breaker format

- **Heats discarded in tie breaker**: Number of heats discarded used to resolve tie break. The value 0 indicates that no discarded heats are used.
- **Use of discarded heats**: Establishes in which moment the results of discarded heats are used.
	- **Before comparing individual valid heats**: The individual results of discarded heats are used BEFORE individual results of valid heats.
	- **After comparing individual valid heats**: The individual results of discarded heats are used AFTER individual results of valid heats. 
	
		*For example, In 5 round qualifying where the best 3 count not being able to resolve a tie breaker the 4th best round will be used if tie breaker persists the 5th, before comparing the positions of the best 3 rounds.*

- **Tie break by position**: Establishes the mode of individual comparison by position obtained in each heat (only if results are by points)
	- **Best position**: Uses comparison mode based on points obtained.
	- **disabled**: Does not use position based tie breakers.
- **Tie break by result**: Establishes individual results based comparison mode laps/time for each of the heats.
	- **Best result**: Individual results based comparison of heats laps/time.
	- **Combined results**: The tie-break is calculated by the sum of laps/time of all valid heats.
	
!!! note "Tie break resolution by individual comparison"
	In the case where several drivers obtain the same points results (or laps/time), The following tie breaker process is established:

	- The driver with the best position in best heat wins. If the tie breaker persists the second best heat is used, and so on only valid heats (only if the result is by points)
	- If tie break still exists, The driver with the best result (laps/time) in best heat wins. If tie break still exists the second best heat is compared, and so on only valid heats. 

---

#### Tags

Allows assigning Tags for a race. For more information in the [Tags](../common-tasks/tags/index.html) section.

- **Re-calculate points when filtering results by tag**: if enabled, when generating a filtered result based on tags points are re-calculated for the session only for the drivers with the specific tag. The results may vary compared with that of the disabled option and that of the filtered general result, since re-calculating the results depending on points format, the final sum could designate different positions to the drivers.
