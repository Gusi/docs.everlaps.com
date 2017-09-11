## &fa-road; Rennen

Hier werden die Rennen verwaltet die Einstellungen dafür festgelegt.

![Rennen](../img/races.png)

---

### Rennliste

Zeigt die Liste der aktuell verfügbaren Rennen an.

##### verfügbare Funktionen

- **Hinzufügen**: fügt ein neues Rennen entsprechend der Auswahl des Rennformates aus folgenden Möglichkeiten aus:
	- **Vorläufe und Finale**: erstellt ein Rennen aus [Vorläufen und Finals](../race-formats/qualify-finals/index.html)
	- **Vorläufe, Halfinale und Finale**: erstellt ein Rennen im [Aufsteigersystem](../race-formats/christmas-tree/index.html)
	- **Freies Training**: erstellt im Rennen ein [Freies Training](../race-formats/free-practice/index.html)
	- **aus Datei laden**: erstellt ein Rennen aus einer zuvor exportierten Rennkonfiguration.

- **Löschen**: löscht alle Daten des gewählten Rennens inklusive Nennung, Läufen und Ergebnissen.

##### Rennen Eingabefelder

- **Rennen**: Titel für das Rennen, wird in der Zuordnung der Läufe und oben auf den Listen ausgegeben

- **aktiv**: Zeigt ob das Rennen aktiviert ist. Aktive Läufe werden angezeigt in der [Laufliste](./heats/index.html#mangas_1) Über den AutoModus kann der zeitliche Rennablauf automatisiert werden.

---

### &fa-gear; Format

##### verfügbare Funktionen

- **exportieren**: exportiert eine Rennkonfiguration um damit später verschiedene Rennen mit gleicher Konfiguration erstellen zu können.

Die weitere Rennkonfiguration hängt vom Typ Format des gewählten Rennens ab - siehe bei den möglichen Formaten: 

- **[Vorläufe und Finale](../race-formats/qualify-finals/index.html)**
- **[Aufsteiger](../race-formats/christmas-tree/index.html)**
- **[Freies Training](../race-formats/free-practice/index.html)**

---

### &fa-user; Nennungen

![Nennungen](../img/registrations.png)

Das Nennmanagement (ausser für [Freies Training](../race-formats/free-practice/index.html) dort werden die Fahrer automatisch regisriert sobald sie die Meßschleife erstmals passieren - vorausgesetzt sie sind in der Datenbank eingepflegt).

Der Bildschirm ist horizontal zweigeteilt:

- Der *obere* Teil beinhaltet die im Rennen genannten Fahrer.
- Der *untere* Teil ist die *Liste verfügbarer Fahrer* und zeigt die in der Datenbank gespeicherten Fahrer die noch nicht im Rennen genannt sind.

##### Funktionen

- **Alle Hinzufügen**: fügt alle aus der Datenbank verfügbaren Fahrer in die Nennliste ein.

- **Löschen**: löscht alle gewählten Fahrer aus der Nennliste (diese werden in die Liste verfügbarer Fahrer zurückgestuft).

- **Importieren**: 
	- **aus einer lokalen Datei**: läde die Nennliste aus einer über die [Everlaps-Website](http://everlaps.com) heruntergeladenen Nennliste.
	- **aus dem Internet**: läde die Nennliste direkt von der Everlaps-Website, sofern das [Rennpasswort](../race-formats/qualify-finals/index.html#campos-de-formato) gesetzt ist.
	
	!!! beachte ""
		Werden Fahrer importiert die zuvor schon lokal genannt waren, werden diese nicht überschrieben - Transponder und Rang bleiben erhalten, nur zuvor nicht genannte werden importiert.
	
- **Exporieren**: exportiert die Nennliste in eine Textdatei.

- **Drucken**: Druckt die Nennliste mit Fahrern und Transpondernummern.

- **Werkzeuge**:
	- **Rang zu Fahrzeugnummer**: Kopiert den Rang auf die Fahrzeugnummer.
	- **Fahrzeugnummer zu Rang**: Kopiert die Fahrzeugnummer zum Rang.
	- **Aufeinanderfolgende Fahrzeugnummern**: Nummeriert die Liste der Fahrzeuge entsprechend der Rangordnung beginnend mit 1 neu.

- &fa-search; **(Suche)**: Führt eine Suche unter den genannten Fahrern durch, deren Datenfelder (Name, Nachname, Kurzname, usw.) ganz oder teilweise mit dem im Suchfeld eingegebenen Text übereinstimmen.

##### Felder

- **Name, Surname and Nick name**: These values are copied directly from the database. They can be modified on the [drivers](./drivers/index.html) screen. This change will affect all the races that the driver is registered in.

- **Transponder und Rang**: These fields can be changed and will only affect the selected race. If a transponder is changed, a dialog window will ask permission to change it to the default transponder in the database for future races, if the driver belongs to an active heat, a dialogue will ask permission to hot-swap the transponder number. See [transponder changes](../common-tasks/change-transponders/index.html) for more information.

- **Ausgeschlossen**: The penalised driver will be placed last in all race results. The excluded drivers will no longer be included in the automatic generation of new series. See [penalties and corrections](../common-tasks/punishments-corrections/index.html) for more information.

#### verfügbare Fahrer

die *Liste verfügbarer Fahrer* zeigt die in der Datenbank gespeicherten Fahrer die noch nicht im Rennen genannt sind.

##### Aktionen

- &fa-search; **(Suche)**: Führt eine Suche unter den nicht genannten Fahrern durch, deren Datenfelder (Name, Nachname, Kurzname, usw.) ganz oder teilweise mit dem im Suchfeld eingegebenen Text übereinstimmen.

---

### &fa-th; Gruppen

![Gruppen](../img/series.png)

Der Bildschirm in diesem Bereich ist zweigeteilt:

 - auf der rechten Seite die *Gruppeneinteilung*, enthält die Liste der Gruppen für die ausgewählte Session und Ihre jeweiligen Fahrer
 - auf der linken Seite die Liste der *Fahrer ohne Gruppeneinteilung*, enthält die Liste der Fahrer die in der ausgewählte Session noch keiner Gruppe zugeordnet wurden.
 
##### Aktionen

- **Session**: Wählt die Session aus für die die Gruppen gezeigt werden sollen.

- **Generieren**: Automatically generates a list of series with the number of drivers per series indicated in the session configuration, following rank order or based on the results of previous sessions, according to the parameters selected in the following dialogue:
	
	![Gruppen einteilen](../img/serie-distribution-selection.png)

	- **Fahrer Rang**: Driver order is defined by ranking.
	- **Kopiere Von Session**: Driver distribution is copied exactly the same as established in the session selected in the lower list.
	- **Session Ergebnis**: The driver order is defined by the results of the session selected in the lower list.

		!!! beachte ""
			Beim Generieren von Läufen auf Basis von Ergebnissen einer vorherigen Sitzung werden ausgeschlossene Fahrer ignoriert.

- **Hinzufügen**: Fügt eine leere Gruppe hinzu.

- **Löschen**: Löscht die gewählte Gruppe. Die Fahrer in dieser Gruppe werden zu den *Fahrern ohne Gruppe* zurückgestuft. 

- **ohne Gruppe**: fügt alle *Fahrer ohne Gruppe* der letzten Gruppe hinzu.

- **Bestätigen**: Erzeugt die Läufe entsprechend der Gruppenverteilung aus der Konfiguration.

	!!! beachte ""
		If after creating the heats new series are added, these can be *confirmed* and the heats for the new series will be added. It is also possible to move drivers once the heats are confirmed, the program is flexible in that way.

- **Drucken**: Prints the list of series with the drivers that are in each series.

- **Werkzeuge**:
	- **Re-order heats**: Allows manual re-order of the actual series.

#### Gruppeneinteilung

Die Fahrer können per drag & drop von einer Gruppe in eine andere umverteilt werden.

##### Felder

- **Name, surname and Nick name**: These are the same as appear in the database.

- **Bester Lauf**: Allows a driver to be penalised with the loss of *best heat*. See [penalties and corrections](../common-tasks/punishments-corrections/index.html) for more information.

- **Excluded**: A driver can be penalised and will occupy the last place in this session. Excluded drivers will not automatically be added to new sessions. See [penalties and correctiones](../common-tasks/punishments-corrections/index.html) for more information

#### Fahrer ohne Gruppen

Alle genannten Fahrer die im Rennen noch keiner Gruppe zugeordnet sind, werden auf der rechten Seite des Bildschirms angezeigt. Die Fahrer dieser Liste können nach Bedarf in die Gruppen gezogen werden.

!!! beachte ""
	Wenn die Gruppen einmal generiert wurden, können Nachnennungen per drag & drop aus den *Fahrer ohne Gruppe* in die bestehenden Gruppen zugeordnet werden, werden zusätzliche Gruppen erzeugt müssen sie diese *Bestätigen* 
	
	Es ist nicht erforderlich bestehende Gruppen neu zu generieren
	
---

### &fa-trophy; Ergebnisse

![Ergebnisse](../img/results.png)

Zeigt die Ergebnisste der gewählten Session mit den Details der von jeden Fahrer zurückgelegten Runden, ausserdem werden Gleichstände, Korrekturen und Strafen der Session ausgegeben.

##### Funktionen

- **Sitzung**: Wählt die Session für die die Ergebnisse ausgegeben werden sollten.

- **Neu Berechnen**: Aktualisiert das Ergebniss der Session sofern der aktuelle Lauf Einfluss darauf hat.

- **Drucken**: Druckt die Ergebnisse der gewählten Session.

