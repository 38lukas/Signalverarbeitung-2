# Student Information

|                   |                             |
|-------------------|-----------------------------|
| Name              | Lukas Stieneke              |
| Matrikelnummer    | 222754                      |
| Studiengang       | SEB3                        |
| Kurs              | SV2                         |
| Betreuer          | Prof. Dr. supervisor        |
| Akademisches Jahr | 2025/2026                   |

---
# Aufgabe 1 – Resonanzfrequenz des Reihenschwingkreises

## Aufgabenstellung
Verifizieren Sie die Resonanzfrequenz eines Reihenschwingkreises anhand einer theoretischen Berechnung und einer praktischen Simulation im Falstad-Simulator.

## 1. Berechnung
Berechnen Sie zuerst die theoretische Resonanzfrequenz f₀ mit der Formel von Folie 5 und den gegebenen Werten.

f₀ = 1 / (2π√(LC)) = 1/(2π√())
eingesetzt:  1/(2π√(10*10^-3 * 100*10^-9)) = 5032.92121045Hz

## 2. Simulation
Bauen Sie die Schaltung auf. Finden Sie im Simulator die Frequenz, bei der der Strom I maximal ist.


## 3. Dokumentation
Notieren Sie die Frequenz, die Sie im Simulator gemessen haben.

Die Frequenz, bei der der Strom I maximal ist, ist um 5kHz


## 4. Vergleich
Vergleichen Sie Ihren Rechenwert (aus 1.), Ihren Messwert (aus 3.) und den Wert auf Folie 7. Was stellen Sie fest?

Man kann deutlich erkennen, dass Rechenwert und der Messwert fast gleich sind. Zum Wert aus Folie 7 kann man sagen, das andere Bauteile verwendet wurden und somit natürlich andere Werte entstehen

---
# Aufgabe 2 – Güte und Dämpfung visualisieren

## Aufgabenstellung
Untersuchen Sie den Einfluss des Widerstands R (Dämpfung) auf die Schärfe der Resonanzkurve (Güte Q), wie auf Folie 9 dargestellt.

## 1
Finden Sie eine Methode in der Simulationssoftware, um den Frequenzgang des Stroms sichtbar zu machen.

## 2
Stellen Sie den Widerstand R so ein, dass Sie ihn interaktiv verändern können

## 3
Dokumentieren Sie durch ein GIF, wie sich die Form der Resonanzkurve (die "Peak-Form") ändert, wenn Sie R von einem sehr kleinen Wert (z.B. 5 Ω) zu einem großen Wert (z.B. 300 Ω) ändern.

## 4
Erklären Sie den Zusammenhang, den Sie beobachten:
1. Was passiert mit der Höhe des Peaks?
2. Was passiert mit der Breite des Peaks?
3. Was bedeutet das für die Güte Q und die Bandbreite der Schaltung (vgl. Folie 9)?

---

1. Mit zunehmendem Widerstand wird der Resonanz-Peak niedriger. Der maximale Strom bzw. die maximale Amplitude nimmt also ab, da der     Widerstand mehr Energie im Schwingkreis dämpft.
2. Mit zunehmendem Widerstand wird der Resonanz-Peak breiter. Die Resonanz ist weniger stark ausgeprägt und verteilt sich über einen größeren Frequenzbereich.
3. Ein kleiner Widerstand führt zu einer hohen Güte Q und einer schmalen Bandbreite, da die Schaltung nur in einem engen Frequenzbereich stark schwingt.
Mit steigendem Widerstand sinkt die Güte Q, während die Bandbreite zunimmt, weil die Dämpfung größer wird und die Resonanz weniger scharf ist.
---
# Aufgabe 3 - Bandpass vs. Bandsperre

## Aufgabenstellung
Verstehen Sie den fundamentalen Unterschied zwischen einem Bandpassfilter und einem Bandsperrfilter (siehe Folie 12). Beide nutzen dieselben L/C-Werte, haben aber gegensätzliche Funktionen.

## 1
Bauen Sie beide Schaltungen im Simulator auf.

## 2
Berechnen Sie zuerst die erwartete Resonanzfrequenz f₀ (Thomsonsche Formel).

