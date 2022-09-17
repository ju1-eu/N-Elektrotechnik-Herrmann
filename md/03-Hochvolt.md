---
title: 'Hochvolt'
author: ''
date: \today
subject: "Markdown"
keywords: [Markdown]
lang: "de"
bibliography: literatur-kfz.bib 
csl: zitierstil-number.csl
---
<!-----------------------------
Quelle: Europa-Verlag SimKfz
![, Quelle: Europa-Verlag SimKfz](images/HV/.png){width=70%}
ju 15-9-22 Hochvolt
+------------------------------>

**Reichweite Batterie** $\sim 770~km$ (MERCEDES EQS (2021) - S-KLASSE [^1] (Stand: Mai/2022)         

[^1]: <https://www.auto-motor-und-sport.de/>)

**Spannung Bordnetz** $400~V - 800~V$ (Porsche Taycan, Audi e-tron)

**Batterie laden (Möglichkeiten)** 

- AC (Wechselstrom) 230 V (1-Phase), umwandeln in Gleichstrom ($3,7~KW/h$)
    - Ladestecker: Typ-2-Ladekabel mit ICCB
- AC (Wechselstrom) 380 V (3-Phasen), umwandeln in Gleichstrom ($11 \dots 22~KW/h$) 
    - Ladestecker: Typ-2
- DC (Gleichstrom) 
    - Ladestecker: CHAdeMO ($50~KW/h$) / CSS ($50 \dots 350~KW/h$)

**Was ist ein Hybridfahrzeug? Hybrid-Vehicle (HV)** ist mit mindestens zwei unterschiedlichen Energiewandlern und -speichern für den Antrieb des Fahrzeuges  ausgestattet.

Beispiel: Verbrennungsmotor und Kraftstofftank & E-Motor und HV-Batterie

**Was ist Hochvolt?** Ab einer Wechselspannung von AC > 30 V und einer Gleichspannung von DC > 60 V. 

**IT-Netz** IT steht für isoliert und Terra (von der Erde isoliertes System): Das HV-System ist sowohl wechsel- als auch gleichstromseitig von der Fahrzeugmasse galvanisch getrennt oder isoliert (nicht geehrtes Stromnetz).

**Rekuperation (Regeneration)** Bremsenergierückgewinnung, Bremsenergie wird in elektrische Energie umgewandelt. 

**Range-Extender** Reichweiten verlängern

**Boost** Drehmomentunterstützung


# Was sind HV-eigensichere Fahrzeuge?

Für den Benutzer durch technische Maßnahmen ein vollständiger Berühr- und Lichtbogenschutz gegenüber dem HV-System gewährleistet ist.

- System überwacht sich selbst
- Serienfahrzeug (Direkt vom Hersteller auf die Straße)
- Sicherheitslinie (Pkw)
- **Außer:** Lkw, Busse, Eigenbau (Vorsicht beim Umrüsten und Nachrüsten), Unfallfahrzeug


# Qualifikationsstufen 

Jeder **Gewerbetreibende** benötigt die Stufe-S, um ein HV-Fahrzeug bewegen zu dürfen. 

**Unterweisung** einmal jährlich für Gesellen und halbjährlich für Lehrlinge. $\to$ Person sensibilisieren auf jedes Fahrzeug einzeln.

**Wie heißt die neue Sicherheitsverordnung?**

DGUV 209-093 (Deutsche gesetzliche Unfallversicherung) Qualifizierung für Arbeiten an Fahrzeugen mit HV-Systemen.

## Qualifikationsstufen

- **Stufe S** sensibilisierte Person (Bedienen von Fahrzeugen mit HV-System)

- **Stufe 1S** fachkundige unterwiesene Person (Motto: Hände weg von Orange!)

- **Stufe 2S** fachkundige Person (alle arbeiten, aber nicht unter Spannung, Freischalten) 

- **Stufe 3S** fachkundige Person -- für Arbeiten unter Spannung stehenden HV-System (Energiespeicher öffnen), erste Hilfe-Schein


**Welche Qualifikationen sind für folgende Arbeiten notwendig?** 

1. **VW E-Golf kommt zum Räderwechsel**
    - Fachkundige unterwiesene Person
1. **Lehrling soll VW E-Golf in eine andere Filiale fahren**
    - Sensibilisierte Person
1. **Beim Smart ED soll der Klimakompressor getauscht werden**
    - Fall 1: Wenn nicht freigeschaltet ist $\to$ Stufe 2S
    - Fall 2: Wenn freigeschaltet ist $\to$ Stufe 1S + Klimaschein
1. **Tesla Model S braucht eine neue HV-Batterie**
    - Fachkundige Person
1. **Nach Unfall lässt sich Mercedes Vito E-Cell nicht mehr über Service-Disconnect-Stecker spannungsfrei schalten**
    - Fachkundige Person -- für Arbeiten unter Spannung stehenden HV-System

# Erkläre das Freischalten des HV-Systems?

Kunde kommt mit E-Auto in die Werkstatt. Was passiert jetzt?

Beginn Gefahrübergang: mit Schlüsselübergabe + Normalauftrag (Garantieauftrag) unterschrieben.

**Probefahrt** ja der Fehler ist aktuell.

Vorgaben des Herstellers beachten!

1. Blitzhütchen "Hochvolt" mit Magnet aufs Dach
1. Fahrzeug in Werkstatt fahren
    - fester Platz für HV-Fahrzeug
    - HV-Werkzeug, Rettungshaken, Feuerlöscher, Defibrillator (Herzrhythmusstörung beseitigen, Stromstoß)
1. Abschranken 
    - Gefahren absperren im Abstand 1,50 m um das Fahrzeug herum
    - Bedeutung von gelb/schwarzes Band - langfristig oder rot/weiß Band - kurzfristig
1. Hinweisblatt rot "Hochvolt-Spannungen sind eingeschaltet" auf die Windschutzscheibe kleben, mit Namen und Telefonnummer
1. Diagnosetester - Fehlerspeicher auslesen
1. Zündung ausschalten und Zündschlüssel entfernen (mind. 10 m Entfernung) und wegschließen
1. Sicherheitshandschuhe prüfen und anziehen, Schutzbrille, lange Kleidung ohne Reißverschluss (Vgl. Körperwiderstand)
1. Minuspol der 12 V-Batterie abklemmen (Motorhaube, Türen und Kofferraum vorher öffnen)
1. Warten 5 Minuten $\to$ bis Kondensatoren sich entladen von Bordnetz und HV-System
    - Sicherheitslinie wird geöffnet
    - Trennrelais öffnen und schalten Spannung ab
    - Kondensatoren entladen sich
1. Service-Disconnect-Stecker der HV-Batterie abziehen, falls nicht vorhanden, Sicherheitslinie unterbrechen
1. Zündschlüssel und Disconnect-Stecker wegschließen (mind. 10 m Entfernung) und Fahrzeug gegen Wiedereinschalten sichern
1. Messen mit dem Duspol (geeignetes Messgerät auswählen, Zweipoliger Spannungsprüfer)
    - Messgerät an sicherer Spannungsquelle überprüfen: Hochspannungsbereich 230 V-Steckdose, Niederspannungsbereich 12 V-Batterie
    - Spannungsfreiheit überprüfen: am Inverter alle drei Phasen messen
    - Messgerät nochmals überprüfen (gleiche Spannungsquelle)
    - Spannungsfreiheit festgestellt
1. Protokoll über die Freischaltung führen (Was wurde gemacht? Wie wurde das Fahrzeug übergeben?)
1. Hinweisblatt weiß "Hochvolt-Spannungen sind sicher ausgeschaltet" auf die Windschutzscheibe kleben, mit Namen und Telefonnummer
1. Jetzt kann gearbeitet werden.

**HV-Interlock** Pilotlinie, Sicherheitslinie (überwacht die HV-Steckverbindungen)

## Wie hoch ist der Körperwiderstand ab einer Spannung von 100 V?

Berührung der beiden Batteriepole

- $1000~\Omega$ von Hand-zu-Hand oder Hand-zu-Fuß
- $450~\Omega$ von Hand-zu-Brust
- $\text{Körperstrom} = \frac{400~V}{1000~\Omega} = 400~mA$ der absolut tödlich wäre.

Ein Strom von beispielsweise $50~mA$ kann zur Muskelverkrampfung führen, sodass sich die Person nicht mehr selbstständig von der Spannungsquelle lösen kann. Schon nach wenigen Sekunden könnte es auch bei niedrigen Strömen zu tödlichen Unfällen kommen. (Einwirkzeit)

**Wovon hängt es ab, welche Schäden der elektrische Strom im menschlichen Körper verursacht?**

- der Stromstärke und
- der Zeit, für die der Strom den Körper durchfließt

## Sicherheitshandschuhe prüfen

- vor jedem Freischalten
- Handschuh aufdrehen und auf Dichtheit prüfen oder Prüfgerät
- keine Verfärbung oder Punkte
- Aufdruck vollständig

Sicherheitsklasse 0 sind bis 1000 V zugelassen.

# Elektromotoren - Drehstrommotor

Sind bürstenlose Motoren (d. h. keine Kohlestifte = Kohlebürsten; kein Schleifring).

**Drehstrommotor** wird mit Dreiphasenwechselspannung betrieben, der in drei Leitern eine periodisch um 120° versetzte Spannung anlegt. Dadurch werden in den Statorspulen Magnetfelder induziert, die eine Bewegung im Rotor erzeugen. Ein umlaufendes Magnetfeld nimmt einen magnetischen Rotor mit, sodass es zu einer Drehbewegung kommt.

- **Stator** steht
- **Rotor** dreht sich

**Was ist ein Drehfeld?**

Ein Magnetfeld das um den Rotor wandert (rotierendes Magnetfeld).

## Synchronmotor (Prüfung)

Der Frequenzumrichter legt eine Dreiphasenwechselspannung an die Erregerspulen. Das dadurch erzeugte magnetische Drehfeld des Stators setzt den Rotor in Bewegung.

PSM (Permanenterregt)

- **Stator** elektromagnetische Spule wird bestromt und es entsteht ein Drehfeld
- **Rotor** Magnetfeld wird erzeugt durch Dauermagnet, der vom Drehfeld direkt mitgenommen wird.
- Stator = Rotor (Drehzahl, mit gleicher Geschwindigkeit)
- Ansteuerung: über Inverter / IGBTs

FSM (F‚remderregt)

- **Stator** elektromagnetische Spule 
- **Rotor** Magnetfeld wird erzeugt durch Fremderregung, elektromagnetische Spule 

## Asynchronmotor (Prüfung)

Das Magnetfeld des Rotors muss erst erzeugt werden. 

ASM (Induktionsmotor)

- **Stator** elektromagnetische Spule 
- **Rotor** Kurzschlussläufer (Bauform, Käfigläufer), die Enden der Spulen werden gemeinsam verbunden. Die induzierte Spannung wird kurzgeschlossen und es fließt ein hoher Strom, der das Magnetfeld erzeugt. 
- Stator $\neq$ Rotor (Drehzahl, nicht mit gleicher Geschwindigkeit)
- Stator = Rotor (Kraft NULL)

Die Drehzahl wird über die Frequenz des Erregerfeldes eingestellt. 

**Schlupf** unterschied zwischen Rotordrehzahl und Drehzahl des Erregerfeldes.  Asynchronmotoren laufen immer etwas langsamer als das angelegte Erregerfeld.

# HV-Komponenten

1. **HV-Batterie** Lithium-Ionen, Nickel-Metallhydrid
1. **DC/DC-Wandler** (Konverter, Gleichstromwandler) Spannungswandler zwischen HV-Netz und 12-V-Bordnetz
1. **Inverter** (Pulswechselrichter) 
    - Leistungselektronik
        - Umwandlung DC $\to$ AC, Gleichrichten AC $\to$ DC
        - Laden der HV-Batterie 
        - Antrieb der Motorgeneratoren (MG, E-Maschine) und Klimakompressor
        - **IGBT** (Aufbau: Mosfet + Bipolarer Transistor), Wie? $\to$  Mit PWM-Signal werden die Spulen der Elektromotoren angesteuert. Durch eine Frequenzweitenmodulation lässt sich die Frequenz des Wechselstroms verändern.
1. **Ladeelektronik** Batterie-Balancing 
    - Aktiv Balancing (Ladungsausgleich der einzelnen Batteriezellen)
    - Passiv Balancing, wenn Zelle bei 100 \%, dann über Widerstand (Wärme)
1. **Batteriemanagementsystem** (BMS) Batterieüberwachung
1. **E-Maschine** (E-Motor / Generator)

**Energiefluss**

1. **Elektroantrieb** HV-Batterie - Inverter - E-Motor
1. **Generatorbetrieb** Generator - Gleichrichter - HV-Batterie
1. **Bordnetzversorgung** MG - DC/DC Wandler - 12-V-Batterie
1. **AC-Laden** Ladesteckdose - Gleichrichter - HV-Batterie

# Hauptrelais oder Trennrelais oder Sicherheitsrelais

**Einschalten der Zündung und betriebsbereiten Zustand**

- Relais 3 ($\text{HV}_-$) und Relais 1 ($\text{HV}_+$) mit Widerstand (begrenzter Stromfluss für Kondensatoren) geschlossen und Relais 2 offen
- Lädt die  Kondensatoren auf
- Isolationsprüfung (Isolationsfehler oder Stecker ab $\to$ Sicherheitslinie offen)
- Fahrbereit

**Ausschalten der Zündung** trennen die Relais die HV-Spannung vom HV-Netz