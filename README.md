# SAM2 Bildsegmentierung

Dieses Projekt implementiert eine automatische Bildsegmentierung unter Verwendung des SAM2 (Segment Anything Model 2) von Facebook. Es bietet Funktionen zur automatischen Erkennung von markanten Punkten und zur Segmentierung mit verschiedenen Prompting-Methoden.

## Features

- Automatische Erkennung von markanten Punkten im Bild
- Unterstützung verschiedener Segmentierungsmethoden:
  - Positive Punkt-Segmentierung
  - Negative Punkt-Segmentierung
  - Box-basierte Segmentierung
- Visualisierung der kombinierten Segmentierungsergebnisse
- Speicherung der Ergebnisse als PNG-Dateien

## Voraussetzungen

```python
torch
numpy
opencv-python (cv2)
matplotlib
sam2
```

## Installation

1. Klonen Sie das Repository:
```bash
git clone [repository-url]
```

2. Installieren Sie die benötigten Pakete:
```bash
pip install torch numpy opencv-python matplotlib
pip install sam2  # SAM2 Modell
```

## Verwendung

1. Das Skript wird wie folgt ausgeführt:
```python
python segmentation.py
```

2. Der Code:
- Lädt ein vortrainiertes SAM2-Modell
- Findet automatisch markante Punkte im Bild
- Führt verschiedene Segmentierungen durch
- Speichert die Ergebnisse im "output_segmentations" Ordner

## Funktionen

### find_prominent_points()
- Findet automatisch positive und negative Punkte im Bild
- Verwendet Konturerkennung und Schwerpunktberechnung
- Parameter: `object_area_threshold` (Standard: 0.01)

### visualize_combined_segmentation()
- Visualisiert die Segmentierungsergebnisse
- Zeigt positive Punkte (grün), negative Punkte (rot) und Boxen (blau)
- Überlagert die Segmentierungsmasken mit dem Originalbild

## Ausgabe

- Die Ergebnisse werden im Ordner "output_segmentations" gespeichert
- Jedes Ergebnis enthält:
  - Originalbild
  - Markierte Punkte und Boxen
  - Überlagerte Segmentierungsmasken
