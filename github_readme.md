<div align="center">

  ![Header Banner](https://via.placeholder.com/1200x400/0d1117/58a6ff?text=Bank+Credit+Card+Fraud+Detection+%7C+Isolation+Forest+in+R)

  # 🛡️ Détection de Fraude Bancaire par Machine Learning
  ### *Détection d'anomalies non supervisée sur des transactions bancaires avec R*

  [![Language](https://img.shields.io/badge/Language-R-blue.svg)](https://www.r-project.org/)
  [![Algorithm](https://img.shields.io/badge/Algorithm-Isolation%20Forest-orange.svg)](https://github.com/david-cortes/isotree)
  [![Dataset](https://img.shields.io/badge/Dataset-Kaggle%20ULB-green.svg)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
  [![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](#)

</div>

---

## 🎯 Objectif du Projet

Ce projet s'intéresse à la **détection non supervisée d'anomalies** dans un contexte de transactions par carte bancaire fortement déséquilibrées. L'objectif principal est de repérer efficacement les comportements frauduleux en utilisant l'algorithme **Isolation Forest** sans s'appuyer sur des étiquettes d'apprentissage historiques durant l'étape d'isolement.

---

## 📊 Données & Prétraitement

- **Source :** Jeu de données Kaggle [Credit Card Fraud Detection (ULB)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).
- **Volume initial :** 284 807 transactions bancaires.
- **Déséquilibre :** Seulement **0,17 %** de transactions frauduleuses (ratio de 1 pour 578).

### 🛠️ Nettoyage et Feature Engineering
1. **Déduplication :** Suppression de 1 081 doublons identifiés dans le jeu d'origine.
2. **Normalisation :** Standardisation z-score des variables `Amount` et `Time`.
3. **Analyse Exploratoire (EDA) :** Étude comparative des distributions marginales et des matrices de corrélation entre classes.

> ⚠️ **Note sur le jeu de données local (`creditcard_sample.csv`) :**  
> Le fichier complet (143 Mo) étant volumineux pour GitHub, un échantillon de démonstration de **4 992 transactions (dont 492 fraudes, soit ~10%)** est mis à disposition. Les métriques obtenues sur cet échantillon varient donc de celles publiées dans le rapport global. Pour exécuter le code complet, téléchargez le fichier source et adaptez le chemin d'accès dans le script.

---

## 🔬 Méthodologie

```mermaid
flowchart LR
    A[Données Brutes] --> B[Nettoyage & Deduplication]
    B --> C[Standardisation Z-Score]
    C --> D[Modélisation Isolation Forest]
    D --> E[Analyse de Sensibilité du Seuil]
    E --> F[Évaluation: Précision / Rappel / F1]
```

1. **Modélisation :** Construction du modèle d'isolation au moyen du package R `isotree`.
2. **Calibrage du seuil :** Analyse de sensibilité afin de régler le seuil d'anomalie et d'optimiser le compromis entre la **Précision**, le **Rappel** et le **F1-Score**.

---

## 📁 Structure du Dépôt

```bash
.
├── script Banking fraud detection.R  # Script R complet (Prétraitement, IF, Évaluation)
├── Banking_Fraud_Detection.pdf       # Rapport d'analyse complet en format PDF
├── creditcard_sample.csv             # Échantillon de démonstration (4 992 obs.)
└── README.md                         # Documentation du projet
```

---

## 🛠️ Outils & Bibliothèques R

- **R Base & Tidyverse :** Manipulation de données et visualisations.
- **`isotree` :** Implémentation haute performance de l'algorithme *Isolation Forest*.
- **`caret` / `PRROC` :** Calcul des métriques et courbes d'évaluation.

---

## 👩‍💻 Auteure

**Amina Mir** ([@amina-mir](https://github.com/amina-mir))  
*Master Économie Appliquée et Data Science*  
FSJES Meknès — Université Moulay Ismail

---

<div align="center">
  <i>Si ce projet vous a été utile, n'hésitez pas à lui accorder une ⭐️ sur GitHub !</i>
</div>