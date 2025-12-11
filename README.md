# 🚀 Customer Segmentation: Datengetriebene Einblicke 

<!-- Eine kurze, prägnante Beschreibung deines Data Science Projekts in 1-2 Sätzen.-->
In diesem Projekt untersuche ich ein E-Commerce-Datenset mit Informationen über Kunden, Bestellungen und Produkte. 


## 📊 Projektübersicht

**Problemstellung:** 
<!-- Beschreibe das Problem, das du lösen möchtest -->

Für das Ziel müssen die Daten zunächst gründlich bereinigt werden, da sie sehr roh und unstrukturiert sind. Anschließend können wir durch eine explorative Analyse erste Muster, Zusammenhänge und wichtige Kennzahlen erkennen, die helfen, das Kunden- und Kaufverhalten besser zu verstehen.

### **Ziel:** 

<!-- Was ist das Hauptziel deines Projekts? -->
Ziel ist es, das Kaufverhalten besser zu verstehen, wichtige Kundengruppen zu erkennen und erste Muster in den Daten sichtbar zu machen. 

**Das Kundenverhalten verstehen und zentrale Segmente identifizieren**

- Ermitteln, welche Kundengruppen den höchsten Umsatz generieren.
- Kaufmuster analysieren: Häufigkeit, durchschnittlicher Bestellwert, Produkttypen, Vertriebskanäle.
- Welche Produkte sind am profitabelsten?
- Wie beeinflussen Rabatte die Conversion Rate und den durchschnittlichen Warenkorbwert?


**Methoden:** 
<!-- Welche Techniken/Algorithmen verwendest du? -->

✍️ später


##  Datenquelle

Die Rohdaten stammen aus dem Kaggle-Datensatz Customer Segmentation:  
https://www.kaggle.com/datasets/yunusemretokdemir/customer-segmentation/data

Es handelt sich um unstrukturierte Rohdaten aus einer E-Commerce-Datenbank, vollständig in einer einzigen Tabelle abgelegt und nicht für Analysen vorbereitet. Die Datei enthält viele leere oder unvollständige Spalten.

Nach Entfernen vollständig leerer Spalten wurden **60 Spalten** für die weitere Verarbeitung geladen.  
Die Daten kombinieren Kunden-, Bestell-, Bestellpositions- und Produktinformationen, jedoch ohne klare Trennung der Entitäten.

### Warum diese Daten?

Um auch meine Fähigkeiten im Umgang mit „Daten-Bolzen“ — also unaufgeräumten, realitätsnahen Rohdaten — zu demonstrieren und diese in eine analysierbare Form zu bringen.



##  Data Cleaning 

Die geladenen Rohdaten waren unstrukturiert und enthielten zahlreiche fehlende, redundante oder technisch erzeugte Spalten. Daher wurden folgende Schritte durchgeführt:

- Entfernen von irrelevanten Spalten sowie von Spalten, in denen kaum oder praktisch keine verwertbaren Daten vorhanden waren
- Umwandlung und Vereinheitlichung der Datentypen  
    (Datumsfelder → datetime, Kategorien → category).
- Trennung des ursprünglichen Datensatzes in vier logische Entitäten:  
    **Customers**, **Orders**, **Order_Items** und **Products**.
- Behandlung fehlender Werte (gezielte Imputation oder bewusstes Belassen – abhängig von ihrer analytischen Relevanz)
- Bereinigung von Duplikaten anhand sinnvoller Schlüsselattribute  
    (z. B. Kunden-ID + Erstellungsdatum, Bestell-ID + Bestelldatum).
- Entfernen von Datensätzen ohne Produkt-ID sowie Überprüfung auf logische Konsistenz.
- Feature Engineering: Hinzufügen der Kennzahl cost_price_ratio zur Bewertung der Marge je Bestellposition.
- **Nach der Bereinigung liegen nun vier getrennte, klar strukturierte und analysierbare DataFrames vor sowie ein zusammengeführter Gesamtdatensatz (55 Spalten, 4194 Zeilen). Diese bilden die Grundlage für die weitere explorative Datenanalyse.**
    
    Der bereinigte Datenbestand umfasst:
    
    - **3054 eindeutige Kunden**
        
    - **3565 Bestellungen**
        
    - **4194 Bestellpositionen (Order Items)**
        
    - **1710 einzigartige Produkte**


## 📊 Explorative Datenanalyse (EDA)

✍️ später


## 📈 Insights & Ergebnisse

✍️ später

* * *

## Setup

Klone das Repository
```bash
# Repository klonen
git clone [DEIN-REPO-LINK]
cd [REPO-NAME]
```

Installiere [uv](https://uv.dev) (falls noch nicht installiert) und synchronisiere die Abhängigkeiten
```bash
# Dependencies installieren
uv sync
```

### Ausführung 

Notebooks in dieser Reihenfolge ausführen:

1. notebooks/01_exploration.ipynb - raw owerview
2. notebooks/02_preprocessing.ipynb - clean
3. notebooks/03_modeling.ipynb - deep EDA
4. notebooks/04_results.ipynb 
<!--



-->


