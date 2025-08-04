Prévision avec les séries temporelles — Partie 1 : Préparation et Visualisation

Objectif:

Préparer et visualiser les données quotidiennes de ventes pour un produit spécifique dans un magasin donné, à partir d’un dataset d’inventaire de magasin de détail.

Étapes réalisées
Chargement des données
Lecture du fichier CSV contenant les données d’inventaire et de ventes.

Conversion du format de date
Transformation de la colonne Date en type datetime, pour faciliter les opérations sur les séries temporelles.

Filtrage des données
Sélection des observations pour un produit (Product ID = P0001) et un magasin (Store ID = S001) spécifiques.

Agrégation des ventes
Regroupement des unités vendues (Units Sold) par date.

Visualisation
Tracé de la série temporelle des ventes quotidiennes afin d’identifier tendances et variations.

Utilisation du code
Pour analyser un autre produit ou magasin, modifier les valeurs de Product ID et Store ID dans le code.


Bibliothèques utilisées
pandas : manipulation des données

matplotlib : visualisation graphique

Fichier de données
retail_store_inventory.csv : données d’inventaire et ventes journalières des produits par magasin.


Le graphique ci-dessous représente les ventes quotidiennes du produit P0001 dans le magasin S001.

<img width="1044" height="459" alt="image" src="https://github.com/user-attachments/assets/79fc80da-3fb9-4f39-b7b7-104d8848a86a" />


Prévision des ventes avec les séries temporelles — Partie 2 :

Modélisation avec Prophet

Objectif

Prévoir les ventes futures quotidiennes d’un produit spécifique dans un magasin donné, à partir des données historiques, en utilisant le modèle Prophet.

Étapes réalisées
Préparation des données
Adaptation des colonnes pour correspondre aux exigences du modèle Prophet.

Création et entraînement du modèle
Instanciation du modèle Prophet et apprentissage sur les données historiques.

Prédiction des ventes futures
Génération des dates futures et prédiction des ventes pour ces dates.

Visualisation des résultats
Affichage des prévisions avec les données historiques et visualisation des différentes composantes (tendance, saisonnalité, etc.).

Utilisation
Installer la bibliothèque Prophet.

Adapter la période de prévision selon les besoins.

Visualiser les prévisions et les composantes pour interpréter le modèle.

Bibliothèques utilisées
pandas

prophet

matplotlib

1. Graphique principal des prévisions

Affiche les données historiques (observées) et la courbe des prévisions futures.

Montre aussi l’intervalle d’incertitude (bandes de confiance).

<img width="999" height="401" alt="image" src="https://github.com/user-attachments/assets/7cade96b-72f4-4ac6-9913-3281a128f77c" />

2. Graphique des composantes

Montre la décomposition de la série en tendances, saisonnalités (jour de la semaine, année, etc.) et éventuellement effets des jours fériés si ajoutés.

Permet de comprendre ce que le modèle retient dans la série.

<img width="1007" height="448" alt="image" src="https://github.com/user-attachments/assets/6a20f002-300f-4cd4-9881-9d02ec7cdb07" />

