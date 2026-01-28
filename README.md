🏡 EstimaTours : IA de Prédiction Immobilière
Estimer un bien à Tours n'est plus une question d'intuition, mais de Data Science.

Ce projet utilise l'apprentissage automatique (Machine Learning) pour prédire le prix des appartements à Tours (37), en se basant sur les données réelles des Demandes de Valeurs Foncières (DVF).

🎯 L'Objectif
L'enjeu n'est pas seulement de calculer un prix moyen, mais de capturer la réalité géographique de Tours. Le modèle combine la puissance de calcul des arbres de décision avec une analyse spatiale pour comprendre pourquoi un appartement rue Colbert n'a pas le même prix qu'au Sanitas.

🛠️ Le "Moteur" sous le capot
Le projet utilise une architecture hybride pour maximiser la précision :

Clustering K-Means : Découpage automatique de Tours en 20 micro-quartiers basés uniquement sur la latitude et la longitude.

Target Encoding : Calcul du "standing" de chaque quartier (prix moyen au m²) pour informer le modèle.

Random Forest Regressor : L'algorithme final qui croise la surface, le nombre de pièces, la date et la position géographique pour estimer le prix final.

📊 Fonctionnalités clés
Analyse Géographique : Intégration de la distance au centre-ville (Place Plumereau).

Nettoyage de données : Filtrage automatique des valeurs aberrantes (châteaux, caves à 1€, ou erreurs de saisie).

📈 Résultats du modèleErreur Moyenne (MAE) : Environ 21 000 € sur le prix total des biens.Score $R^2$ : Précision constante sur le marché tourangeau entre 2021 et 2025.

👤 Auteur Eddy De Castro étudiant en Informatique spécialisé en IA et Data (Prépa --> Mines Alès et en même temps une L3 de maths)

Projet réalisé dans le cadre de l'apprentissage des algorithmes de régression, clustering et de SK Learn.
