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
Dozent: 
# 
## 
ju 13-8-22 Hochvolt
+------------------------------>

**Reichweite Batterie** $\sim 770~km$ (MERCEDES EQS (2021) - S-KLASSE [^1] (Stand: Mai/2022)         

[^1]: <https://www.auto-motor-und-sport.de/>)

**Spannung Bordnetz** $400~V - 800~V$ (Porsche Taycan, Audi e-tron)

**Batterie laden** 1-Phase ($3,7~Km$), 3-Phasen, Gleichstrom

# Was sind HV-eigensichere Fahrzeuge?

Gewährleisten einen vollständigen Berühr- und Lichtbogenschutz gegenüber HV-System.

- System überwacht sich selbst
- Serienfahrzeug
- Sicherheitslinie (Pkw)
    - **Außer:** Lkw, Busse, Eigenbau (Vorsicht beim Umrüsten und Nachrüsten), Unfallfahrzeug

**IT-Netz** IT steht für isoliert und Terra (von der Erde isoliertes System): Das HV-System ist sowohl wechsel- als auch gleichstromseitig von der Fahrzeugmasse galvanisch getrennt oder isoliert.


# Qualifikationsstufen

Jeder **Gewerbetreibende** benötigt die Stufe-S, um ein HV-Fahrzeug bewegen zu dürfen. 

**Unterweisung** einmal jährlich für Gesellen und halbjährlich für Lehrlinge. $\to$ Person sensibilisieren auf jedes Fahrzeug einzeln.

**Wie heißt die neue Sicherheitsverordnung?**

DGUV 209-093 (Deutsche gesetzliche Unfallversicherung) Qualifizierung für Arbeiten an Fahrzeugen mit HV-Systemen.

**Qualifikationsstufen**

- **Stufe S** sensibilisierte Person (Bedienen von Fahrzeugen mit HV-System)

- **Stufe 1S** Fachkundige unterwiesene Person (Motto: Hände weg von Orange!)

- **Stufe 2S** fachkundige Person (alle arbeiten, aber nicht unter Spannung, Freischalten) 

- **Stufe 3S** fachkundige Person -- für Arbeiten unter Spannung stehenden HV-System (Energiespeicher öffnen)


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

Beginn Gefahrübergang: mit Schlüsselübergabe + Werkstattauftrag unterschrieben

1.  Hütchen mit Magnet aufs Dach $\to$ Achtung Hochspannung! 
1. Fahrzeug in Werkstatt fahren
1. Abschranken 
    - im Abstand $1~m$ um das Fahrzeug herum
    - Gefahren absperren: Bedeutung  von gelb/schwarzes Band - langfristig oder rot/weiß - kurzfristig
1. rotes Schild auf die Windschutzscheibe kleben $\to$ Achtung Hochvolt! Nicht freigeschaltet, mit Namen und Telefonnummer
1. Zündung ausschalten und Zündschlüssel entfernen
1. Sicherheitshandschuhe prüfen und anziehen, Schutzbrille, lange Kleidung ohne Reißverschluss (Vgl. Körperwiderstand)
1. Minuspol der 12 V-Batterie abklemmen
1. Warten 5 Minuten $\to$ bis Kondensatoren sich entladen von Bordnetz und HV-System
    - Sicherheitslinie wird geöffnet
    - Trennrelais öffnen und schalten Spannung ab
    - Kondensatoren entladen sich
1. Service-Disconnect-Stecker der HV-Batterie abziehen, falls nicht vorhanden, Sicherheitslinie unterbrechen
1. Zündschlüssel und Disconnect-Stecker wegschließen (mind. 10 m Entfernung) und sichern gegen wieder einschalten
1. Messen mit dem Duspol
    - Messgerät überprüfen: Hochspannungsbereich 230 V-Steckdose, Niederspannungsbereich 12 V-Batterie
    - Messung durchführen: am Inverter alle drei Phasen messen
    - Messgerät überprüfen (gleiche Spannungsquellen): Hochspannungsbereich 230 V, Niederspannungsbereich 12 V-Batterie
    - Spannungsfreiheit festgestellt
1. Dokumentieren über das Freischalten (Was wurde gemacht? Wie wurde das Fahrzeug übergeben?)
1. weißes Schild auf die Windschutzscheibe kleben $\to$ Fahrzeug ist spannungsfrei, Fahrzeug gegen Wiedereinschalten gesichert, mit Namen und Telefonnummer
1. Jetzt kann gearbeitet werden.

Pilotlinie, Interlock, Sicherheitslinie (Niedervolt)

**Wie hoch ist der Körperwiderstand ab einer Spannung von 100 V?**

Berührung der beiden Batteriepole

- $1000~\Omega$ von Hand-zu-Hand oder Hand-zu-Fuß
- $450~\Omega$ von Hand-zu-Brust
- $\text{Körperstrom} = \frac{400~V}{1000~\Omega} = 400~mA$ der absolut tödlich wäre.

Ein Strom von beispielsweise $50~mA$ kann zur Muskelverkrampfung führen, sodass sich die Person nicht mehr selbstständig von der Spannungsquelle lösen kann. Schon nach wenigen Sekunden könnte es auch bei niedrigen Strömen zu tödlichen Unfällen kommen. (Einwirkzeit)

**Sicherheitshandschuhe prüfen** (rot, bis $1000~V$, vor jedem Freischalten) 

- Handschuh aufdrehen und auf Dichtheit prüfen oder Prüfgerät
- keine Verfärbung oder Punkte
- Aufdruck vollständig