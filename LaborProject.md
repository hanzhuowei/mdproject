# Labor Projekt - 2,3
> Statistical Signal Processing - Automotive Radar

##Keywords
-Fachspezifische:   *LFMCW-Radar DSV System, OS-CFAR Peak Detection, R-V Abschätzung, Objektverfolgung*

##Gesammelte Erfahrung 
(mit Beispiel erklären)

- **Statistische** Radar-Signalverarbeitung für Echtzeit-Anwendung (was ist Statistische?)
- Systementwicklung
- Algorithmentwicklung für echte Anwendung, dabei Literatur lesen, geeignete Technik ausprobieren und wählen, Leistung verbessern.
- Matlab Implementierung, Code Management mit Git
- Gruppenarbeit 

## Ziel
Aufbau des gesamten System, von empfangene zeitliche Rauschsignal bis zu die **Position**(Entfernung, Winkel) und **Geschwindigkeit** des Objekt, und Objekt verfolgen


###Motivation
-Adaptive cruise control 
-FAS
-Technik Umwandelung zu Audio-DSV, MRI

###LFMCW-Radar
-Tx und Rx
-Untermischung ins Basisband, Abtastung mit FFT
-LFMCW - eigenschaft, Frequency shift = Doppler + Distance

###Peak Detection
- CA-CFAR 
- OS-CFAR
- Center of Gravity for Peak Interpolation  

###Frequency Matching und R-V Abschätzung
- 4 Rampe, zwei gesuchte R, V
- 2 Rampe für Berechnen, 2 für Prognose
- R-V Diagramm, Cross-Section
- Clustering, Ghost object

###Winkel Abschätzung & Order 
- Grundlage: Antennenarray, jede hat unterschiedliche Laufzeit / Entfernung zum Objekt
- DML
- Multi Objekt?

###Tracking
- Kalman Filter
- Messung oder Prognose? 