Formel: f₀ = 1 / (2π√(LC))
Eingesetzt: 1/(2π√(1*10^-3 * 10*10^-9)) = 50329.2121045Hz

## 3
Simulieren Sie den Frequenzgang der Ausgangsspannung für beide Schaltungen

## 4
Dokumentieren Sie Ihre Ergebnisse durch GIFs, die den Frequenzgang beider Schaltungen zeigen.

## 5
Beantworten Sie die folgenden Fragen:
1. Bestätigt Ihre Simulation die berechnete Resonanzfrequenz?
2. Beschreiben Sie präzise das gegensätzliche Verhalten der beiden Schaltungen bei dieser Frequenz.
3. Erklären Sie Warum führt Aufbau 1 (Parallelschwingkreis als Ausgang) zu einem Spannungsmaximum, während Aufbau 2 (Reihenschwingkreis parallel zum Ausgang) zu einem Spannungsminimum führt?

---

1. Die Simulation bestätigt die berechnete Resonanzfrequenz, da das beobachtete Resonanzmaximum sehr nahe am theoretischen Wert liegt. Kleine Abweichungen sind auf Rundungen der Bauteilwerte zurückzuführen.
2. Bei der Bandpass-Schaltung erreicht die Ausgangsspannung bei der Resonanzfrequenz ein Maximum, während sie bei der Bandsperr-Schaltung an derselben Frequenz ein Minimum annimmt.
3. Der Unterschied ergibt sich aus dem Impedanzverhalten der Schwingkreise. Beim Parallelschwingkreis ist die Impedanz bei der Resonanzfrequenz maximal, wodurch die Ausgangsspannung groß wird. Beim Reihenschwingkreis ist die Impedanz dagegen minimal, was zu einem Spannungsminimum am Ausgang führt.

---
# Aufgabe 4 - Der 3-Bit D/A-Wandler (R-2R-Netzwerk)

## Aufgabenstellung
Verstehen Sie das Grundprinzip eines Digital-Analog-Wandlers (DAC). Wie auf Folie 30 und Folie 31 konzeptionell gezeigt, ist dies der umgekehrte Prozess zur Abtastung.

## 1
Bauen Sie das R-2R-Netzwerk im Simulator auf.

## 2
Stellen Sie nacheinander alle 8 Binärkombinationen (von 000 bis 111) mit den drei Schaltern ein.

## 3
Messen Sie für jede Kombination die resultierende analoge Ausgangsspannung Uaus (Tipp: der "DC Level" im Scope) und füllen Sie die folgende Tabelle aus.

## 4
Dokumentieren Sie durch ein GIF, wie sich die Ausgangsspannung ändert, wenn Sie die Binärkombinationen durchschalten.

## Auswertung

1. Analysieren Sie Ihre Messwerte. Was stellen Sie fest?
2. Berechnen Sie die Spannungsdifferenz (die "Schrittgröße") zwischen den einzelnen Dezimalwerten (z.B. die Differenz zwischen Wert 1 und Wert 2). Ist diese Schrittgröße konstant?
3. Erklären Sie, warum die Schaltung das tut, was auf Folie 30 (Quantisierung/Treppenstufen) gezeigt wird.

---

1. Beim Betrachten der Messwerte fällt auf, dass der Spannungsanstieg nicht gleichmäßig verläuft. Die Spannung steigt also nicht linear mit den einzelnen Schritten.
2. Berechnung der Schrittgrößen:
| Übergang  | Schrittgröße (V) |
|-----------|------------------|
| 0 → 1     | 3.3              |
| 1 → 2     | 0.7              |
| 2 → 3     | 0.8              |
| 3 → 4     | 0.2              |
| 4 → 5     | 1.0              |
| 5 → 6     | 0.3              |
| 6 → 7     | 0.3              |
Fazit: Einige Übergänge verändern die Spannung stärker als andere.
3. Die Schaltung verwendet Widerstände und drei Schalter (3 Bits), um bestimmte Spannungen zu erzeugen. Dadurch entstehen stufenartige Werte („Treppenstufen“), wie auf Folie 30 gezeigt, die z. B. für Pulsamplitudenmodulation genutzt werden können.

---

# Aufgabe 5 - Filterung von Obertönen (Rechteck-zu-Sinus-Wandler)