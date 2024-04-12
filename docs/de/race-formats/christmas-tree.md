# Aufsteiger

Das Aufsteigersystem ist charakterisiert durch eine Reihe an Sub-Finals in Form einer Pyramide oder eines * Weihnachtsbaumes *, das ermöglicht jedem Fahrer sich selbst bei schlechter Platzierung in den Vörläufen durch die Sub-Finals bis ins grosse Finale hochzufahren.

Die Sessions vor den Finals (Training, Zeitqualifikation und oder Vorläufe) sind von dieser Einstellung nicht betroffen und bleiben wie definiert in den [Vorläufen und Finals](./qualify-finals.md), diese Funktion betrifft nur die Finals - daher bezieht sich der folgende Abschnitt nur auf diese...

### Konfiguration von Sub-Finals und Finale

![Aufsteiger](../img/subfinals.png)

!!! note
	The number of drivers used to calculate the distribution of the sub-finals is that of the registration list, except those drivers excluded from the race or qualifying session. This is useful to fine tune the distribution in case there are drivers that are registered but are not going to race, or have abandoned after qualifying.

- **Name**: bezeichnet das Subfinale oder Finale und wird automatisch gesetzt.

- **Gruppen**: Anzahl aller Gruppen der Sub-Finals - werden automatisch berechnet. Jedes Subfinale hat immer zwei Gruppen ausser:

	- Das Finale - es besteht immer aus einer Gruppe.
	- Das letzte Subfinale, sofern die Anzahl Fahrer gleich oder kleiner als der Wert *Fahrer/Gruppe* und die Option *Optimieren des letzten Sub-Finals* zum Erzeugen nur einer einzelnen Gruppe aktiviert ist.

- **Dauer**: Dauer jedes Laufes in Sub-Finals oder Finale.

- **Fahrer/Gruppe**: maximale Anzahl an Fahrern jeder Gruppe in Sub-Finals oder Finale.

- **Direkt/Gruppe**: Anzahl der Fahrer, die je nach Qualifikationsergebnis direkt zu jedem Subfinale oder Finale aufsteigen. Im obigen Beispiel gelangen die ersten beiden qualifizierten Fahrer in das Finale.

- **Aufsteiger/Gruppe**: Anzahl der Fahrer, die je nach Ergebnis im aktuellen Subfinale in das nächste Subfinale oder Finale aufsteigen.

	* Im obigen Beispiel sind das vom Halbfinale bis zum Finale 4 Fahrer pro Gruppe (8 insgesamt: Die ersten 4 aus dem Semifinale A und die ersten 4 aus dem Semifinale B). *

      Das Finale wird anders behandelt, da es das letzte Level des Aufstieges ist und damit kein weiterer Aufstieg erfolgen kann. Wählen Sie hier wie das Starterfeld aus den Fahrern der höchsten Subfinale generiert werden soll.

	- **durch Zeit**: Alle Fahrer aus den Gruppen A und B sind nach ihrem *Runden/Zeiten* der Semifinals in die Startaufstellung positioniert.
	- **verschachtelt**: Die Fahrer werden von beiden Gruppen gleichmäßig platziert: erster Platz Gruppe A, erster Platz Gruppe B, zweiter Platz Gruppe A, zweiter Platz Gruppe B, etc ...
	!!! note
		Für den Fall, dass die Summe der Fahrer mit direktem Aufstieg und denen, die durch Ihr Ergebnis Aufsteigen, nicht die Gesamtsumme der Fahrer pro Gruppe übereinstimmt, werden die weiteren Fahrer um die Gruppe zu komplettieren über *Runden/Zeit* hinzugefügt.

- **Gruppenverteilung**: Zeigt eine Zusammenfassung der Zusammenstellung der Sub-Finals nach den im Rennen registrierten Fahrern an, um zu überprüfen, ob die eingegebenen Daten die gewünschte Verteilung erzeugen.

	- **Nummer + Nummer**: teilnehmende Fahrer in jeder Gruppe.
	- **D**: Anzahl der Fahrer, die je nach Qualifikationsergebnis *Direkt* zu jedem Subfinale oder Finale aufsteigen
	- **P**: Anzahl der Fahrer, die je nach *Position* im vorhergehenden Subfinale zu weiteren Sub-Finals oder ins Finale aufsteigen
	- **T**: Anzahl der Fahrer, die je nach Runden/Zeit (TIME)* im vorhergehenden Subfinale zu weiteren Sub-Finals oder ins Finale aufsteigen
	
##### zusätzliche Funktionen

- **Sub-Finals generieren**: Initialisiert oder aktualisiert die Liste der Sub-Finals entsprechend den eingegebenen Konfigurationsparametern und der Anzahl der im Rennen genannten Fahrer.

- **direkt qualifizierte drucken**: Sobald die Vorläufe abgeschlossen sind, kann hier eine Liste mit den direkt in die jeweiligen Finals qualifizierten Fahrern erstellt werden

!!! warning "Subfinals generieren"

    Nachdem Änderungen an einem der Konfigurationsparameter des Aufsteigersystems vorgenommen wurden, der Einfluss auf die Anzahl der Sub-Finals hat, ist es notwendig auf *Sub-Finals erstellen* zu klicken um die Liste der Sub-Finals im Rennen zu aktualisieren.

	erst nachdem *Subfinals generieren* ausgeführt wurde, werden auch die Gruppen im Panel [Gruppen](../user-guide/races.md#series) erzeugt.
