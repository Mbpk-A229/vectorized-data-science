# 📌 Projet 03 : Moteur de Régression & Ajustement de Courbes (Curve Fitting)

> **Stack :** NumPy • SciPy (`optimize`) • Matplotlib

---

## 1. Contexte & Description du Problème
En modélisation statistique et physique, il est fréquent qu'un phénomène ne puisse pas être décrit par un simple modèle linéaire. Il devient alors nécessaire d'ajuster des modèles mathématiques complexes (non-linéaires, exponentiels ou polynomiaux) à des observations expérimentales entachées d'incertitudes.

---

## 2. Énoncé des Objectifs
Concevoir un moteur d'optimisation capable d'estimer automatiquement les paramètres théoriques d'un système à partir d'un ensemble de données bruitées :

- Formuler une fonction cible paramétrique complexe (ex: combinaison d'harmoniques ou loi d'atténuation exponentielle).
- Simuler un jeu de données synthétiques comportant un bruit gaussien contrôlé.
- Optimiser la recherche des paramètres en minimisant l'erreur quadratique via un algorithme de résolution numérique.
- Calculer la matrice de covariance pour évaluer l'incertitude et les intervalles de confiance sur chaque paramètre estimé.
- Visualiser la convergence du modèle théorique ajusté sur les observations.

> ⚠️ **Contraintes d'implémentation :**
> - Interdiction d'utiliser les régressions automatiques de Scikit-Learn (`LinearRegression`, etc.).
> - Emploi direct des modules d'optimisation numérique de SciPy (`curve_fit` / `minimize`).
> - **Développement 100% autonome :** Aucune assistance ni génération de code par IA n'a été utilisée pour résoudre ce problème.

---

## 3. Critères de Validation
1. Convergence des paramètres estimés vers les valeurs théoriques avec une erreur relative minime.
2. Calcul rigoureux de l'écart-type sur l'estimation des paramètres.
3. Affichage clair montrant les points expérimentaux, la fonction réelle et la courbe d'ajustement.
