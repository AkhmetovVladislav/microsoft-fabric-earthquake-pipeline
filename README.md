# Microsoft Fabric – Earthquake Data Pipeline (Bronze–Silver–Gold Architektur)

Dieses Projekt zeigt eine vollständige **End-to-End-Datenpipeline** in **Microsoft Fabric**, die globale Erdbebendaten aus dem **USGS-API** erfasst, verarbeitet und für die Analyse in **Power BI** aufbereitet.  
Die Lösung basiert auf der **Medallion-Architektur (Bronze → Silver → Gold)** und demonstriert einen modernen, skalierbaren Workflow für Data Engineering und Reporting.

---

## Architektur & Workflow

Die Pipeline integriert mehrere Microsoft-Fabric-Komponenten zu einem durchgängigen Prozess:

1. **Data Ingestion (Bronze Layer)**  
   Rohdaten werden automatisch über das USGS-API abgerufen und als Delta- oder Parquet-Dateien im Lakehouse gespeichert.

2. **Transformation (Silver Layer)**  
   Die Daten werden bereinigt, typisiert und mit zusätzlichen Attributen angereichert, um ein konsistentes, qualitätsgesichertes Dataset zu erzeugen.

3. **Aggregation (Gold Layer)**  
   Business-fertige Tabellen werden erstellt – z. B. Aggregationen nach Land, Datum und Magnitüde – als Grundlage für analytische Dashboards.

4. **Orchestrierung (Data Factory)**  
   Alle Schritte sind in einer **Microsoft Fabric Data Factory-Pipeline** automatisiert.  
   Die Notebooks werden sequentiell ausgeführt (Bronze → Silver → Gold) mit Erfolgs-Triggern und täglicher Zeitplanung.

5. **Visualisierung (Power BI)**  
   Die Gold-Daten werden über **Direct Lake** an Power BI angebunden.  
   Das interaktive Dashboard **„Worldwide Earthquake Events“** zeigt:
   - Anzahl und Stärke der Erdbeben weltweit  
   - Kartenvisualisierung mit regionalen Filtern  
   - Zeitliche Analyse über Datums-Slicer  
   - KPI-Karten für Gesamtereignisse und maximale Signifikanz  

---

## Nutzen & Ergebnisse

- Vollständig automatisierte Pipeline von der Rohdatenaufnahme bis zur Analyse  
- Echtzeit-Einblicke in globale Erdbebenaktivitäten  
- Transparente Datenqualität und einheitliches Datenmodell  
- Skalierbare Architektur für zukünftige Erweiterungen  

---

## Technologien

**Microsoft Fabric (Data Engineering, Data Factory, Power BI)** | **Python / PySpark** | **USGS API** | **Lakehouse / OneLake**

---

## Lizenz

Dieses Projekt steht unter der **MIT-Lizenz**.  
Siehe [`LICENSE`](./LICENSE) für weitere Informationen.

---

## Autor

**Vladislav Akhmetov**  
Data Engineer • Microsoft Azure & Fabric • Python  
📧 [LinkedIn](https://www.linkedin.com/in/vladislav-akhmetov/) | 🌐 [GitHub](https://github.com/AkhmetovVladislav)
