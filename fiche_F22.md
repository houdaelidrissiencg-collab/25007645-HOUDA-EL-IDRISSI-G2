# Fiche attribuée : F22, Anticipations d'inflation des marchés

## Sujet
Régression sur séries mensuelles (algorithmes 1, 2 et 3). Série quotidienne T10YIE agrégée au mois.

## Problématique
Le niveau des anticipations d'inflation à 10 ans du mois précédent et son historique récent permettent-ils de mieux prévoir le T10YIE du mois suivant qu'une simple persistance ?

## Objectif mesurable (fixé avant les résultats)
- Cible : T10YIE moyen du mois t+1.
- Variables : retards (t, t−1, t−2), variation 1 mois, moyenne mobile 3 mois, volatilité, calculées avec le passé uniquement.
- Découpage chronologique : environ 70 % entraînement, 15 % validation, 15 % test.
- Référence naïve : persistance. Métrique principale : RMSE test. Secondaire : MAE.
- Critère de réussite : RMSE inférieur à celui de la persistance. Sinon, conclusion honnête : série quasi marche aléatoire.

## Sources
- Federal Reserve Bank of St. Louis, FRED, série T10YIE (10-Year Breakeven Inflation Rate) : https://fred.stlouisfed.org/series/T10YIE
- Données utilisées : 6 222 observations quotidiennes du 02/01/2003 au 06/11/2026 (255 valeurs manquantes).

## Références (outils)
- pandas : https://pandas.pydata.org
- scikit-learn : https://scikit-learn.org
- matplotlib : https://matplotlib.org
- seaborn : https://seaborn.pydata.org
