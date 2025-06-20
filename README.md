# 🧠 Reporting de Personnalité : Introvertis vs Extravertis (Power BI + Microsoft Fabric)

Ce projet explore et visualise les traits de personnalité à partir d’un jeu de données, à travers un rapport interactif Power BI, enrichi par un traitement dans Microsoft Fabric Notebook (Spark).

## 🔍 Objectif

Analyser des comportements comme le temps passé seul, la fréquence de publication, ou la participation sociale, et les relier aux prédictions de personnalité (introverti ou extraverti).

## 🧱 Contenu du repo

📁 data/ : jeu de données brut (.csv ou exporté depuis Fabric) récupéré à partir de Kaggle  
📁 notebooks/ : notebook Microsoft Fabric utilisé pour nettoyer/analyser les données  
📁 powerbi/ : fichier Power BI (.pbix) contenant les visuels et KPIs  
📁 measures/ : mesures DAX utilisées dans le rapport  
📄 README.md : ce fichier  

## ⚙️ Technologies

- Microsoft Fabric (Notebook Spark + Lakehouse)
- Power BI (Desktop & Service)
- DAX
- GitHub

## 📊 Exemple de visualisations

- Carte KPI : % d’extravertis vs introvertis
- Histogrammes : temps d’isolement moyen par type
- Graphe à bulles : relation entre sociabilité, isolement, cercle d’amis
- Filtres dynamiques : explorer par fréquence de publication, sociabilité, etc.

## 📌 Mesures DAX principales

- `% d’introvertis`, `% d’extravertis`
- `Score sociabilité moyen`
- `Score isolement moyen`
- `Profil_post_frequency_mesure`
- `Profil_personality_mesure`
