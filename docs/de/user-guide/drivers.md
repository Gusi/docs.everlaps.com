## &fa-users; Fahrer

Ermöglicht die Verwaltung aller Fahrer in der Programmdatenbank.

![Fahrer](../img/drivers.png)

Glossar der Begriffe, die in der Fahrerverwaltung verwendet werden

- ** Fahrer **: Eine Person, die in einem der konfigurierten Rennen genannt werden kann
- ** Klassen **: Klassifiziert Die verschiedenen Klassen nach Fahrzeugtyp
- ** Transponder **: Persönliche Transpondernummer, die von der Zeitmessanlage verwendet wird, um einen Fahrer zu identifizieren
- ** Rangliste **: Die Fahrerfähigkeit in Bezug auf die Gesamtheit in der entsprechenden Klasse (Jahresrangliste,Bestenliste)
- ** Tag **: Ermöglicht es Ihnen, Treiber mit einer gemeinsamen Kennung zu gruppieren 

Einem Fahrer können verschiedene Transponder oder Ränge in den entsprechend den Klassen zugeordnet werden, sowie auch jeder in der Datenbank definierte Marker.

---

### Fahrerliste

erlaubt das Hinzufügen, Löschen und Ändern aller verfügbaren Fahrer.

##### Aktionen

- **Hinzufügen**: Fügt eine neue Zeile in die Fahrerliste ein, die dann mit Fahrerdaten gefüllt werden kann.

- **Löschen**: löscht den markierten Fahrer aus der Datenbank. 

- **Importieren**: läd eine Liste an Fahrern aus einer Datei in die Datenbank.

- **Exportieren**: speichert markierten Fahrer als eine Liste in eine Datei.

- &fa-search; **(Suche)**: Führt eine Suche nach den Fahrern mit den im Suchfeld eingegeben Texten durch und zeigt Treffer und teilweise Treffer aus den Feldern (Name, Nachname, Transponder, Kategorie, Tags usw.)

##### Felder

- ** Name und Nachname **: Wird in der Liste angegeben, um den Fahrer zu identifizieren.

- **Kurzname**: Kurznamen werden von den Sprachansagen verwendet, um die Zeiten und die Position der Fahrer auszugeben sowie in den Livetime-Rennberichten. Doppelte Kurznamen sind in der Datenbank gestattet, aber sie sind im gleichen Lauf nicht erlaubt (Das Programm wird eine Warnung ausgeben, damit sie geändert werden können).

- **email**: Die E-Mail-Adresse ist dient dazu, dass das Programm den Fahrer zwischen der lokalen Datenbank und der im Internetportal der [Everlaps Website](http://everlaps.com) synchronisieren kann. Damit werden Nennung und Resultate bidirektional verwaltet.

	Wenn Fahrer manuell hinzugefügt werden, ist es wichtig, die E-Mail-Adresse korrekt hinzuzufügen, falls sie bereits auf [Everlaps](http://everlaps.com) registriert sind - nur so werden die Ergenisse korrekt zugeordnet.

- **Marker**: Zeigt alle dem Fahrer zugeordneten Marker.

---
	
### Fahrerkarte

Zeigt alle Informationen über einen Fahrer, einschließlich der bereits erwähnten personenbezogenen Daten wie Listen von Transpondern, Ranglisten pro Klasse und auch aktive Rennen, an denen der Fahrer teilnimmt sowie alle zugewiesenen Marker.

#### Transponder, Ränge und Startnummern

Hier verwalten Sie in der Fahrerliste die Transponder, Ranglisten und Startnummern nach den Klassen, an denen die Fahrer teilnehmen.

- **Klassen**: erlaubt die Auswahl der [Klassen](./config/ind	ex.html#categorias), aus den Werten der Liste.
- **Transponder, Ränge, Startnummern Kommentare**: Ermöglicht die Zuordnung von Werten, die dem Fahrer in der gewählten Klasse entsprechen.

!!! beachte ""
	Wenn man einen Fahrer manuell in einem Rennen registriert, vergleicht das System die Klassen des Rennens mit den dem Fahrer zugeordneten Klassen um den entsprechenden Transponder zuzuordnen. Falls es keine Übereinstimmung gibt, wird der Standard-Transponder für diese Klasse zugewiesen. 

#### aktive Nennungen

Liste der als aktiv markierten Rennen, an denen ein ausgewählter Fahrer teilnimmt.

Es ist möglich, den Transponder und den Rang des ausgewählten registrierten Fahrers zu ändern, genauso wie in der [Nennung](./races/index.html#inscripciones).

#### Marker

Zeigen Sie die dem Fahrer zugeordneten Marker an.

Die Marker erlauben das schnelle Filtern und Gruppieren von Fahrern innerhalb der verschiedenen Klassen. (Fahrerliste, Nennungen, Läufe ...).

Jeder Marker kann aus dem unteren Dropdown-Feld zugewiesen werden und kann durch Klicken auf das * X * entfernt werden, das angezeigt wird, wenn der Cursor über dem zu entfernenden Tag liegt. Die vollständige Liste steht in der [Marker](./config/index.html#etiquetas) Sektion.


