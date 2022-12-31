---
title: 'CAN-Bus'
author: 'Jan Unger'
date: \today
subject: "Markdown"
keywords: [Markdown]
lang: "de"
bibliography: literatur-kfz.bib 
csl: zitierstil-number.csl
---
<!-----------------------------
Quelle: Europa-Verlag
![, Quelle: Europa-Verlag](images/CAN-Bus/.png){width=70%}

Quelle: Europa-Verlag Arbeitsblätter Kfz-Technik Lernfeld 9-14
ju 15-12-22 Datenbus
+------------------------------>

Quelle: Fabian Lindenberg, Kfz-Technik einfach erklärt [^1]

[^1]: <https://www.youtube.com/watch?v=0a33FFpn_eM&list=PLJXzCsL6HEwzoI3j8tGLKUHjLx0gTxus8>

**Früher** für jedes Signal eine Leitung $\to$ viele Kabel notwendig, wenn mehrere Steuergeräte auf Sensordaten zugreifen wollen.

**Heute** ein Steuergerät liest die Sensordaten aus und schickt diese auf den Datenbus. *Beispiel* Motordrehzahlsignal wird von folgenden Steuergeräten benötigt: Motor, Getriebe, Kombiinstrument, Klimaanlage, ESP.

**Datenübertragung im Kfz** Ermöglicht den Transport und Austausch von Informationen in Form von Daten und Signalen. 

**Gateway** ermöglicht und überwacht den Datenaustausch zwischen Datenbussysteme mit unterschiedlichen Übertragungsgeschwindigkeiten.

**Vorteile**

1. gemeinsame Nutzung von Sensoren 
1. verbesserte Diagnosefähigkeit 
1. weniger elektrische Leitungen
1. weniger Fehlerquellen

# Datenbusarten

1. **elektrische Einleiter - Datenbussysteme**: LIN (Local Interconnect Network, Master-Slave), Multiplex
    - Übertragungsart: elektrische Leitung
1. **elektrische Zweileiter - Datenbussysteme**: CAN (Controller Area Network), Flexray, Ethernet
    - Übertragungsart: elektrische Leitung
1. **optische Datenbussysteme**: Glasfaser, MOST 
    - Übertragungsart: Lichtwellen
1. **drahtlose Datenbussysteme**: WLAN, Bluetooth
    - Übertragungsart: Funkwellen (elektromagnetische Wellen, 2,4 GHZ / 5 GHz)

\newpage
# Datenbusstrukturen - Topologie - Netzwerkstruktur

![Datenbusstrukturen, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-6.pdf){width=50%} 

1. **Sternstruktur:** (Gateway / Router $\leftrightarrow$ PC / Handy / Tablet / Drucker usw.)
    - **aktiv** (Ein Steuergerät im Zentrum eine sternförmig aufgebauten Datennetzes ist über Punkt-zu-Punkt-Verbindungen mit dem benachbarten Steuergerät verbunden.), **passiv** (Leitungsknoten in der Mitte)
1. **Daisy-Chain:** Steuergeräte sind wie die Glieder einer Kette/Reihe aneinander gereiht. (Gateway $\to$ PC $\to$ PC $\to$ PC $\to$ TV)
1. **Busstruktur / Linear:** CAN-Bus (Datenbusleitung, Knotenpunkte, $SG_1 \Longleftrightarrow SG_2 \Longleftrightarrow SG_3 \Longleftrightarrow SG_n$)
1. **Ringstruktur** (Most) Nachteil: Bei fehlerhaften Lichtwellenleiter oder Steuergerät fällt die gesamte Kommunikation aus.
1. **Hybrid** (mehrere Busse, Stern-Bus oder Stern-Ring)
1. **Maschen** (hohe Ausfallsicherheit)

