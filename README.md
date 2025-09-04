# Prédiction des anomalies de température / Temperature Anomaly Forecasting

## Présentation du projet (FR)

Ce projet vise à anticiper les anomalies de température à l’aide de données climatiques historiques et simulées. Les données utilisées incluent :

- Des anomalies observées entre **1850 et 2021**
- Des simulations climatiques couvrant **1850 à 2099**
- Les incertitudes associées aux observations

### Partie 1 — Exploration et hypothèses

La première phase du projet consiste à manipuler les données, identifier leur structure et formuler des hypothèses :

- Supposition d’une distribution gaussienne pour les données simulées
- Identification du scénario **SSP5-8.5** comme trajectoire probable
- Application de méthodes simples pour prédire les anomalies entre **2090 et 2099**, telles que :
  - Régression linéaire
  - Moyenne pondérée

### Partie 2 — Modélisation avancée

La seconde partie explore des approches plus robustes, en univarié et multivarié :

- Validation croisée pour évaluer les performances
- Modèles utilisés (liste non exhaustive) :
  - **Filtrage de Kalman à un pas (One-step Kalman)**
  - **Régression Ridge**
  - **Random Forest**
- Réduction de dimension via **ACP** sur les données simulées
- Application des modèles sur les données réduites pour affiner les prédictions

---

## Overview (EN)

This project focuses on forecasting temperature anomalies using a combination of historical records and climate model simulations. The dataset includes:

- Observed anomalies from **1850 to 2021**
- Simulated climate data spanning **1850 to 2099**
- Associated uncertainty estimates for observed values

### Phase 1 — Data exploration and assumptions

The initial phase involves data preprocessing, structural analysis, and hypothesis formulation:

- Assuming a Gaussian distribution for simulated data
- Inferring that the simulations follow the **SSP5-8.5** scenario
- Applying baseline forecasting methods for the **2090–2099** period:
  - Linear regression
  - Weighted averaging

### Phase 2 — Advanced modeling techniques

The second phase introduces more sophisticated approaches, both univariate and multivariate:

- Cross-validation to assess model performance
- Models used (non-exhaustive list):
  - **One-step Kalman filter**
  - **Ridge regression**
  - **Random Forest**
- Dimensionality reduction via **Principal Component Analysis (PCA)**
- Predictive models applied to the reduced simulation dataset

---

## Données utilisées / Data Sources

| Type de données (FR)             | Description (FR)                                                                 |
|----------------------------------|----------------------------------------------------------------------------------|
| Anomalies observées              | Écarts de température mesurés entre 1850 et 2021                                |
| Données simulées                 | Projections climatiques de 1850 à 2099, suivant le scénario SSP5-8.5            |
| Incertitudes des observations    | Estimations d’erreur associées aux données historiques                          |

| Data Type (EN)                  | Description (EN)                                                                 |
|----------------------------------|----------------------------------------------------------------------------------|
| Observed anomalies               | Temperature deviations recorded from 1850 to 2021                               |
| Simulated data                   | Climate projections from 1850 to 2099, likely following the SSP5-8.5 scenario   |
| Observation uncertainties        | Error estimates associated with historical measurements                         |

---

## Fichiers du projet / Project Files

### Notebooks

| Fichier              | Description (FR)                                                                 | Description (EN)                                                                 |
|----------------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `part_1.ipynb`       | Exploration des données, hypothèses, manipulation et premières méthodes          | Data exploration, assumptions, manipulation, and initial forecasting methods     |
| `part_2.ipynb`       | Modélisation avancée : Kalman, Ridge, Random Forest, ACP...                      | Advanced modeling: Kalman, Ridge, Random Forest, PCA...                            |

### Rapport

| Fichier              | Description (FR)                                                                 | Description (EN)                                                                 |
|----------------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| `part2_report.pdf`   | Résultats et interprétations du notebook `part_2.ipynb`                          | Results and insights from the `part_2.ipynb` notebook                            |

### Matrices `.npy`

| Variable Python              | Fichier source         | Description (FR)                                               | Description (EN)                                               |
|-----------------------------|------------------------|----------------------------------------------------------------|----------------------------------------------------------------|
| `data_simulated_past`       | `matrix_3.npy`         | Données simulées du passé (1850-2021)                          | Simulated past data (1850-2021)                               |
| `data_simulated_future`     | `matrix_1.npy`         | Données simulées du futur (2022–2099)                          | Simulated future data (2022–2099)                             |
| `data_observed_past`        | `matrix_2.npy`         | Données observées historiques (1850–2021)                      | Historical observations (1850–2021)                           |
| `data_observed_past_sigma`  | `matrix_4.npy`         | Incertitudes associées aux données observées                   | Uncertainty estimates for observed data                       |

---

## Auteurs / Authors

**Aboukacem Elias**  
**Lahontaa Theo**
