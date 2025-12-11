# 🧹 Data Cleaning Documentation

## 1\. Überblick

Die ursprünglichen Rohdaten stammen aus einem unstrukturierten E-Commerce-Datenbankexport und lagen vollständig in **einer einzigen Tabelle** vor. Die Datei enthielt zahlreiche leere, redundante oder technisch erzeugte Spalten und war für analytische Zwecke nicht unmittelbar nutzbar.

Für den Analyseprozess wurden die Daten umfassend bereinigt, neu strukturiert und in logisch getrennte Einheiten überführt.

* * *

## 2\. Schritte der Datenbereinigung

### 2.1 Entfernen irrelevanter und kaum befüllter Spalten

Alle vollständig leeren oder analytisch irrelevanten Spalten wurden gelöscht.  
Nach diesem Schritt verblieben 60 Variablen.

Numerische Statuscodes (z. B. Zahlungs-, Bestell- oder Produktstatus) wurden durch verständliche, textbasierte Kategorien ersetzt

Nach der detaillierten Analyse der einzelnen DataFrames blieben insgesamt **55 relevante und analytisch nutzbare Spalten** erhalten.

### 2.2 Trennung des Gesamtdatensatzes in vier Entitäten

Die ursprüngliche Tabelle wurde anhand der Präfixe in den Spaltennamen in vier fachliche DataFrames zerlegt:

- `df_customers` – Kundendaten
    
- `df_orders` – Bestellungen
    
- `df_items` – Bestellpositionen
    
- `df_products` – Produktinformationen
    

Zusätzlich wurde ein aggregierter Gesamtdatensatz (`aggregate_df`) für übergreifende Analysen erstellt.

### 2.3 Bereinigung von Duplikaten

Duplikate wurden gezielt über fachlich sinnvolle Kombinationen aus Primär- und Zeitstempelfeldern entfernt, z. B.:

- Kunden: `Customers.id` + `Customers.create_date`
    
- Bestellungen: `Orders.id` + `Orders.placed_date`
    
- Produkte: `Products.id` + `Products.last_modified`
    

### 2.4 Behandlung fehlender Werte

Fehlende Werte wurden entweder:

- durch geeignete Schätzwerte ersetzt (z. B. Preisrelationen), oder
    
- bewusst beibehalten, sofern sie analytisch aussagekräftig sind.
    

Die Entscheidung erfolgte abhängig von der Relevanz der jeweiligen Variable.

### 2.5 Konsistenzprüfungen & Datentypen

- Datumsangaben → `datetime`
    
- Kategorische Variablen → `category`
    
- Numerische Werte → `float` bzw. `int`
    

Ungültige IDs (z. B. Produkte ohne Produkt-ID) wurden entfernt.

### 2.6 Feature Engineering

Für die Bestellpositionen wurde die Kennzahl **`cost_price_ratio`** ergänzt, um die Marge pro Artikel analysieren zu können.

* * *

## 3\. Ergebnis der Bereinigung

Nach Abschluss des Data Cleaning liegen folgende strukturierte Datensätze vor:

- **Aggregierter Datensatz**: 55 Spalten, 4194 Zeilen
    
- **3054 eindeutige Kunden**
    
- **3565 Bestellungen**
    
- **4194 Bestellpositionen**
    
- **1710 einzigartige Produkte**
    

Alle DataFrames sind nun klar strukturiert, konsistent und für die weitere **explorative Datenanalyse (EDA)** bereit.