*Bemerkung:* Datenbusleitungen sind miteinander verdrillt (twisted pair), um elektromagnetische Auswirkungen  von einem auf den anderen Draht zu minimieren. Durch die gegensätzliche Spannungsänderung heben sich die bei jeder Umschaltung entstehenden Magnetfelder beider Leitungen gegenseitig auf. Die Leitungen sind nach außen elektromagnetisch neutral. (**EMV** Elektromagnetischen Verträglichkeit)

\newpage
# Klassifikation von Bussystemen

**Nenne Merkmale des CAN-Datenbus** 

1. **Klasse A**
    - LIN bis 10 kBit/s
    - Vernetzung von Aktoren und Sensoren

1. **Klasse B** (Lowspeed-CAN, CAN-B, Komfortbereich)
    - bis 125 kBit/s
    - **Eindrahtfähig**  Datenkommunikation ist gegeben, auch wenn eine Busleitung ausfällt
    - keine Abschlusswiderstände 
    - **Dominanter Pegel 0** low: 1,4 V und high: 3,6 V (Quelle: Bosch S.1693, 30. Auflage)
    - **Rezessiver Pegel 1** low: 5 V und high: 0 V 

1. **Klasse C** (Highspeed-CAN, CAN-C, Antriebs- und Fahrwerkbereich)
    - Datenrate bis 1 MBit/s
    - Nicht Eindrahtfähig
    - Abschlusswiderstand im Steuergerät
    - Leitungen sind verdrillt
    - CAN-High
    - CAN-Low
    - keine Potenzialverteiler
    - oder Potenzialverteiler mit Abschlusswiderständen
    - **Dominanter Pegel 0** low: 1,5 V und high: 3,5 V (Quelle: Bosch S.1693, 30. Auflage)
    - **Rezessiver Pegel 1** low: 2,5 V und high: 2,5 V 

1. **CAN FD** (Flexible Data)
    - bis ca. 8 MBit/s
    - Erst wenn die Daten kommen, wird die Geschwindigkeit hoch geschaltet.

1. **Klasse C+**
    - FlexRay bis 10 MBit/s
    - Antriebs- und Fahrwerkbereich

1. **Klasse D**
    - MOST, Ethernet ab 10 MBit/s
    - Telematik-, Multimediabereich

**Multi-Master** Alle Steuergeräte sind gleichberechtigt. Regelung erfolgt nach Priorität.

**Autonomes Fahren** Drive-by-Wire (alle sicherheitsrelevanten Bauteile sind zweifach ausgelegt und zwei Bussysteme)

\newpage
# Aufbau CAN-Bus

Steuergerät sendet Nachricht auf den Datenbus. 

![Aufbau CAN-Datenbus, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-2.pdf){width=60%} 

![Aufbau-elektrisches-CAN-Datenbussystem, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-3.pdf){width=60%} 

**Steuergerät** (Knoten, Busteilnehmer)

1. **Microprozessor** verarbeitet die eingehenden Informationen, berechnet die Funktionen und steuert die Aktoren.

1. **Controller** filtert die für das Steuergerät notwendigen Daten und übermittelt sie dem Mikroprozessor.

1. **Transceiver** empfängt und sendet die Daten auf der Busleitung. Transmitter (Sender), Receiver (Empfänger)

\newpage
**Spannungspegel der CAN-Datenübertragung**

Beim CAN-Bussystem werden die Informationen durch Spannungsänderungen in der Datenleitung übertragen. Dadurch empfangen alle Steuergeräte gleichzeitig die Informationen. Die Bits werden nacheinander übertragen (seriell).

**Zwei Leitungen**

1. **High-Leitung** Beim Wechsel von rezessiven (Bit = 1) zum dominanten (Bit = 0) Pegel steigt die Spannung.
1. **Low-Leitung** Beim Wechsel vom rezessiven (Bit = 1) zum dominanten (Bit = 0) Pegel sinkt die Spannung.


![Spannungspegel, Quelle: Bosch](images/CAN-Bus/CAN-Bus-11.pdf){width=40%} 

**Steuern** "dominant" 0 überschreibt immer "rezessiv" 1 (tritt zurück) 

