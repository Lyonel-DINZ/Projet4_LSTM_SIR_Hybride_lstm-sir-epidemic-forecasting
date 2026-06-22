# Projet4_LSTM_SIR_Hybride_lstm-sir-epidemic-forecasting
Modèle hybride LSTM + SIR pour la prédiction des épidémies à partir de séries temporelles et de variables exogènes.

# 📊 Modèle Hybride LSTM + SIR pour la Prédiction des Épidémies

Ce projet implémente un **modèle hybride combinant deep learning et modélisation épidémiologique** afin de prédire l’évolution des cas d’une épidémie.

## 🎯 Objectif

Prédire les cas incidents sur un horizon de **14 jours** à partir :
- des séries temporelles des cas passés (21 jours)
- de variables exogènes (température, mobilité, mesures sanitaires)

## ⚙️ Méthodologie

Le modèle hybride fonctionne en deux étapes :

### 1. LSTM (Réseau de neurones récurrent)
- Prend en entrée les données historiques et variables externes
- Apprend les paramètres dynamiques :
  - β(t) : taux de transmission
  - γ(t) : taux de guérison

### 2. Modèle SIR (Susceptible - Infecté - Rétabli)
- Utilise les paramètres prédits par le LSTM
- Génère les prévisions des cas futurs

## 📈 Modèles comparés

- ✅ LSTM + SIR (modèle hybride)
- ✅ LSTM pur
- ✅ SIR classique

## 📊 Résultats (horizon 14 jours)

| Modèle              | RMSE  | MAE   |
|---------------------|------|------|
| LSTM                | 3.514 | 2.792 |
| LSTM + SIR hybride  | 3.948 | 2.171 |
| SIR classique       | 3.949 | 2.170 |

👉 Le LSTM pur réduit mieux les grandes erreurs (RMSE), tandis que les modèles structurés ont une meilleure erreur moyenne (MAE).

## 💡 Apports du modèle hybride

- Combine puissance du deep learning et interprétabilité du SIR
- Capture les effets de :
  - la mobilité
  - la température
  - les mesures sanitaires
- Permet d’estimer des paramètres épidémiologiques dynamiques

## 🔬 Données

- Données simulées
- Population : 100 000 individus
- Période : 220 jours
- Entraînement : 75 % / Test : 25 %

## 🚀 Améliorations futures

- Application à des données réelles (ex : COVID-19)
- Intégration de données multi-régions
- Amélioration de l’estimation des paramètres

## 👨‍💻 Auteurs

- Lyonel Sydney DINZEBI
- Houssein Robleh Abdisalam
