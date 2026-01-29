🏡 EstimaTours : IA de Prédiction Immobilière
Estimer un bien à Tours n'est plus une question d'intuition, mais de Data-Science.

Ce projet utilise l'apprentissage automatique (Machine Learning) pour prédire le prix des appartements à Tours (37), en se basant sur les données réelles des Demandes de Valeurs Foncières (DVF).

Genèse du projet: Première apprentissage de Scikit-Learn.

🎯 L'Objectif
L'enjeu n'est pas seulement de calculer un prix moyen, mais de capturer la réalité géographique de Tours. Le modèle combine la puissance de calcul des arbres de décision avec une analyse spatiale pour comprendre pourquoi un appartement rue Colbert n'a pas le même prix qu'au Sanitas.

🛠️ Le "Moteur" sous le capot
Le projet utilise une architecture hybride pour maximiser la précision :

Clustering K-Means : Découpage automatique de Tours en 20 micro-quartiers basés uniquement sur la latitude et la longitude.

Target Encoding : Calcul du "standing" de chaque quartier (prix moyen au m²) pour informer le modèle.

Random Forest Regressor : L'algorithme final qui croise la surface, le nombre de pièces, la date et la position géographique pour estimer le prix final.

Comparaison avec un modèle de régression linéaire (R²=0.20 et erreur moyenne au m²=500€/m²)
Comparaison avec un modèle de K-NN (R²=0,28 et erreur moyenne au m² =455€/m²

Random Forest Regressor : L'algorithme final qui croise la surface, le nombre de pièces, la date et la position géographique pour estimer le prix final. (R²=0,40 et erreur moyenne au m² =400 €/m²)

Je précise que les R² sont volontairement faible. J'aurais pu chercher avoir le R² gonflé artificiellement si on avait prix y=valeur foncière (la surface gonfle le R² car elle fait baissé l'erreur).
Le R² est faible car l'algorithme ne peut pas deviner l'état de l'appartement pour déterminer sa valeur (au m²).
Sur une maison

📉 Simulation sur un appartement moyen. Prenons les statistiques classiques pour un appartement à Tours :Surface : 50m² (T2/T3 typique).Prix moyen au m² : Environ 3000€/m².Prix total du bien : 150 000€.
Ce qui donne une erreur moyenne de 20 000€ soit 13% d'écart avec la réalité (C'est pas si mal)

📊 Fonctionnalités clés
Analyse Géographique : Intégration de la distance au centre-ville (Place Plumereau).

Nettoyage de données : Filtrage automatique des valeurs aberrantes (châteaux, caves à 1€, ou erreurs de saisie).

📈 Résultats du modèle Erreur Moyenne (MAE) : Environ 21 000 € sur le prix total des biens. #en moyenne avec Random Forest

Voici quelques graphiques intéressant:
<img width="1090" height="700" alt="image" src="https://github.com/user-attachments/assets/74fcf107-4c39-47ff-b234-45c7f104308c" />
<img width="982" height="854" alt="image" src="https://github.com/user-attachments/assets/fbeaf3bd-69da-4991-ae26-f9a1d3ce3a59" />
<img width="850" height="546" alt="image" src="https://github.com/user-attachments/assets/53b0e286-9f5f-43b0-8bb4-d79c590c85e2" />
<img width="992" height="547" alt="image" src="https://github.com/user-attachments/assets/28ca0b34-ac45-4ab7-8fd2-77b125610344" />
l'emplacement compte pour beaucoup (il apparait sous plusieurs formes)
<img width="602" height="454" alt="image" src="https://github.com/user-attachments/assets/33c7990a-ba72-4169-9be4-433732848e9e" />


👤 Auteur Eddy De Castro étudiant en Informatique spécialisé en IA et Data (Prépa --> Mines Alès et en même temps une L3 de maths)

Projet réalisé dans le cadre de l'apprentissage des modèles de régression, clustering, Random Forest, K-NN et K Means.
