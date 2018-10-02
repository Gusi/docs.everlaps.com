## Schnellstartanleitung

Hier werden die grundlegenden Schritte zum Installieren und Starten eines Rennens in Everlaps beschrieben. Für weitere Details schauen Sie bitte in der Dokumentation.

---

### grundlegende Tätigkeiten

1.  Fahrerdaten eingeben unter [&fa-users; **Fahrer**](./user-guide/drivers.md)

2.  ein neues Rennen anlegen unter [&fa-road; **Rennen**](./user-guide/races.md), vorkunfigurieren durch die [&fa-flag; **Session**](./race-formats/qualify-finals.md) Optionen

3.  teilnehmende Fahrer eintragen unter [&fa-user; **Nennung**](./user-guide/races.md#inscripciones)

4.  &fa-check-circle; **Generieren** und &fa-print; **Drucken** der Fahrergruppen unter [&fa-th; **Gruppen**](./user-guide/races.md#series)

	*nach jeder Session gehen Sie hierhin zurück um die Gruppen für die nächsten Sessions zu generieren. z.B. um die Final-Gruppen nach Abschluss der Vorläufe zu generieren*

5.  zum Abschluss &fa-check-circle-o; **Bestätigen** der Fahrer in [&fa-th; **Gruppen**](./user-guide/races.md#series)

	*Die Gruppen wurden erzeugt*

6.  [&fa-upload; **Aktivieren**](./user-guide/heats.md#mangas_1) und starten ([&fa-check-circle; **Start**](./user-guide/heats.md#control-de-la-manga-activa)) der Läufe nacheinander [&fa-clock-o; **Läufe
**](./user-guide/heats.md)

7.  Korregieren und Bestrafen wenn nötig und &fa-print; **Drucken** der Ergebnisse

---

### Installation des Programmes

Systemvoraussetzungen

- Windows Vista / 7 / 8 / 10

- Microsoft .NET Framework 4.5 oder höher

- TTS kompatible Sprachausgabe SAPI 5 kompatibel (z.B. Ivona, Loquendo, ...)

- Decoder AMB/MyLaps kompatibel mit seriellen / USB / Netzwerk - Anschluss

- PDF-Reader ([Foxit Reader](http://www.foxitsoftware.com/Secure_PDF_Reader/), [Adobe Reader](http://get.adobe.com/reader/), ...)

!!! Warnung !!!  "Windows Energiesparoptionen"
Während des Timings ist es wichtig, dass alle Computer-Energiesparoptionen ausgeschaltet sind (Ruhezustand, Festplattenlaufwerk im Leerlauf usw.), da diese die ordnungsgemäße Funktion während der Perioden der persönlichen Inaktivität am Rechner aber laufender Zeitnahme unterbrechen können.  

---

### Sprachausgabe installieren

Die Sprachausgabe erfordert die Installation eines TTS-Stimmpaketes (Dieses ist nicht in der Everlaps Lizenz enthalten). Die Empfehlung sind Stimmpakete von [Ivona](http://www.ivona.com).

Sind die Stimmen installiert konnen Sie eingestellt werden unter [&fa-gear; **Optionen in der Konfiguration**](./user-guide/config.md)

---

### Decoder anbinden

Schliessen sie den AMB/MyLaps Decoder entsprechend der Anweisungen des Herstellers an. 

Abhängig von der Art der Verbindung müssen die korrekten Werte eingestellt werden unter [&fa-gear; **Optionen in der Konfiguration**](./user-guide/config.md)

- serielle oder USB Anbingung: geben Sie den Port an durch den der Decoder verbunden ist (Beispiel: COM1, COM2, ...)

- Netzwerkanbindung: geben Sie die IP Adresse des Decoders ein (Beispiel: 192.168.1.2)


!!! Warnung!!! "Netzwerkverbindung"
	
	- Wenn Sie den Decoder direkt an einen Computer anschließen, kann es sein, dass Sie ein [Crossover-Kabel] (https://en.wikipedia.org/wiki/Ethernet_crossover_cable) benötigen. Wenn es einen Hub, Switch oder Router dazwischen gibt ist dies nicht notwendig.
	
	- Decoder und der Rechner müssen sich im gleichen Subnetz befinden (z.B. Rechner 192.168.0.1 ist und Decoder 192.168.0.2). Wenn Sie keine Verbindung zum Decoder bekommen, müssen Sie möglicherweise das automatische DHCP auf dem Decoder deaktivieren und eine statische IP manuell auf dem LCD-Bildschirm des Decoders eingeben. Beachten Sie hier die Anweisungen im Handbuch des Decoderherstellers. 
	
	
	
