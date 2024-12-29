# projet-salaires

---
# Analyse et Prédiction des Offres d’Emploi en France**
## Présentation du projet
Ce projet vise à explorer les offres d’emploi en France en utilisant des données collectées sur France Travail et What the jungle (WTJ). 
Les objectifs sont de :
1. Analyser les tendances du marché du travail (localisation, domaines, salaire, qualifications, etc.).
2. Comprendre l’impact des études et de l’expérience sur le salaire.
3. Prédire le salaire à partir des caractéristiques des offres grâce à des modèles économétriques et de machine learning.

---
## Structure du projet
Le projet est organisé en trois dossiers principaux :

### 1."Recuperation_data"
Ce dossier contient :
- "France_Travail/" et "Wtj/" : Scripts de scraping pour collecter et compléter les catégories à l'aide des dees données ainsi que des descriptions en utilisant regex. Cette partie étant longue, nous avons garder juste les fichiers csv finaux : "offres_emploi_concatene_cleaned.csv" et "dataset_wtj_cleaned.csv"

### 2."Statistique"
- "Carte_interactive.ipynb" : Notebook pour créer une carte interactive des offres d’emploi en fonction de leur localisation.
- "stats.ipynb" : Notebook contenant des analyses statistiques descriptives (salaires par domaine, région, corrélations, etc.).

### 3."Prediction"
- "Econometrie/econometrie.ipynb" : Modèle économétrique pour prédire les salaires.
- "XGboost/xgboost.ipynb" : Modèle basé sur XGBoost pour prédire les salaires.

---

## Exécution du projet

### 1. Prérequis
Assurez-vous d’avoir :
- Python
- Les packages listés dans `requirements.txt`.

### **2. Reproduire les analyses et prédictions**
L’ensemble des analyses est orchestré par le fichier `main.ipynb`. Ce notebook exécute :
1. **`stats.ipynb`** (analyses statistiques descriptives).
2. **`econometrie.ipynb`** (modèle économétrique).
3. **`xgboost.ipynb`** (modèle machine learning).

Pour lancer le projet :
- Clonez ce dépôt GitHub.
- Ouvrez et exécutez le fichier `main.ipynb`.

---

## **Données**
### **Sources**
- **France Travail** et **What The Jungle**.
- Les variables collectées incluent :  
  - Salaire brut annuel.
  - Domaine d’activité.
  - Localisation géographique.
  - Niveau d’études requis.
  - Années d’expérience demandées.
  - Type de contrat.

### **Stockage des données**
Les données combinées sont stockées dans `Recuperation_data/combined_dataset.csv`. Les étapes de préparation des données sont détaillées dans le notebook `combine_FT_Wtj.ipynb`.

---

## **Résultats et Insights**
### **Analyses descriptives**
- Comparaison des salaires par domaine et localisation.
- Corrélation entre études, expérience et salaire.
- Carte interactive des opportunités d’emploi.

### **Prédictions**
- Modèle économétrique pour interpréter les facteurs influençant le salaire.
- Modèle XGBoost pour prédire les salaires avec précision.

---

## **Contributeurs**
- **[Nom 1]**  
- **[Nom 2]**  
- **[Nom 3]**

---

Si vous souhaitez des ajustements ou un format différent pour le `README.md`, faites-le-moi savoir ! 😊