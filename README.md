# UnitTesting_Logging für das K-Nearest Neighbors (K-NN) Klassifikationsprojekt
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/beckceline/UnitTesting_Logging/HEAD)

Diese README-Datei enthält eine ausführliche Dokumentation für das K-Nearest Neighbors (K-NN) Klassifikationsprojekt. Dieses Projekt verwendet den MNIST-Datensatz, um Handgeschriebene Ziffern zu klassifizieren. Der Code ist in Python geschrieben und verwendet Bibliotheken wie NumPy, pandas, Matplotlib und scikit-learn. Ziel ist es, die Genauigkeit eines K-NN-Modells zu bestimmen und einige Tests zur Validierung durchzuführen.

Inhaltsverzeichnis

Voraussetzungen
Projektübersicht
Datenbeschaffung
Datenbereinigung und Vorbereitung
Klassifikation mit K-NN
Tests
Loggen und Zeitmessung

Voraussetzungen<a name="voraussetzungen"></a>
Bevor wir dieses Projekt ausführen, sollten wir sicherstellen, dass wir die folgenden Bibliotheken installiert haben:

NumPy
pandas
Matplotlib
scikit-learn
unittest (Teil der Python-Standardbibliothek)
Wenn wir diese Bibliotheken nicht installiert haben, können wir sie über pip install <bibliotheksname> installieren.

Projektübersicht<a name="projektübersicht"></a>
Dieses Projekt zielt darauf ab, die Genauigkeit eines K-Nearest Neighbors (K-NN) Klassifikators auf dem MNIST-Datensatz zu bestimmen. Der Code ist in Python geschrieben und besteht aus den folgenden Schritten:

Importieren der benötigten Bibliotheken.
Laden des MNIST-Datensatzes.
Aufteilung der Daten in Trainings- und Testsets.
Datenexploration und Anzeigen von Beispielen.
Datenbereinigung und Vorbereitung durch Skalierung.
Training und Auswertung des K-NN-Modells.
Durchführung von Tests zur Validierung des Modells.
Implementierung von Logging und Zeitmessung für Laufzeitanalysen.

Datenbeschaffung<a name="datenbeschaffung"></a>
Der MNIST-Datensatz wird mithilfe von scikit-learn fetch_openml Funktion geladen. Es wird eine Teilmenge des Datensatzes ausgewählt (z. B. 10.000 Beispiele) und in Trainings- und Testsets aufgeteilt.

Datenbereinigung und Vorbereitung<a name="datenbereinigung-und-vorbereitung"></a>
Die Daten werden mithilfe von StandardScaler skaliert, um sicherzustellen, dass alle Merkmale denselben Maßstab haben. Dies ist wichtig für viele Machine Learning-Algorithmen, einschließlich K-NN.

Klassifikation mit K-NN<a name="klassifikation-mit-k-nn"></a>
Ein K-NN Klassifikator wird erstellt und mit den Trainingsdaten trainiert. Die Anzahl der Nachbarn (k) kann angepasst werden. Anschließend werden Vorhersagen auf den Testdaten gemacht, und die Genauigkeit des Modells wird berechnet und angezeigt.

Tests<a name="tests"></a>
Für die Validierung des K-NN-Modells werden einige Tests durchgeführt. Einige dieser Tests umfassen:

Die Vorhersagegenauigkeit des Modells wird überprüft und sollte über 90% liegen.
Eine Konfusionsmatrix wird erstellt und angezeigt.
Die Laufzeit des Modells wird gemessen und mit einer repräsentativen Laufzeit verglichen.

Loggen und Zeitmessung<a name="loggen-und-zeitmessung"></a>
Das Projekt implementiert eine einfache Methode zum Loggen von Informationen und zur Messung der Laufzeit von Funktionen. Dies kann nützlich sein, um die Performance des Modells und seiner Komponenten zu überwachen.

Die Ergebnisanzeigen im Projekt liefern wichtige Informationen über den Fortschritt, die Leistung und die Validierung des K-Nearest Neighbors (K-NN) Klassifikationsmodells. Hier sind die erwarteten Bildschirmausgaben im Detail:

