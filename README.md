# 🧠 Reporting de Personnalité : Introvertis vs Extravertis (Power BI + Microsoft Fabric)

Ce projet explore et visualise les traits de personnalité à partir d’un jeu de données, à travers un rapport interactif Power BI, enrichi par un traitement dans Microsoft Fabric Notebook (Spark).

## 🔍 Objectif

Analyser des comportements comme le temps passé seul, la fréquence de publication, ou la participation sociale, et les relier aux prédictions de personnalité (introverti ou extraverti).

## 🧱 Contenu du repo

📁 data/ : jeu de données brut (.csv ou exporté depuis Fabric) récupéré à partir de Kaggle  
📁 notebooks/ : notebook Microsoft Fabric utilisé pour nettoyer/analyser les données  
📁 powerbi/ : fichier Power BI (.pbix) contenant les visuels et KPIs  
📄 README.md : ce fichier  


## 🏗️ Prérequis

Pour reproduire ce projet dans votre environnement Microsoft Fabric, vous devez :

1. **Créer un Lakehouse dans Microsoft Fabric**
   - Ce Lakehouse stockera les données sources sous forme de fichiers Delta (ou CSV).
   - Le fichier `personality_dataset.csv` peut être importé dans la partie Files.

2. **Créer un Notebook Spark**
   - Utilisez le notebook fourni dans pour récupérer les données du lakehouse `/notebooks/analysis_introvert_extravert.ipynb`
   - Vous pouvez y préparer les données, enrichir les colonnes, ou lancer un traitement statistique.
   - Utiliser le module d'AutoML (FlaML) intégré à Fabric pour créer un modèle de ML.
   - Stocker les résultats dans un lakehouse `personality_dataset_predictions.csv`.

3. **Connecter Power BI au Lakehouse**
   - Utilisez DirectLake ou Import pour analyser les données depuis le Lakehouse.
   - Le rapport Power BI utilise des **mesures DAX** dynamiques et plusieurs **slicers visuels**.



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
