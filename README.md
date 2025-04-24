# 🛰️ Projekt-Prompt: Satellitenbild der Siegessäule über Copernicus CDSE

Dieses README ist zugleich auch ein CHatGPT-Prompt um eine erste. einfache Satelliten-Abfrage durchzuführen und via dem CDSE-SDK direkt von den Satelliten-Datenspaces des Projekts abzuholen und zu rendern: 

Schreibe ein Python-Programm, das mithilfe des offiziellen SDKs des Copernicus Data Space Ecosystem (CDSE) ein aktuelles Sentinel-2-Satellitenbild über der Berliner Siegessäule (Tiergarten) abruft und speichert.

## 🔧 Anforderungen:

###    Geografischer Ausschnitt:

        Zentrum: Siegessäule, Koordinaten
        📍 Breitengrad: 52.514543, Längengrad: 13.350119

        Fläche: Quadrat, dessen Diagonalen sich im Referenzpunkt schneiden

        Seiten verlaufen in Ost-West und Nord-Süd Richtung

        Die Seitenlänge des Quadrats ist jeweils 16 km, also sind die Diagonalen jeweils Sqrt(2) * 16 km ≈ 22.627 km

###    Zielbild:

        Darstellung in True Color (RGB): Bänder B04, B03, B02

        Bildauflösung: 2000 × 2000 Pixel (jedes Pixel ist 8x8 m² groß, sollte nochmal mit der Satellitenauflösung vergleichen werden)

        Exportformat: PNG-Datei

        Dateiname: siegessaeule_satellite.png

###    CDSE-Datenabfrage:

        Nutze das aktuellste verfügbare Sentinel-2 L2A-Produkt

        Region of Interest (ROI): berechnet aus obigem Quadrat

        Zugriff über das CDSE SDK, das von GitHub installiert wird:

        pip install git+https://github.com/SERCO-CDSE/CDSE_Catalog.git

        Bildrendering über integrierte Methoden des SDK

## 🛠️ Weitere Hinweise:

    Stelle sicher, dass Pillow installiert ist für die Bildspeicherung:

    pip install Pillow

    Optional: Registrierung bei dataspace.copernicus.eu zur Nutzung der API

### Prompt

Generiere aus diesem Prompt auch ein Markdown-Dokument, ein Jupyter-Notebook und vor allem eine Python-Datei.
