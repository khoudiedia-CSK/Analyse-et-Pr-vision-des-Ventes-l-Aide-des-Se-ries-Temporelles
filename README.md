# 📈 Prévision des ventes quotidiennes d’un magasin avec Prophet

## 🧾 Contexte du projet

MauriShop, une enseigne de distribution commerciale située en Mauritanie, souhaite améliorer la gestion de ses stocks et optimiser ses approvisionnements.
Pour cela, elle cherche à mettre en place un système de prévision des ventes quotidiennes de ses produits, en s’appuyant sur les données historiques enregistrées dans ses magasins.

Elle dispose d’un historique détaillé des ventes par jour, par magasin et par produit.  
L’équipe data est chargée de concevoir un modèle de prévision fiable, afin d’anticiper les quantités vendues chaque jour pour un produit spécifique dans un magasin donné.

Ce projet s’inscrit dans une démarche plus large de pilotage de la chaîne logistique par la donnée, avec pour objectifs :
- D’éviter les ruptures de stock
- De limiter le surstockage inutile
- D’améliorer la planification des commandes

---

## 🎯 Objectif

Prévoir les ventes journalières d’un produit à l’aide du modèle **Prophet**, à partir des données historiques issues d’un fichier d’inventaire (`retail_store_inventory.csv`).

---

## 🛠️ Technologies utilisées

- `pandas` – manipulation de données
- `matplotlib` – visualisation graphique
- `prophet` – prévision de séries temporelles

  ---

## 📂 Structure du projet

retail-forecast/
├── retail_forecast.ipynb # Notebook Jupyter avec tout le pipeline

├── data/

│ └── retail_store_inventory.csv # Données brutes

├── outputs/

│ ├── forecast_chart.png # Graphique de la prédiction

│ └── forecast_components.png # Graphique des composantes Prophet

└── README.md # Description du projet

## 🔎 Partie 1 – Analyse exploratoire

- Chargement et nettoyage du fichier CSV
- Conversion de la colonne `Date` au format `datetime`
- Filtrage pour un produit (`Product ID = P0001`) et un magasin (`Store ID = S001`)
- Agrégation des ventes (`Units Sold`) par jour
- Visualisation de la série temporelle des ventes quotidiennes

📌 Exemple de graphique :

![Time Series](https://github.com/user-attachments/assets/79fc80da-3fb9-4f39-b7b7-104d8848a86a)

---

## 🤖 Partie 2 – Modélisation avec Prophet

- Préparation des données au format attendu par Prophet (`ds`, `y`)
- Création et entraînement du modèle Prophet
- Génération de 30 jours de prévision future
- Visualisation de la courbe des prévisions et des composantes

📈 Résultats visuels :

**1. Prédictions avec intervalle de confiance :**

![Forecast](https://github.com/user-attachments/assets/7cade96b-72f4-4ac6-9913-3281a128f77c)

**2. Composantes du modèle :**

- Tendance
- Saison hebdomadaire
- (Effets calendaires possibles)

![Components](https://github.com/user-attachments/assets/6a20f002-300f-4cd4-9881-9d02ec7cdb07)

---

## 💡 Pour adapter le projet

Tu peux facilement réutiliser le code pour :
- Un autre **produit** → changer `Product ID`
- Un autre **magasin** → changer `Store ID`
- Une autre **période de prévision** → modifier la durée dans `make_future_dataframe()`

---

## 🧠 Ce que j’ai appris

- Préparation et agrégation de données temporelles
- Visualisation efficace d’une série chronologique
- Utilisation du modèle Prophet pour la prévision
- Interprétation des tendances et saisonnalités

