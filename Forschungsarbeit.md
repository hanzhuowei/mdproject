# Forschungsarbeit - 1,7
>Validierung und Optimierung der Schwellenparameter im ultraschall-basierte Detektionssysteme
## Übersicht Feedback
* Schnell in dem Projekt einarbeiten, Code lesen, KernIdee nachvollziehen
* Aufgabe gute geleistet, Messung durchführen
* eigenständige Messdaten auswerten und Matlab implementieren
* Ergebnis in der wöchentliche Sitzung präsentieren
* Aufgetretene Problem diskutieren. 

##Gesammelte Erfahrung 
* Signalverarbeitung in Matlab, Abtastung, Filter, I-Q Signal-Mischung. 
* Algorithm/ Funktion Entwicklung, CA-CFAR, Puls-Laufzeit Entfernungmessung
* GUI-Funktionsentwicklung, VBA-Entwicklung
* Hinblick im FAS gewinnen.
## Ziel
Im Fahrerassistenz-Systems wird die Objektdetektion im Nahfeld (0-3m) üblichweise mittels Ultraschalls durchgeführt.

Eine Detektionsschwelle von realer Wert wird zunächst anhand voraus gewählten Algorithm definiert. Wenn die Amplitude des empfangenen Echos diese überschreitet, danach gestalt sich die Entfernungmessung nach dem Puls/Laufzeitprinzip sehr einfach. 

Aber wegen der sich stets geändert Fahrenumgebung kommt Falschalarm manchmal vor, da im bisherigen System die Schwelle Konstant bleibt. In der zukünftigen Generation soll eine adaptive Schwelle, die sich im Lauf der Zeit mit dem Bodenechos anpassen kann, bestimmt werden.  

Verwendet Algorithm für Ada.Schwelle ist **Constant False Alarm Rate** , für die Optimierung dieses Algorithmus sind zwei Parameter betroffen Fensterlänge L und Mutiplikationsfaktor $\alpha$

## Inhalt
_Messung Durchführung, Parameter Auswertung und Algorithm Optimierung, AutomatisierungsTool_

### *Messung Durchführung*
* Sendemuster Definieren: 
Der Ultraschallsensor betriebt sich mit dem zentralen Frequenz 50 kHz im F-Band von 40-60 kHZ.  Das vom Sensor ausgesendete Signal enthält ein fallend/steigende Freq.Band, die Signaldauer, Mittelfrequenz, Bandbreite sind Einflussfaktoren des Falschalarmrate.  Für jede unterschiedliche Fahrbahnoberfläche soll diese Faktoren definiert werden, um den  Zusammenhang zwischen Schwellenparameter und Signaleigenschaft bei jedem Oberfläche herauszufinden.

* Messung in der Einbauhalle:

1.Handbuch für Messung durchlesen, Hinweis notizen und Fragen stellen, wie z.B, 
	
* Wie wird alle Messgeräte und Laptop mit einanderen mit dem Kabel verbindet werden
*  achten darauf, die Polen zu dem Sensor nicht vertauschen

  2.Messgeräte einbauen, Probemessung durchführen, Troubleshooting. 
3.Da die Bodenecho vom Glattgrund in der Einbauhalle sehr gering sind,  kann der Ergebnis als Referenz betrachtet werden. 

* Messung auf Gras, Schotter, Pflaster, Aspalt

### Parameter Auswertung und Algorithm Optimierung
* Kriterium: FP-Rate konstant = 0,3 einbehalten, d.h. Die Anzahl von falschen Alarm soll weniger als 30 wenn 100 mal Test durchführt.  
* Grid-Search des Parameter $\alpha$
* Prozess für jede Sendemuster und Boden. 
* $\alpha$ soll für Nah- und Fernfeld unterschiedliche eingesetzt werden.
* Abhängigkeit der Parameter von Impuls & Oberfläche in Grafik darstellen

### AutomatisierungsTool
pro Sendemuste (21) jedem Boden (5), grid-search $\alpha$ 7 - 10 Werte,  Ergebnis in Grafik automatisch darstellen