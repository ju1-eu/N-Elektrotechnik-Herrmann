---
title: 'Generator'
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
![, Quelle: Europa-Verlag](images/Generator/.png){width=70%}
ju 6-10-22 Generator
+------------------------------>
**Drehstromgenerator / Lichtmaschine / Generator**

Quelle: Fabian Lindenberg, Kfz-Technik einfach erklärt [^2]

[^2]: <https://www.youtube.com/watch?v=O7ydsAZ6bes>

# Komponenten

1. **Regler** (Multifunktionsregler hat keine Erregendioden, bekommt Spg. von Kl.30)
1. **Schleifringe**
1. **Gleichrichterdioden** (Leistungsdioden)
1. **Klauenpolläufer** (mit Riemenscheibe $\to$  Antrieb Motor und Schleifringe $\to$ Regler) 
1. **Erregerwicklung** (Rotor, dreht sich, sitzt im Klauenpolläufer)
1. **Ständerwicklung** (mit Gehäuse, Stator, steht)
1. **Lüfter**

**Diodenplatte:** 6x Gleichrichterdioden (3x Plusdioden, 3x Minusdioden), 3x Erregerdioden

**Klauenpolläufer** 12 Pole (je 6 Nord- und Südpole) x 3 Statorspulen = 36 Halbwellen = 1x Umdrehung. Batterie und Kondensator glättet die Gleichspannung.

![Generatoraufbau - Drei Ständerwicklungen U,V,W und ein Polrad](images/Generator/Generator-11.pdf){width=40%} 

![3 Wechselspannungen mit 120° Phasenverschiebung](images/Generator/Generator-8.pdf){width=40%} 

# Multifunktionsregler

![Schaltung Generator mit Multifunktionsregler, Quelle: Europa-Verlag](images/Generator/Generator-1.pdf){width=85%} 

**Merkmale**

1. Unterstützung Motormanagement
1. Batterieüberwachung
1. Auslastungsüberwachung
1. Temperaturabhängige Ladespannung
1. Schutz gegen Überlastung / Kurzschluss
1. Interne Fehlerdiagnose $\to$ SG
1. Vorerregerstrom Steuern (Dreht sich der Generator)
1. Low-Response (Start & Fahrt: Belastung des Generators wird verzögert zugeschaltet, Kraftstoff sparen)

\newpage
# Generator prüfen

**Ladekontrolle an**

- Zündung an, Motor steht
- Erregungsunterbrechung
- Überspannung
- Keilriemen gerissen
- Leitungsunterbrechung
- Defekte Masseverbindung

**Generator Anschluss**

1. **W** Drehzahl
1. **B-** Masse
1. **D+** Ladekontrolle, Erregerwicklung
1. **B+** Batterie
1. **DF** Regler, Erregerwicklung

**Generator mit Multifunktionsregler Anschluss**

1. **L** Ladekontrollleuchte
1. **S** Sense, Batterie überwachen
1. **W** Drehzahlsignal zur Regelung des Vorerregerstroms
1. **V** Phasenspannung überwachen (Fehlerdiagnose, Beispiel: def. Keilriemen erkennen)
1. **DFM** PWM-Signal des Erregerstroms zur Auslastung des Generators

**Erregerspannung und Generatorspannung / Ladespannung messen**

- Unter Belastung (Verbraucher EIN)
- Motordrehzahl (ca. 1800 - 2200 1/min)
- **Erregerspannung** 
    - Messpunkt: (D+ und D-/B-/Masse)
- **Generatorspannung / Ladespannung**
    - Messpunkt: (B+ und D-/B-/Masse)

**Fehler**

1. Oberwelle normal
1. Minusseitig eine Sperrdiode defekt $\to$ Eine Welle wäre weg, Leistung von der Spule fehlt
1. Erregerdiode defekt $\to$ Ladespannung geht runter

![Generator Gutbild, Quelle: Europa-Verlag](images/Generator/Generator-2.pdf){width=40%} 
 