(dominant hat Vorrang, dann Datenübertragung)

\newpage
# Aufbau CAN-Nachricht - Datenprotokoll

Das Datenprotokoll bestimmt den Aufbau der Datenbotschaft und ist einheitlich festgelegt.

![Aufbau CAN-Botschaft, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-1.pdf){width=60%} 

1. Anfangsfeld (1 Bit)
    - Beginn der Botschaft
1. Statusfeld (11 Bit) Identifier
    - Botschaftsname (Beispiel: Motordaten)
    - Je niedriger die Zahl, desto wichtiger die Nachricht.
    - höchste Priorität vs. geringste Priorität
    - wichtige Daten vs. weniger wichtige Daten
1. RTR (1 Bit) Remote Transmission Request Feld
    - **0** Senden und **1** Gib mir Daten
1. Kontrollfeld (6 Bit)
    - Enthält Prüfsumme
1. Datenfeld (max. 64 Bit) 
    - Motordrehzahl, Motormoment, Motortemperatur usw.
1. Sicherungsfeld (16 Bit) 
1. Bestätigungsfeld (2 Bit)
1. Ende (7 Bit)
    - der Nachricht, Bus wieder frei

\newpage
# Binärzahlen umwandeln

**Was ist die kleinste Informationseinheit bei der Datenübertragung?** Bit

**Wie viele Informationen können mit einem Bit übertragen werden?** Es können zwei Informationen übertragen werden.

```
// Beispiel: 8 bit = 256 (Anzahl der Informationen)
1 Bit = 0,1 2^1 = 2
2 Bit = 00,01,10,11 2^2 = 4
3 Bit = 000,001,011,111,110,100,101,010 2^3 = 8
1 Byte = 8 bit
2^8 = 256
2^16 = 65536 
```

**Zweier Potenzen** 

$2^0 = 1 \\ 2^1 = 2 \\2^2 = 4 \\2^3 = 8 \\2^4 = 16 \\2^5 = 32 \\2^6 = 64 \\2^7 = 128 \\2^8 = 256$

**Binär in Dezimal** 

```
 1 0 1 1 1 // Binärzahl (5-stellig)
16 8 4 2 1 // 2-Potenz
16 0 4 2 1 // Addieren
__________
Dezimal: 23
```

**Dezimal in Binär**

```
Dezimal: 99
Test 99 < 128        // also 7-stellige Binärzahl
64 32 16  8  4  2  1 // 2-Potenz
64+32                // Addieren
96             +2 +1 
 1  1  0  0  0  1  1 // Binärzahl 
```

\newpage
# Fehler am CAN-Bus

Messung am OBD-Stecker direkt machen.

**Messpunkte** CAN-High (PIN 6) und CAN-Low (PIN 14)

**Gutbild** (CAN-Low-Signal & CAN-High-Signal sind spiegelverkehrt)

![CAN-Bus, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-4.pdf){width=40%} 

1. Signal CAN - High
1. Signal CAN - Low
1. Einstellung Spannung/Division Kanal1
1. Einstellung Spannung/Division Kanal2
1. CAN-Low, rezessiver Pegel, Bit 1
1. CAN-Low, dominanter Pegel, Bit 0
1. CAN-High, rezessiver Pegel, Bit 1
1. CAN-High, dominanter Pegel, Bit 0

![Fehlermöglichkeiten CAN-Bus, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-10.pdf){width=40%} 

![Fehler CAN-Bus, Quelle: Europa-Verlag](images/CAN-Bus/CAN-Bus-5.pdf){width=80%} 

\newpage
## Keine Kommunikation zum SG möglich

1. CAN-High überprüfen
    - **Messpunkt:** Oszi an (Pin6 & Masse)
1. CAN-Low überprüfen
    - **Messpunkt:** Oszi an (Pin14 & Masse)

**kein Spannungsverlauf?**

- Beide Leitungen durchmessen 
- CAN-High (SG gegen Masse)
- CAN-Low (SG gegen Masse)




