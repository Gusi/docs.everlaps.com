# Vorläufe und Finale

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

- **Kurzname**: Kurzname für die Sprachausgabe, welches Rennen eine aktive Hitze gehört. Seine Verwendung wird nur empfohlen, wenn die Hitze von verschiedenen Rassen gemischt wird. (Zum Beispiel, wenn zwei Klassen am selben Tag laufen), so dass die Fahrer identifizieren können, welche der Klassen die aktive Wärme gehört.

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

- **Warmup**: Zwischenzeit nachdem der (Start) Knopf gedrückt wurde bis zum Beginn des Laufes.

- **minimale Rundenzeit**: Minimale Rundenzeit für die jeweilige Strecke. Schnellere Runden werden automatisch als Abkürzung betrachtet und nicht gezählt.
 
	!!! note
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

- **Fahrer/Gruppe**: maximale Anzahl an Fahrern jeder Gruppe in Sub-Finals oder Finale für die automatische *Generiere* Option im Tab [Gruppen](../user-guide/races.md#series). Im Gruppenmanagement kann die Fahrerverteilung aber auch per drag and drop total frei erfolgen...

- **Gruppenaufteilung**: gibt an wie die Fahrer unter Berücksichtigung des Wertes *Fahrer/Gruppe* in die Gruppen der einzelnen Läufe verteilt werden.

	- **komplett in Reihenfolge**: Füllt die Gruppen nacheinander mit dem Wert *Fahrer/Gruppe*. Dies wird normalerweise in den Finals verwendet um diese voll besetzt zu bekommen - nur die letzte Gruppe ist hier kleiner.
	 
		*Bei einem Rennen mit 26 Fahrern mit z.B. 10 Fahrer/Gruppe werden 3 Gruppen generiert: A B und C mit 10, 10 und 6 Fahrern.*
 
	- **gleichmäßige Verteilung**: Füllt die Gruppen gleichmäßig mit dem Wert *Fahrer/Gruppe*. Dies wird normalerweise in den Vorläufen verwendet in allen Gruppen gleichmäßig viele Fahrer auf der Strecke zu haben.

		*Bei einem Rennen mit 26 Fahrern mit z.B. 10 Fahrer/Gruppe werden 3 Gruppen generiert: A B und C mit 7, 7 und 8 Fahrern.*

- **Durchgänge**: die absolute Anzahl an Läufen pro Serie.

- **Wertung**: die gewertete Anzahl an Läufen pro Serie.

- **Dauer**: Auer jedes Laufes.

---

##### Sprachausgabe

- **Srachausgaben-Typ**: Legt die Informationen fest, die während des Rennens per Sprachausgabe durchgegeben werden.

	- **Rennsituation**: In regelmäßigen Abständen werden die Rennsituation, Fahrerpositionen und Abstand zwischen den Fahrern angesagt.
	
		!!! note
			Da in den Vorläufen jeder Fahrer eine eigene Rennzeit hat, kann es zwischen den Sprachausgaben für jeden Fahrer in Abhängikeit des Abstandes zum nächsten Fahrer kleine Pausen geben.
	
	- **Position bei Überfahrt**: Jedes Mal, wenn ein Fahrer die Meßschleife überquert, wird die Fahrerposition ausgegeben. Dieser Modus wird nur auf das Finale angewendet, da alle Fahrer eine gemeinsame Startzeit haben.
	
	- **gemischt (Position bei Überfahrt + Rennsituation)**: gibt die *Position bei Überfahrt* und regelmäßig auch die *Rennsituation* aus.
	
	- **keine Sprachausgabe**: es erfolgen bezüglich der Rennsituation und Position im Rennen keine Sprachausgaben.

- **erste Platzierung**: Zeit nach Start des Laufes bevor die erste Platzierung angesagt wird - das Fahrerfeld sollte bei diesem Wert mindestens eine Runde absolviert haben. 

- **Platzierung**: Intervall zwischen den einzelnen Ansagen der Platzierung nach dem die erste Ansage erfolgt ist.

- **Rennzeit**: Intervall zwischen den einzelnen Ansagen der Rennzeit nach dem die erste Ansage erfolgt ist.

- **Rennzeit Modus**: setzt den Rennzeitmodus für die Sprachausgabe der *Rennzeit*

	- **abgelaufen**: gibt die abgelaufene Zeit seit Beginn des Laufes aus.
	- **verbleibend**: gibt die verbleibende Zeit bis zum Ende des Laufes aus.

---

##### Format

- **Sessions-Format**: legt die Einstellung für die Zeitmessung in allen Abschnitten des Rennens fest

	- **Vorläufe beste aufeinanderfolgende Runden**: Dies wird normalerweise für das Qualify zu den Läufen verwendet. Jeder Pilot startet mit dem ersten Durchgang der Ziellinie seine eigene Zeitmessung, die Summe der 3 schnellsten aufeinanderfolgenden Runden wird dann gewertet. Diese Anzahl Runden (in dem Beispiel 3) wird als Wert in *Rundenergebnis* festgelegt.

	- **Vorläufe gestaffelter Start (Punktewertung oder bestes Ergebnis)**: Das System ruft jeden Fahrer einzeln entsprechend seiner Session-Position nach einem im Feld *Abstand verzögerter Start* angegebenen Zeitintervall zum starten auf. Wurde die Punktewertung gewählt, so ist im Feld *Punkte-System* zusätzlich die gewünschte Punkteverteilung zu setzen.

	- **Vorläufe fliegender Start (Punktewertung oder bestes Ergebnis)**: vergleichbar zu den vorherigen Schemas, mit dem Unterschied, dass sich die Fahrer aus den Aufwärmrunden heraus direkt ins Rennen starten. Die individeuelle Zeitmessung beginnt, sobald der Fahrer das erste Mal die Meßschleife passiert.
 
	- **Finale (Punktewertung oder bestes Ergebnis)**: Start aus der Startaufstellung in Reihenfolge der Rennpositionen. Die Zeitmessung beginnt mit dem Start durch einen Signalton.
	
	- **Training (Punktewertung oder bestes Ergebnis))**: vergleichbar zum fliegenden Start in den Vorläufen, nur startet die Zeitmessung mit dem Signalton anstelle auf die erste Überfahrt zu warten.
	