Trainings- und Testdaten:
Die Ausgabe zeigt die Anzahl der Trainingsdaten und Testdaten nach der Aufteilung. Diese Informationen geben an, wie viele Beispiele für das Training des Modells und für die Evaluierung zur Verfügung stehen. In diesem Beispiel:

"Trainingsdaten: (8000, 784)" bedeutet, dass es 8.000 Trainingsbeispiele gibt, und jedes Beispiel hat 784 Merkmale (in diesem Fall Pixel für die Bilderkennung).
"Testdaten: (2000, 784)" bedeutet, dass es 2.000 Testbeispiele gibt, die ebenfalls 784 Merkmale haben.

Genauigkeit des K-NN-Modells:
Diese Ausgabe zeigt die Genauigkeit des K-NN-Modells für die gewählte Anzahl von Nachbarn (k) an. Die Genauigkeit ist ein Maß dafür, wie gut das Modell in der Lage ist, die Ziffern korrekt zu klassifizieren. In diesem Beispiel:

"Genauigkeit des k-NN-Modells mit k=5" bedeutet, dass das Modell mit einer k-Wert-Einstellung von 5 trainiert wurde.
"0.91" ist die Genauigkeit des Modells, was bedeutet, dass es 91% der Testdaten korrekt klassifiziert hat.

Testergebnisse und Confusion Matrix:
Diese Ausgabe zeigt die Ergebnisse der Tests, die zur Validierung des K-NN-Modells durchgeführt wurden. Es enthält die Genauigkeit und die Verwirrungsmatrix. In diesem Beispiel:

Confusion Matrix:
[[12  0  0  0  0  0  0  0  0  0]
 [ 0  9  0  0  0  0  0  0  0  0]
 [ 0  0  9  0  0  0  0  0  0  0]
 [ 0  0  0 11  0  0  0  0  0  0]
 [ 0  0  0  0  9  0  0  0  0  0]
 [ 0  0  0  0  0  7  0  0  2  0]
 [ 0  0  0  0  0  0  9  0  0  0]
 [ 0  1  0  0  1  0  0  6  0  0]
 [ 0  0  0  2  1  0  0  0 11  0]
 [ 0  1  0  0  0  0  0  0  0  9]]
 
"Accuracy: 0.92" zeigt die Genauigkeit des Modells, die bei 92% liegt.
Die Confusion Matrix zeigt, wie viele Beispiele korrekt in jeder Klasse klassifiziert wurden. Zum Beispiel zeigt die Diagonale (von oben links nach unten rechts), wie viele Beispiele in der entsprechenden Klasse korrekt klassifiziert wurden.

Loggen und Zeitmessung:
Diese Ausgabe liefert Informationen zur Laufzeit bestimmter Funktionen im Projekt. In diesem Beispiel:

Laufzeit: 0.01789689064025879 Sekunden
Vergleich mit repräsentativer Laufzeit: 0.01
Laufzeit liegt im akzeptablen Bereich.

"Laufzeit" zeigt die Zeit in Sekunden an, die für eine bestimmte Funktion benötigt wurde.
"Vergleich mit repräsentativer Laufzeit" vergleicht die tatsächliche Laufzeit mit einer repräsentativen Laufzeit. In diesem Fall liegt die tatsächliche Laufzeit im akzeptablen Bereich.
Diese Ausgaben sind entscheidend, um den Projektfortschritt zu überwachen, die Modellleistung zu beurteilen und eventuelle Probleme oder Verbesserungsbereiche zu identifizieren.

Mit einer Genauigkeit von 92% haben wir in diesem Projekt den K-Nearest Neighbors (K-NN) Klassifikator angewendet, um handgeschriebene Ziffern im MNIST-Datensatz erfolgreich zu klassifizieren. Diese Leistung ist bereits bemerkenswert und zeigt die Effektivität des K-NN-Algorithmus.

Dennoch sind wir uns bewusst, dass Raum für Verbesserungen besteht. Durch zusätzliche Trainingseinheiten und eine mögliche Erweiterung der Trainingsdatenmenge auf etwa 20.000 Beispiele könnten wir eine Genauigkeit von 99% oder mehr erreichen. Es ist wichtig anzumerken, dass dies jedoch erheblich mehr Zeit in Anspruch nehmen würde, und wir haben es aus Zeitgründen nicht durchgeführt.
