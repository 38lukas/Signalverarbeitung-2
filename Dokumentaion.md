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

### Aufgabenstellung
Verifizieren Sie die Resonanzfrequenz eines Reihenschwingkreises anhand einer theoretischen Berechnung und einer praktischen Simulation im Falstad-Simulator.

### Schritt 1
Berechnen Sie zuerst die theoretische Resonanzfrequenz f₀ mit der Formel von Folie 5 und den gegebenen Werten.

Formel: $$
        f_0 = \frac{1}{2\pi\sqrt{LC}}
        $$

Eingesetzt: $$
            f = \frac{1}{2\pi\sqrt{10\cdot10^{-3}\cdot100\cdot10^{-9}}}
            \approx 5.03\,\text{kHz}
            $$

### Schritt 2
Bauen Sie die Schaltung auf. Finden Sie im Simulator die Frequenz, bei der der Strom I maximal ist.

![Gif für Aufgabe 1](https://raw.githubusercontent.com/SpongebobSquarepants35/SV2/main/HDGifs/Task1SV2HD.gif)

### Schritt 3
Notieren Sie die Frequenz, die Sie im Simulator gemessen haben.

Die Frequenz, bei der der Strom I maximal ist, ist um 5kHz


### Schritt 4
Vergleichen Sie Ihren Rechenwert (aus 1.), Ihren Messwert (aus 3.) und den Wert auf Folie 7. Was stellen Sie fest?

Man kann deutlich erkennen, dass Rechenwert und der Messwert fast gleich sind. Zum Wert aus Folie 7 kann man sagen, das andere Bauteile verwendet wurden und somit natürlich andere Werte entstehen

---
# Aufgabe 2 – Güte und Dämpfung visualisieren

### Aufgabenstellung
Untersuchen Sie den Einfluss des Widerstands R (Dämpfung) auf die Schärfe der Resonanzkurve (Güte Q), wie auf Folie 9 dargestellt.

### Schritt 1
Finden Sie eine Methode in der Simulationssoftware, um den Frequenzgang des Stroms sichtbar zu machen.

### Schritt 2
Stellen Sie den Widerstand R so ein, dass Sie ihn interaktiv verändern können

### Schritt 3
Dokumentieren Sie durch ein GIF, wie sich die Form der Resonanzkurve (die "Peak-Form") ändert, wenn Sie R von einem sehr kleinen Wert (z.B. 5 Ω) zu einem großen Wert (z.B. 300 Ω) ändern.

![Gif für Aufgabe 2](https://raw.githubusercontent.com/SpongebobSquarepants35/SV2/main/HDGifs/Task2SV2HD.gif)

### Schritt 4
Erklären Sie den Zusammenhang, den Sie beobachten:
1. Was passiert mit der Höhe des Peaks?
2. Was passiert mit der Breite des Peaks?
3. Was bedeutet das für die Güte Q und die Bandbreite der Schaltung (vgl. Folie 9)?

---

1. Mit zunehmendem Widerstand wird der Resonanz-Peak niedriger. Der maximale Strom bzw. die maximale Amplitude nimmt also ab, da der Widerstand mehr Energie im Schwingkreis dämpft.
2. Mit zunehmendem Widerstand wird der Resonanz-Peak breiter. Die Resonanz ist weniger stark ausgeprägt und verteilt sich über einen größeren Frequenzbereich.
3. Ein kleiner Widerstand führt zu einer hohen Güte Q und einer schmalen Bandbreite, da die Schaltung nur in einem engen Frequenzbereich stark schwingt.
Mit steigendem Widerstand sinkt die Güte Q, während die Bandbreite zunimmt, weil die Dämpfung größer wird und die Resonanz weniger scharf ist.
---
# Aufgabe 3 - Bandpass vs. Bandsperre

### Aufgabenstellung
Verstehen Sie den fundamentalen Unterschied zwischen einem Bandpassfilter und einem Bandsperrfilter (siehe Folie 12). Beide nutzen dieselben L/C-Werte, haben aber gegensätzliche Funktionen.

### Schritt 1
Bauen Sie beide Schaltungen im Simulator auf.

### Schritt 2
Berechnen Sie zuerst die erwartete Resonanzfrequenz f₀ (Thomsonsche Formel).

Formel: $$
        f_0 = \frac{1}{2\pi\sqrt{LC}}
        $$

Eingesetzt: $$
            f = \frac{1}{2\pi\sqrt{1\cdot10^{-3}\cdot10\cdot10^{-9}}}
            \approx 50.3\,\text{kHz}
            $$

### Schritt 3
Simulieren Sie den Frequenzgang der Ausgangsspannung für beide Schaltungen

### Schritt 4
Dokumentieren Sie Ihre Ergebnisse durch GIFs, die den Frequenzgang beider Schaltungen zeigen.

![Gif für Aufgabe 3](https://raw.githubusercontent.com/SpongebobSquarepants35/SV2/main/HDGifs/Task3SV2LongHD.gif)
### Schritt 5
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

### Aufgabenstellung
Verstehen Sie das Grundprinzip eines Digital-Analog-Wandlers (DAC). Wie auf Folie 30 und Folie 31 konzeptionell gezeigt, ist dies der umgekehrte Prozess zur Abtastung.

### Schritt 1
Bauen Sie das R-2R-Netzwerk im Simulator auf.

### Schritt 2
Stellen Sie nacheinander alle 8 Binärkombinationen (von 000 bis 111) mit den drei Schaltern ein.

### Schritt 3
Messen Sie für jede Kombination die resultierende analoge Ausgangsspannung Uaus (Tipp: der "DC Level" im Scope) und füllen Sie die folgende Tabelle aus.

| Bit 2 (MSB) | Bit 1 | Bit 0 (LSB) | Dezimalwert | Uaus (V) |
|-------------|-------|-------------|-------------|----------|
| 0           | 0     | 0           | 0           | 0.0 V    |
| 0           | 0     | 1           | 1           | 3.3 V    |
| 0           | 1     | 0           | 2           | 4.0 V    |
| 0           | 1     | 1           | 3           | 4.8 V    |
| 1           | 0     | 0           | 4           | 5.0 V    |
| 1           | 0     | 1           | 5           | 6.0 V    |
| 1           | 1     | 0           | 6           | 6.3 V    |
| 1           | 1     | 1           | 7           | 6.6 V    |

### Schritt 4
Dokumentieren Sie durch ein GIF, wie sich die Ausgangsspannung ändert, wenn Sie die Binärkombinationen durchschalten.

![Gif für Task 4](https://raw.githubusercontent.com/SpongebobSquarepants35/SV2/main/HDGifs/Task4SV2HD.gif)

### Auswertung

1. Analysieren Sie Ihre Messwerte. Was stellen Sie fest?
2. Berechnen Sie die Spannungsdifferenz (die "Schrittgröße") zwischen den einzelnen Dezimalwerten (z.B. die Differenz zwischen Wert 1 und Wert 2). Ist diese Schrittgröße konstant?
3. Erklären Sie, warum die Schaltung das tut, was auf Folie 30 (Quantisierung/Treppenstufen) gezeigt wird.

---

1. Beim Betrachten der Messwerte fällt auf, dass der Spannungsanstieg nicht gleichmäßig verläuft. Die Spannung steigt also nicht linear mit den einzelnen Schritten.
2. Berechnung der Schrittgrößen:

    0 zu 1 = 3.3 V            
    1 zu 2 = 0.7 V           
    2 zu 3 = 0.8 V             
    3 zu 4 = 0.2 V             
    4 zu 5 = 1.0 V             
    5 zu 6 = 0.3 V              
    6 zu 7 = 0.3 V            

Fazit: Einige Übergänge verändern die Spannung stärker als andere.
3. Die Schaltung verwendet Widerstände und drei Schalter (3 Bits), um bestimmte Spannungen zu erzeugen. Dadurch entstehen stufenartige Werte („Treppenstufen“), wie auf Folie 30 gezeigt, die z. B. für Pulsamplitudenmodulation genutzt werden können.

---

# Aufgabe 5 - Filterung von Obertönen (Rechteck-zu-Sinus-Wandler)

### Aufgabenstellung
Kombinieren Sie die Fourier-Analyse (ab Folie 22) und die Filterwirkung von Schwingkreisen (Folie 12). Verstehen Sie, wie ein Bandpass-Filter Obertöne einer Rechteckwelle herausfiltert und nur die Grundfrequenz durchlässt.

### Schritt 1
Berechnung: Berechnen Sie die theoretische Resonanzfrequenz f₀ für den LC-Bandpass (L = 1 mH, C = 10 nF). Notieren Sie Ihren Rechenweg und das Ergebnis.

Formel: $$
        f_0 = \frac{1}{2\pi\sqrt{LC}}
        $$

Eingesetzt: $$
            f = \frac{1}{2\pi\sqrt{1\cdot10^{-3}\cdot10\cdot10^{-9}}}
            \approx 50.3\,\text{kHz}
            $$

### Schritt 3
Aufbau: Bauen Sie den Bandpass-Filter vom Typ auf Folie 12 (oberes Bild) im Simulator nach. Verwenden Sie Ri = 2,2 kΩ und die gegebenen L/C-Werte.

### Schritt 4
Simulation:
Speisen Sie die Schaltung mit einer Rechteckspannung (Square Wave).
Stellen Sie die Grundfrequenz f₁ der Rechteckwelle genau auf die in Schritt 1 berechnete Resonanzfrequenz f₀ ein.

## Schritt 5
Messung & Dokumentation:
Öffnen Sie das Oszilloskop ("Scope") und zeigen Sie das Eingangssignal (an der Quelle) und das Ausgangssignal (über dem L/C-Parallelkreis) gleichzeitig an.
Dokumentieren Sie durch ein GIF, das beide Wellenformen zeigt.

![Gif für Aufgabe 5](https://raw.githubusercontent.com/SpongebobSquarepants35/SV2/main/HDGifs/Task5SV2HD.gif)

### Auswertung

### Erklärung

1. Beschreiben Sie den Unterschied zwischen der Eingangs- und der Ausgangswellenform.
2. Erklären Sie mit Verweis auf die Fourier-Analyse (Folie 25), warum das Ausgangssignal diese Form hat. Welche Frequenzkomponenten der Rechteckwelle lässt der Filter passieren und welche blockiert er?

---

1. Am Eingang liegt eine Rechteckwelle an, am Ausgang eine nahezu sinusförmige Wellenform.
2.  Eine Rechteckwelle besteht aus der Grundfrequenz f₀ und ungeraden Harmonischen (3f₀, 5f₀, …).  
Der LC-Bandpass ist auf f₀ abgestimmt und lässt hauptsächlich diese Frequenz passieren, während höhere Harmonische stark gedämpft werden.  
Dadurch bleibt am Ausgang im Wesentlichen nur die Grundschwingung erhalten, was zu einem nahezu sinusförmigen Signal führt.

---

# Aufgabe 6

### Schritt 1
Stellen Sie die Quelle auf "Sine" (Sinus), 5V Amplitude.

1. Stellen Sie die Quelle auf "Sine" (Sinus), 5V Amplitude.
2. Führen Sie eine AC-Analyse ("Frequency"-Plot) am Ausgang (V) durch.
3. Finden Sie die Frequenz, bei der die Schaltung ihre stärkste Resonanz (größte Verstärkung) zeigt.

---

2. Bei sinusförmiger Anregung zeigt die Schaltung eine deutliche Resonanzüberhöhung bei einer bestimmten Frequenz.
3. Die maximale Verstärkung tritt bei etwa 3,56MHz auf

### Schritt 2

1. Ändern Sie die Quelle zu einer "Square Wave" (Rechteck), 5V Amplitude.
2. Stellen Sie die Grundfrequenz der Rechteckwelle auf 1,18 MHz ein. (Dies ist 1/3 der Resonanzfrequenz aus Schritt 1).
3. Betrachten Sie den Eingang und den Ausgang (V) im Zeitbereich (Scope).
4. Betrachten Sie den Eingang und den Ausgang (V) im Frequenzbereich (FFT / "Frequency").

---

### Scrhitt 3
1. Ändern Sie die Grundfrequenz der Rechteckwelle auf 712 kHz. (Dies ist 1/5 der Resonanzfrequenz).
2. Beobachten Sie erneut das Spektrum am Ausgang.

### Auswertung
1. **Zeitbereich**: Vergleichen Sie das Eingangs- und Ausgangssignal. Welche Form hat das Ausgangssignal? Welche Frequenz hat es (grob gemessen)?

2. **Frequenzbereich (Eingang)**: Beschreiben Sie das Spektrum der Rechteckwelle, das Sie sehen. Welche Harmonischen sind vorhanden (1., 3., 5. ...)?
3. Frequenzbereich (Ausgang): Beschreiben Sie das Spektrum am Ausgang. Was ist mit der Grundschwingung (1,18 MHz) passiert? Was ist mit der 3. Harmonischen (3,56 MHz) passiert?
4. Erklärung: Fassen Sie zusammen, was der Filter mit dem Rechtecksignal gemacht hat und warum das Ausgangssignal so aussieht, wie es aussieht.

---

1. **Zeitbereich**

Eingangssignal:
- Rechteckwelle  
- Amplitude: 5 V  
- Grundfrequenz: 1,18 MHz

Ausgangssignal:
- Kein Rechtecksignal mehr, nahezu sinusförmig
- Frequenz: ca. 3,56 MHz
- Amplitude deutlich kleiner als Eingang

Erklärung: 
- Das Filter unterdrückt die Grundfrequenz der Rechteckwelle  
- Verstärkt eine höhere Frequenzkomponente nahe der Resonanzfrequenz

2. **Frequenzbereich (Eingang)**
Im Frequenzspektrum des Eingangssignals sind folgende Frequenzanteile sichtbar:
Grundschwingung bei **f₁ = 1,18 MHz** 
Ungerade Harmonische:  
**3. Harmonische:** 3,56 MHz  
**5. Harmonische:** ca. 5,9 MHz  
weitere ungerade Harmonische mit abnehmender Amplitude Gerade Harmonische sind nicht vorhanden. Das Spektrum entspricht der Fourier-Zerlegung einer idealen Rechteckwelle.

 3. **Frequenzbereich  (Ausgang)** 
 Im Ausgangsspektrum zeigt sich folgendes Verhalten:
  Die Grundschwingung bei 1,18 MHz ist stark gedämpft * Die **3. Harmonische** bei 3,56 MHz ist dominant * Höhere Harmonische (5., 7., …) sind stark abgeschwächt. Das Ausgangsspektrum wird fast komplett von der Resonanzfrequenz des Filters bestimmt.

   4. **Erklärung / Zusammenfassung** 
Der Filter lässt nur die Harmonische bei 3,56 MHz passieren → Ausgang fast sinusförmig.


### Ende