!!! note
	Das Format kann modifiziert werden, selbst wenn die Session bereits ausgeführt wurde! Das System berechnet dann die Ergebnisse anhand der neuen Parametern und den aufgezeichneten Runden neu.

##### benutzerdefiniertes Format

dies erlaubt die freie Konfiguration jedes Rennparameters

- **Messung starten**: definiert wann die Zeitmessung gestartet wird

	- **bei Signalton**: Die Zeitmessung startet mit dem Signalton.
	- **bei erster Überfahrt**: Die Zeitmessung startet bei der ersten Überfahrt eines der Fahrer über die Meßschleife.
	
- **Messmodus**: definiert den individuellen Meßmodus

	- **individuell**: jeder Fahrer wird einzeln gemessen (Vorläufe).
	- **gemeinsam**: Die Zeitmessung startet für alle Fahrer gemeinsam (Finals).

- **Verzögerung Zeitmessung**: definiert den Start der Zeitmessung für Fahrer, die nach Rennstart die Meßschleife noch nicht passiert haben.

	- **erste komplette Runde**: die Zeitmessung startet sobald der erste Fahrer seine erste Runde abgeschlossen hat.
	- **verzögert**: die Zeitmessung beginnt nach der bei *Verzögerung Zeitmessung* eingegebenen Zeit nachdem der Lauf gestartet wurde.

- **Verzögerungszeit**: gibt beim Modus *verzögert* an, nach welcher Zeitspanne die Zeitmessung für Fahrer beginnt die nach Rennstart die Meßschleife noch nicht passiert haben.

- **Start Modus**: Definiert die Art des Startes der Läufe.

	- **Startreihen**: Das System führt einen Countdown aus bei dem nach Ablauf und Zufallsverzögerung der Start durch Signal erfolgt.
	- **gestaffelt**: Das System lässt jeden Fahrer einzeln starten.
	- **fliegend**: während der Einführungsrunden wird ein interner Countdown ausgeführt nach dem der fliegende Start für jeden Fahrer auf der Strecke erfolgt.

