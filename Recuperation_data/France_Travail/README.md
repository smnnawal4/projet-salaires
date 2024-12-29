
---

# Projet Salaires - Extraction des Données

## Introduction
Ce fichier décrit les étapes et l'utilité de chaque notebook utilisé dans la phase d'extraction et de préparation des données pour le projet Salaires. Cette étape est essentielle pour obtenir des données propres et exploitables pour les analyses et les modèles prédictifs.

---

## Structure et Fonctionnement

### 1. `scrapping.ipynb`
Ce notebook est responsable de la récupération des données brutes à partir de l'API de **France Travail**. Il utilise des requêtes API pour collecter des informations sur les offres d'emploi.

- **Fonctionnalités principales** :
  - Envoie des requêtes à l'API de France Travail.
  - Sauvegarde les résultats dans des fichiers au format JSON.

- **Output** :
  - Fichiers JSON contenant les données brutes des offres d'emploi.

---

### 2. `concatenate.ipynb`
Ce notebook traite les fichiers JSON générés par `scrapping.ipynb` pour :
1. Sélectionner uniquement les catégories pertinentes.
2. Combiner les différentes catégories en un fichier unique.

- Fonctionnalités principales :
  - Lecture des fichiers JSON bruts.
  - Filtrage des données pour ne conserver que les colonnes importantes (exemple : "salaire", "expérience", "études").
  - Création d'un fichier CSV consolidé avec toutes les données.

- Output :
  - Un fichier CSV combiné contenant les informations nécessaires pour les étapes suivantes.

---

### 3. `fill_data.ipynb`
Ce notebook améliore la qualité des données dans le fichier CSV combiné. Il remplit les informations manquantes et corrige les erreurs dans les catégories importantes.

- Fonctionnalités principales :
  - Lecture des descriptions des offres pour compléter les champs vides (exemple : "salaire", "études", "type de contrat").
  - Utilisation de règles prédéfinies ou de techniques de traitement du langage naturel (NLP) pour analyser les descriptions.
  - Correction des fautes manuelles ou des incohérences laissées par les employeurs (exemple : fautes de frappe, doublons).
  
- Output :
  - Un fichier CSV propre et enrichi, prêt pour l'analyse statistique et les modèles prédictifs.

---

## Flux de Données

Voici un aperçu du processus global de l'extraction des données :

1. Scraping :
   - Données brutes récupérées à partir de l'API de France Travail (`scrapping.ipynb`).

2. Nettoyage et regroupement :
   - Les catégories importantes sont sélectionnées, et un fichier consolidé est généré (`concatenate.ipynb`).

3. Enrichissement :
   - Les informations manquantes sont complétées et les erreurs corrigées (`fill_data.ipynb`).

---

## Fichiers générés

1. JSON brut : 
   Généré par `scrapping.ipynb`, contient les données brutes collectées.

2. CSV consolidé :  
   Généré par `concatenate.ipynb`, il regroupe toutes les catégories pertinentes.

3.CSV enrichi :  
   Généré par `fill_data.ipynb`, il contient les données nettoyées, corrigées et complètes.

---

## Conclusion
Ces étapes d'extraction et de préparation des données permettent de garantir que les données utilisées dans les analyses et les modèles soient de haute qualité, complètes et prêtes à être exploitées. Le processus couvre la collecte brute, le nettoyage, et l'enrichissement des données.

---