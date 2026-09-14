# 📌 Projet 05 : Analyse Exploratoire (EDA), Séries Temporelles & Visualisation

> **Stack :** Pandas • Seaborn • Matplotlib • Pure Python

---

## 1. Contexte & Description du Problème

L'analyse exploratoire de données (EDA) et la préparation des jeux de données (*Data Cleaning* & *Feature Engineering*) constituent les étapes indispensables de tout pipeline de Data Science et de Machine Learning.

Ce projet met en pratique l'ensemble des techniques fondamentales de manipulation de tableaux de données (`Series` et `DataFrame`), le traitement des valeurs manquantes, l'ingénierie de variables, l'analyse stratégique de séries temporelles sans biais du futur, ainsi que la visualisation statistique avancée.

---

## 2. Structure des Exercices & Compétences Clés

| Exercice | Domaine / Objectif | Méthodes Pandas & Seaborn Clés |
| :--- | :--- | :--- |
| **01. Data Cleaning & Feature Engineering** | Nettoyage & analyse croisée sur dataset démographique | `.dropna()`, `.loc`, `.cat.codes`, `.groupby()`, `sns.boxplot` |
| **02. Time Series & Look-Ahead Bias** | Stratégie d'indicateurs glissants sans fuite temporelle | `DatetimeIndex`, `.rolling()`, `.shift(1)`, `.resample()`, `sns.lineplot` |
| **03. Fusion & Matrice de Corrélation** | Croisement multi-sources & mesure d'association | `pd.merge()`, `.corr()`, `sns.heatmap(annot=True)` |

---

## 3. Détail des Exercices

### 🧪 Exercice 1 : Cleaning & Feature Engineering (Dataset Passagers)
* **Inspection & Nettoyage :** Diagnostic des dimensions (`shape`) et suppression contrôlée des données manquantes (`dropna`).
* **Feature Engineering :** Découpage de variables continues en tranches catégorielles avec `.loc` (*Économique*, *Standard*, *Luxe*) et conversion numérique (`.cat.codes`).
* **Agrégation & Visualisation :** Groupement croisé via `.groupby()` pour calculer les taux de survie/médianes, puis analyse des valeurs aberrantes (*outliers*) avec `sns.boxplot`.

### 📈 Exercice 2 : Séries Temporelles & Prévention du Biais du Futur (Crypto / Bourse)
* **Indexation Temporelle :** Conversion et filtrage dynamique via `DatetimeIndex`.
* **Indicateurs Glissants :** Calcul de moyennes mobiles avec `.rolling(window=N).mean()`.
* **Règle d'Or Temporelle :** Application stricte de `.shift(1)` sur toute fenêtre glissante pour éliminer le *look-ahead bias* (utilisation de données du futur $t+1$).
* **Rééchantillonnage :** Changement de fréquence temporelle (`.resample('M')`) et calcul des variations absolues (`.diff()`).

### 📊 Exercice 3 : Fusion Multi-Sources & Matrice de Corrélation
* **Alignement d'Index :** Fusion interne de DataFrames temporels autonomes via `pd.merge(..., how='inner', on='Date')`.
* **Analyse Linéaire :** Calcul des coefficients de corrélation de Pearson (`.corr()`).
* **Rendu Graphique :** Restitution de la carte thermique annotée avec `sns.heatmap(annot=True)`.

---

## 4. Contraintes d'Implémentation & Bonnes Pratiques

> ⚠️ **Directives de Développement :**
> * **Indexation Explicite :** Utilisation obligatoire de `.loc` ou `.iloc` pour éviter les avertissements d'assignation `SettingWithCopyWarning`.
> * **Alignement Temporel :** Application systématique de `.shift(1)` lors du calcul d'indicateurs financiers ou prédictifs.
> * **Engagement d'Autonomie :** L'intégralité du code et de la logique de traitement a été conçue et rédigée manuellement, sans génération ni assistance par IA.

---

## 5. Critères de Validation

- [ ] **Intégrité :** Imputation ou suppression complète des cellules nulles sur les jeux de données d'entraînement.
- [ ] **Exactitude Graphique :** Graphiques Seaborn/Matplotlib annotés, lisibles et correctement dimensionnés.
- [ ] **Validité Temporelle :** Absence totale de fuite de données futures sur les séries rééchantillonnées et décalées.