- **minimale Countdownzeit**: nur bei *Startreihen* , kleinste Verweilzeit zwischen runterzählen des CountDowns und dem Signalton

- **Zufalls-Countdown**: nur bei *Startreihen*, zufällig bestimmte Verzögerungszeitspanne zwischen runterzählen des CountDowns und dem Signalton *Eine minimale Countdownzeit von 2 s und zufällig bestimmte Verzögerungszeitspanne von 3 s bedeutet dass nach dem CountDown von 10 bis 3 das Programm 2 s wartet und danach im Zeitraum zwischen 1 - 2 s das Startsignal gibt.*
- **Verzögerung gestaffelter Start**: nur bei *gestaffelt*, bestimt die Zwischenzeit zwichen den Einzelnen Fahreraufrufen.

- **Reihenfolge gestaffelter Start**: Legt fest, ob in jeder Runde die Startreihenfolge je nach Sitzungsergebnis neu berechnet wird.

	- **Startreihenfolge neu**: Ermöglicht die Neuordnung. Dies ist die Standardoption für gestaffelten Start
	- **feste Reihenfolge**: Behält die gleiche Reihenfolge in allen Runden bei

- **Ergebnistyp**: Defines the values which are used to calculate the session results:

	- **Runden/Zeit**: die Anzahl Runden und die entsprechende Zeit wird als Berechnungsgrundlage für das Ergebnis genommen.
	- **aufeinanderfolgende Runden**: Mindestestzeit, um N aufeinander folgende Runden zu vervollständigen (Startreihenfolge neu).
	- **festgelegte Runden**: Zeitspanne um eine festgelegte  Anzahl aufeinander folgende Runden zu vervollständigen (Formel 1).

- **Rundenergebnis**: Anzahl der Runden für *aufeinanderfolgende Runden* und *festgelegte Runden*.

- **Ergebnisbereich**: Definiert den Anwendungsbereich der Session-Ergebnisse auf die Gruppe der Fahrer.
	- **gemeinsam**: alle Fahrer werden zusammen ausgewertet für das Ergebnis (Vorläufe).
	- **je Gruppe**: nur Fahrer der selben Gruppe werden zum Ergebnis herangezogen (Finale).

- *Wertungstyp**: Legt den Wertungstyp für die Session fest

	- **Punkte**: die Sitzungsergebnisse werden anhand eines Punktesystemes ausgewertet. Standardmäßig ist dies z.B. bei Elektrofahrzeugen anhand der Position in jeder Runde (0, 2, 3 ... für die Vorläufe und  1, 2, 3 ... für Finale).
	- **bestes Ergebnis**: für die Sitzungsergebnisse wird jeweils nur der beste Wert aus Runden/Zeit herangezogen, die Position hat keinen Einfluss.

- **Punktesystem**: Stellt das jeweilige Punktesystem je nach der Möglichkeiten des Programmes ein.

- **Wertungsläufe je Gruppe**: Legt fest, wie viele Läufe in jeder Gruppe gewertet werden. Dies ist zum Beispiel für Finale geeignet, um in der A-Serie 3 Finalrunden zu fahren und 2 werten zu lassen und aber in Serie B (nur) ein einziges Finale zu fahren.

	- **alle Gruppen**: Alle Serien werden mit der gleichen Anzahl an Läufe gewertet. Es gibt keinen Unterschied zwischen der Serie in Bezug auf die Anzahl der gewerteten Runden und Läufe.
	
	- **vorderste Gruppen**: Nur in der führenden Gruppen werden alle Wertungsläufe je Gruppe entsprechend der Rennkonfiguration angewendet, für die restlichen Gruppen gilt der Wert aus *Wertungsläufe niedrigere Gruppen*.
	
		- **bis Gruppe**: Definiert bis zu welcher Gruppe (inklusive) die Wertungsläufe nach Konfiguration angewendet werden. Zum Beispiel, wenn 3 Runden Finale nur für Gruppe A erforderlich ist, muss der Wert auf 1 gesetzt sein.
		- **Wertungsläufe niedrigere Gruppen**: definiert die Anzahl an gewerteten Läufen für die niedrigeren Gruppen. Wenn für die Gruppen B...C...D nur 1 von 3 Läufen gewertet werden soll, dann ist der Wert 1.

