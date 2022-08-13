---
title: 'Grundlagen - Elektrotechnik II'
author: ''
date: \today
subject: "Markdown"
keywords: [Markdown]
lang: "de"
bibliography: literatur-kfz.bib 
csl: zitierstil-number.csl
---
<!-----------------------------+
ju 13-8-22
Keywords - Sensoren und Aktoren
+------------------------------>

**Sensoren** erfassen physikalische Effekte (Druck, Temperatur) und wandeln diese in elektrische Signale um. (Sinne des Autos) 

**Aktoren** wandeln elektrische Spannungssignale in physikalische Effekte um (Stellglieder, Ausführen). 

# Pulsweitenmodulation

1. **PWM-Signal:** Rechtecksignal (vgl. Kennlinie)

1. **Messen:** Oszilloskop

1. **Ansteuerung:** $0 - 100~\%$, Impuls-Pause-Verhältnisänderung (nur Pulsweite ändert sich), aber Periodendauer / Frequenz bleibt konstant (keine Spannungsänderung!)

1. **Anwendung**
    - Elektromotor (Drehzahl)
    - Glühlampen (Helligkeit, dimmen)
    - Beleuchtung, Beispiel: Einfaden-Glühlampe (Standlicht + Bremslicht)

Die **Pulsweitenmodulation** (PWM) ist eine digitale Modulationsart, bei der eine technische Größe zwischen zwei Werten (Spannungspegel $0~V$ und VCC) wechselt. Dabei wird bei konstanter Frequenz ein Rechtecksignal moduliert, das in Pulsweite (*oder* Breite bzw. Länge) variiert. Das Verhältnis zwischen Impuls und Pause (Ein- und Ausschaltzeit) wird als **Tastgrad / Tastverhältnis** bezeichnet. **Anwendung** in der Steuer- und Regelungstechnik.


# Halbleiter

**Halbleiter** ist ein kristalliner Stoff, der sich bei tiefen Temperaturen wie ein Isolator verhält und bei höheren Temperaturen nimmt die elektrische Leitfähigkeit zu. Der Widerstand ist temperaturabhängig.

**Halbleiterwerkstoffe**

- **Metalle** Beispiel: Eisen, Kupfer
- **Isolierstoffe** Beispiel: Kunststoff
- **Halbleitermaterial** Beispiel: reines Silizium / Germanium **Anwendung** Beispiel: Diode, Transistor

**Dotieren** reines Silizium / Germanium wird verunreinigt, um die elektrische Leitfähigkeit zu verbessern.

**P-Leiter und N-Leiter**

1. **P-Leiter** entsteht, wenn das Leitermaterial Silizium verunreinigt wird mit Bohr und bei *Elektronenmangel* enthält es freie positive Ladungen. Löcherstrom

2. **N-Leiter** entsteht, wenn das Leitermaterial Silizium verunreinigt wird mit Phosphor und bei *Elektronenüberschuss* enthält es freie negative Ladungen. Elektronenstrom

$\to$ Legt man an den Halbleiterkristall eine elektrische Spannung an, dann kommt es zum Elektronenfluss, weil die Elektronen versuchen sich auszugleichen.


# Halbleiterwiderstände NTC und PTC

1. **Heißleiter** $\to$ NTC-Widerstände bis $250^\circ\text{C}$
    - *negativer Temperatur-Koeffizient* $\to$ fallender Widerstand bei steigender Temperatur $\uparrow \downarrow$ 
    - vgl. Kennlinie (x = Temperatur, y = Widerstand) 
    - **Anwendung:** Temperatursensoren (Kühlmittel-, Kraftstoff-, Luft-, Motortemperaturfühler)
    - Schaltsymbol
    - typische Werte: Kalt: $2 - 4~k\Omega$ und Warm: $200 - 400~\Omega$
    - *Leitfähigkeit* steigt mit zunehmender Temperatur 
    - Widerstand und Spannungsfall am NTC werden kleiner 

1. **Kaltleiter** $\to$ PTC-Widerstände bis $950 - 1000^\circ\text{C}$
    - *positiver Temperatur-Koeffizient* $\to$ zunehmender Widerstand bei steigender Temperatur $\uparrow \uparrow$ 
    - vgl. Kennlinie (x = Temperatur, y = Widerstand) 
    - **Anwendung:** Hochtemperaturbereich (Diesel-Abgastemperatursensoren), Glühkerzen, Heizungen von Lambdasonden
    - Schaltsymbol
    - *Leitfähigkeit* verringert sich mit zunehmender Temperatur
    - Widerstand und Spannungsfall am PTC werden größer 
    - "Je höher der Widerstand, desto geringer der Stromfluss."
