# prevision-avec-les-series-temporelle
Projet Série Temporelle – Partie 1 : Préparation et Visualisation
Objectif
Préparer et visualiser les données de ventes quotidiennes d’un produit spécifique dans un magasin donné, en utilisant un dataset d’inventaire de magasin de détail.

Étapes réalisées
Chargement des données
Lecture du fichier CSV contenant les données d’inventaire et ventes.

Conversion du format de date
Transformation de la colonne Date en objet datetime pour faciliter les opérations temporelles.

Filtrage des données
Sélection des données correspondant à un seul produit (Product ID = P0001) et un seul magasin (Store ID = S001).

Agrégation des ventes
Regroupement des unités vendues (Units Sold) par date.

Visualisation
Tracé de la série temporelle des ventes quotidiennes, permettant d’observer les tendances et variations dans le temps.

Utilisation du code
Modifier les valeurs de Product ID et Store ID dans le code pour analyser un autre produit ou magasin.

Le graphique affiche les ventes totales par jour pour le produit/magasin sélectionné.

Bibliothèques utilisées
pandas pour la manipulation des données.

matplotlib pour la visualisation.

Fichier de données
retail_store_inventory.csv : données d’inventaire et ventes journalières des produits par magasin.
le graphe ci-dessous represente les ventes quotidienne

<img width="1044" height="459" alt="image" src="https://github.com/user-attachments/assets/79fc80da-3fb9-4f39-b7b7-104d8848a86a" />


Prochaine étape
Prévision des ventes futures à partir des séries temporelles préparées (Partie 2).

Objectif
Prévoir les ventes futures quotidiennes d’un produit spécifique dans un magasin donné, à partir des données historiques, en utilisant le modèle Prophet.

Étapes réalisées
Préparation des données

Renommage des colonnes Date en ds et Units Sold en y pour respecter la structure attendue par Prophet.

Création et entraînement du modèle Prophet

Instanciation du modèle par défaut, puis entraînement (fit) sur les données historiques.

Prédiction des ventes futures

Génération d’un DataFrame avec les dates futures (ici 30 jours).

Prédiction des valeurs pour ces dates.

Visualisation des résultats

Affichage du graphique des ventes historiques et prévues.

Affichage des composantes du modèle : tendance, saisonnalités, etc.

Utilisation
Installer Prophet avec pip install prophet.

Modifier la période de prévision (variable periods dans make_future_dataframe) si besoin.

Visualiser la prévision avec model.plot() et les composantes avec model.plot_components().

Bibliothèques utilisées
pandas pour la manipulation des données.

prophet pour la modélisation et la prévision.

matplotlib pour la visualisation.

1. Graphique principal des prévisions

Affiche les données historiques (observées) et la courbe des prévisions futures.

Montre aussi l’intervalle d’incertitude (bandes de confiance).

<img width="999" height="401" alt="image" src="https://github.com/user-attachments/assets/7cade96b-72f4-4ac6-9913-3281a128f77c" />

2. Graphique des composantes

Montre la décomposition de la série en tendances, saisonnalités (jour de la semaine, année, etc.) et éventuellement effets des jours fériés si ajoutés.

Permet de comprendre ce que le modèle retient dans la série.

<img width="1007" height="448" alt="image" src="https://github.com/user-attachments/assets/6a20f002-300f-4cd4-9881-9d02ec7cdb07" />

