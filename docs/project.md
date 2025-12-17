## Projekt: Kundensegmentierung und Umsatzanalyse im E-Commerce

Dieses Projekt analysiert Kunden-, Bestell- und Produktdaten eines E-Commerce-Unternehmens
mit Fokus auf Kundensegmentierung (B2B/B2C, RFM), Umsatzmuster und prädiktive Modelle
zur Margen- und Nachbestellprognose.

## Überblick

Dieses Projekt analysiert das Kunden-, Bestell- und Produktverhalten eines E-Commerce-Unternehmens auf Basis eines bereinigten, relational strukturierten Datensatzes.  
Der Schwerpunkt liegt auf Kundensegmentierung, Umsatz- und Bestellanalysen sowie prädiktiver Modellierung zur Bewertung von Margen und Wiederbestellungen.

Die Analyse umfasst:

- Segmentierung von Kunden (B2C vs. B2B, RFM)
    
- Untersuchung von Umsatz-, Bestell- und Zahlungsstrukturen
    
- Analyse von Produktperformance und Margen
    
- Entwicklung logistischer Regressionsmodelle zur Prognose von Margen und Reorders
    

Ziel ist es, datengetriebene Einblicke in Kundenverhalten und Geschäftsmechanismen zu gewinnen und analytische Methoden strukturiert anzuwenden.

## Projektstruktur

```
ecommerce-customer-segmentation/
├── .git/                                 # Git Repository
├── .venv/                                # Virtuelle Python-Umgebung
├── .vscode/                              # VS Code Konfiguration
│   ├── extensions.json                   # Empfohlene VS Code Extensions
│   └── settings.json                     # Workspace-spezifische Einstellungen
├── data/                                 # Datenverzeichnis (nicht versioniert)
│   ├── clean/                            # cleandaten
│   ├── raw/                              # Rohdaten
│   └── processed/                        # Verarbeitete Daten
├── docs/                                 # Dokumentation
│   └── data_cleaning.md                  # Dokumentation der Datenbereinigung
│   └── project.md                        # Projektbeschreibung und Workflow
│   └── structure.md                      # Analytische Projektstruktur
├── notebooks/                            # Jupyter Notebooks
│   └── 01_Data_Overview.ipynb            # 
│   └── 02_Data_Cleaning.ipynb            # 
│   └── 03_Data_Analysis.ipynb            # 
├── src/                                  # Python Source Code
│   └── core/
│       ├── __init__.py                   # Macht core zu einem Package
│       └── data.py                       # Datenlade-Funktionen
├── .gitignore                            # Git Ignore Regeln
├── .python-version                       # Python Version für uv
├── pyproject.toml                        # Projekt-Konfiguration
├── README.md                             # Projekt-Beschreibung
└── uv.lock                               # Abhängigkeiten Lock-File
```

## Analysestruktur

1. Customer Analytics  
2. Order & Revenue Analytics  
3. Payment & Shipping Operations  
4. Product & Profitability Analytics  
5. Predictive Analytics  
6. Key Findings & Conclusions


## Workflow

1.  **Datenaufbereitung**
    
    - Bereinigung, Typkonvertierung und Deduplikation
        
    - Aufteilung des aggregierten Datensatzes in logisch getrennte DataFrames (Customers, Orders, Items, Products)
        
2.  **Explorative Datenanalyse (EDA)**
    
    - Grundlegende Verteilungen, Ausreißeranalyse
        
    - Erste Visualisierungen zu Kunden-, Bestell- und Umsatzdaten
        
3.  **Analytische Vertiefung**
    
    - Kundensegmentierung (B2B/B2C, RFM)
        
    - Zeitreihen- und Umsatzanalysen
        
    - Zahlungs- und Versandanalysen
        
    - Produkt- und Margenanalyse
        
4.  **Prädiktive Modellierung**
    
    - Logistische Regression zur Vorhersage hochmargiger Produkte
        
    - Modelle zur Prognose von Wiederbestellungen
        
    - Modellvergleich und Interpretation der Ergebnisse

    - Die prädiktive Modellierung ist im letzten Analyse-Notebook integriert.
        
5.  **Dokumentation & Strukturierung**
    
    - Klare Trennung von Analyse (Notebooks), Code (`src/`) und Dokumentation
        
    - Zusammenfassung zentraler Erkenntnisse in README und Projektbeschreibung



## Methoden & Werkzeuge

- Explorative Datenanalyse (EDA)
- RFM-Analyse und Kundensegmentierung
- Zeitreihenanalyse (Moving Averages, saisonale Muster)
- Logistische Regression
- Python (pandas, matplotlib, seaborn, scikit-learn)
```
