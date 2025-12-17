## **TEIL 1: CUSTOMER ANALYTICS**

Verständnis unserer Kunden und ihres Verhaltens

**1.1 Kundensegmentierung**  

Kundendaten (Diagramme) – B2B- vs. B2C-Verteilung
- Anzahl der Kunden
- Gesamtumsatz
- Bestellhäufigkeit


**1.2 RFM-Analyse**  

RFM-Berechnung, Tabelle  

RFM-Heatmap: Durchschnittlicher Umsatz

**1.3 Customer Lifetime Value**  

CLV-Berechnung + zentrale Erkenntnisse:
- „Die Top-20 % der Kunden generieren 61,78 % des Umsatzes“
- „Im ‚At-Risk‘-Segment stehen 56.894 $ CLV auf dem Spiel“  
    CLV-Visualisierung (3 Streudiagramme)
    

* * *

## **TEIL 2: ORDER & REVENUE ANALYTICS**

Vertiefte Analyse von Bestellmustern und Finanzkennzahlen

**2.1 Bestellverteilung**  

Bestellvisualisierungen – Histogramm nach Bestellwert und Boxplot mit Ausreißern  

Hochwertige Bestellungen (über 1.500 $)

**2.2 Analyse des Bestellstatus**  

Kreuztabelle: Bestellstatus × Zahlungsstatus  

Orders.status × Feature-Indikatoren  

Heatmap: Feature-Heatmap nach Bestellstatus

**2.3 Zeitliche Trends**  

Umsatztrend mit gleitenden Durchschnitten  

Saisonale Trends  

Monatlicher Umsatz (Gesamtumsatz pro Monat)

* * *

## **TEIL 3: PAYMENT & SHIPPING OPERATIONS**

Operative Effizienz und Zahlungsverhalten

**3.1 Zahlungsanalyse**  

Zahlungsart × Zahlungsstatus

Payment Analysis (4 Diagramme in einer Abbildung):
- Verteilung der Zahlungsstatus
- Heatmap (Zahlungsstatus nach Zahlungsmethode)
- Verteilung der Zahlungsmethoden (horizontal, sortiert)
- Durchschnittlicher Bestellwert nach Zahlungsmethode
    

**3.2 Versand & Logistik**  

Kreuztabelle: Orders.shipping_carrier × shipping_paid + Diagramm  

shipping_paid × Orders.shipping_method  

Streudiagramm: Bestellwert vs. Versandkosten

* * *

## **TEIL 4: PRODUCT & PROFITABILITY ANALYTICS**

Produktperformance und Margenanalyse

**4.1 Produktverteilung**  

Histogramm: 
- Anzahl der Produkte pro Bestellung  
- Häufigkeit von Wiederbestellungen

**4.2 Preis- & Margenanalyse**  

Histogramm: Preis vs. Kosten  

Streudiagramm: Produktmarge vs. Kosten  

Boxplot: Verteilung der Produktmargen

**4.3 Top-Performer**  

Top-10-Produkte mit der höchsten Marge (Tabelle + Diagramm)

**4.4 Lieferantenanalyse**  

Heatmap: Produktstatus vs. Lieferant (%)

* * *

## **TEIL 5: PREDICTIVE ANALYTICS & MODELING**

Statistische Modelle und Prognosen

**5.1 Margenprognosemodelle**  

Logistische Regression: Hochmargige Produkte nach Lieferant (Pseudo-R² = 0,75)  

Streudiagramm: Wahrscheinlichkeit für hochmargige Produkte

**5.2 Nachbestellprognosemodelle**  

Verbessertes Modell: made_reorder ~ Recency_days + Monetary_total (Pseudo-R² = 0,154)  

Vollständiges Modell: + is_business  

Visualisierung: Logistische Regressionskurve (Einfluss der Rezenz)