---

##### Gleichständler

Diese Funktion ermöglicht die Rangeinteilung der Fahrer bei gleichem Ergebnis / gleicher Punktzahl nach Abschluss der gültigen Läufe (Gleichstand) 

- **Gleichstandsformat**
	- **standard**: nur gültige Läufe werden genutzt und es werden dort die Positionen der Gleichständler verglichen
	- **benutzerdefiniert**: hier können benutzerdefinierte Regelungen zur Behebung des Gleichstandes festgelegt werden.
	
##### benutzerdefinierte Gleichstandsauflösung

- **verworfene Läufe bei Gleichstand**: Gibt die Anzahl an verworfenen Läufen an die zur Auflösung des Gleichstandes herangezogen werden. Der Wert 0 bedeutet keine.
- **verworfene Läufe nutzen**: gibt an in welchem Moment die verworfenen Läufe mit herangezogen werden.
	- **vor dem Verlauf der gültigen Läufe**: Die individuellen Ergebnisse aus den verworfenen Läufen werden VOR dem Vergleich der gültigen Läufe angewendet.
	- **nach dem Verlauf der gültigen Läufe**: Die individuellen Ergebnisse aus den verworfenen Läufen werden NACH dem Vergleich der gültigen Läufe angewendet.
	
		*Wenn sich beispielsweise ein Gleichstand ergibt bei 5 Vorläufen und davon 3 gewerteten, dann werden zur Auflösung nacheinander auch der 4. Lauf und der 5. Lauf herangezogen - und dies je nach Wahl vor bzw nach dem Vergleich der Positionen in den 3 gewerteten Läufen.*    

- **Position Gleichstand**: Establishes the mode of individual comparison by position obtained in each heat (nur bei Punktewertung)
	- **beste Position**: Vergleichsmodus auf der Grundlage der entsprechend der Position erhaltenen Punkte.
	- **nicht verwenden**: keine Nutzung der Position für Gleichstände.
- **Ergebnis Gleichstand**: setzt den Modus für die Gleichstandsauflösung auf die individuellen Ergebnisse aus Runden/Zeit für jeden der Läufe.
	- **bestes Ergebnis**: zieht das beste Ergebniss aus Runden/Zeit zur Auflösung heran...
	- **kombinierte Ergebnisse**: zieht die Summe der Ergebniss aus Runden/Zeit aller gültigen Läufe zur Auflösung heran...
	
!!! note "Gleichstandsauflösung durch Einzelvergleich"
	Für der Fall dass mehrere Fahrer die gleichen Punkte (oder Runden/Zeit) haben, ist der Modus der Gleichstandsauflösung wie folgt:

	- Der Fahrer mit der besten Position im Lauf gewinnt. Wenn der Gleichstand anhält, wird die zweitbeste Lauf verwendet, und so weiter (nur für gültige Läufe und nur wenn das Ergebnis nach Punkten ermittelt wird)
	- Wenn der Gleichstand weiterhin existiert, gewinnt der Fahrer mit dem besten Ergebnis (Runden/Zeit) im besten Lauf. Wenn der Gleichstand weiterhin existiert, die wird der zweitbeste Lauf verglichen, und so weiter (nur für gültige Läufe)

---

#### Marker

erlaubt das Hinzufügen von Markern zum Rennen - für nähere Informationen siehe [Marker](../common-tasks/tags.md)

- **Neuberechnen der Ergebnisse für die nach Marker gefilterten Werte**: wenn aktiviert, werden beim darauffolgenden Erzeugen der Ergebnisse nur die Fahrer mit den angegebenen Markern zur Berechnung herangezogen - damit können z.B. Altersgruppenwertungen innerhalb des Rennens parallel erzeugt werden. 