![Generator Fehler - Unterbrechung einer Minusdiode, Quelle: Europa-Verlag](images/Generator/Generator-5.pdf){width=40%} 

\newpage
# Energieumwandlung 

kinetische Energie + elektrische Energie (Drehmoment) $\to$ **Generator** $\to$ elektrische Energie

**Induktion** mit ein Magnetfeld Elektronen bewegen. 

Magnet (Nordpol/Südpol, anziehen / abstoßen)

Rechte-Handregel: Magnetfeld bestimmen

1. Stromdurchflossener Leiter $\to$ erzeugt Magnetfeld
1. Stromdurchflosse Spule $\to$ erzeugt großes Magnetfeld
1. Rotor (Erregerwicklung, Fremderregt) und Stator (mit 3x Spulen, U / V / W) $\to$ erzeugt drehbares Magnetfeld 

**indizierte Spannung** ist abhängig

1. Anzahl Wicklungen von Statorspulen 
1. Drehzahl Generator 
1. Stärke des Magnetfeldes
1. Fläche

![Drehstrom - Brückenschaltung](images/Generator/Generator-6.pdf){width=30%} 

![Gleichrichtung der Generatorspannung](images/Generator/Generator-7.pdf){width=30%} 

\newpage
# Energiefluss

![Energiefluss](images/Generator/Generator-Energiefluss.pdf){width=80%} 

**Erregerwicklung** sitzt im Klauenpolläufer, erzeugt Magnetfeld welches auf die Statorspulen wirkt

**Statorspulen** Sternschaltung, Durch das Magnetfeld der Erregerwicklung wird eine Spannung induziert. 3x Spulen um 120° versetzt $\to$ 3-phasige Wechselspannung

**Leistungsdioden** Richten die 3-phasige Wechselspannung in eine Gleichspannung um.

**Erregerdioden** Spannungsversorgung des Spannungsreglers.

**Spannungsregler** regelt den Erregerstrom und variiert damit die Stärke des Magnetfeldes. **Ladespannung ist Konst.** bei allen Motordrehzahlen (Leerlauf - Vollast) u. Belastungen (Verbraucher). **Wie?** Je stärker das Magnetfeld, desto größer ist die Spannung die in den Statorspulen induziert wird.



\newpage
# Schaltung

![Schaltung Generator mit Transistorregler, Quelle: Europa-Verlag](images/Generator/Generator-9.pdf){width=85%} 

Zündung an, Motor steht

**Vorerregerstromkreis (blau)** B+ $\to$ Fahrtschalter $\to$ Ladekontrolllampe $\to$ D+ $\to$ Erregerwicklung $\to$ Regler DF $\to$ Masse $\to$ B-

Zündung an, Motor läuft

**Erregerstromkreis (grün)** Ständerwicklung $\to$ Erregerdioden $\to$ D+ $\to$ Erregerwicklung $\to$ Regler DF $\to$ Regler D- $\to$ Minusdioden $\to$ Ständerwicklung

**Ladestromkreis (rot)** Ständerwicklung $\to$  Plusdioden $\to$  B+ $\to$ Verbraucher $\to$ Masse $\to$  Minusdioden $\to$ Ständerwicklung


\newpage
![Schaltung Generator mit Multifunktionsregler, Quelle: Europa-Verlag](images/Generator/Generator-10.pdf){width=85%} 

**Vorerregerstromkreis (blau)** B+ $\to$ Erregerwicklung $\to$ Regler DF $\to$ Reglerendstufe $\to$ B-

Zündung an, Motor läuft

**Erregerstromkreis (grün)** Ständerwicklung $\to$ Plusdioden $\to$ Regler B+ $\to$ Regler DF $\to$ Erregerwicklung $\to$ Regler D- $\to$  Regler B- $\to$ Minusdioden $\to$ Ständerwicklung

**Ladestromkreis (rot)** Ständerwicklung $\to$  Plusdioden $\to$  B+ $\to$ Verbraucher $\to$ Masse $\to$  Minusdioden $\to$ Ständerwicklung








