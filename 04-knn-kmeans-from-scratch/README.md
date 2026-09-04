# 📌 Projet 04 : Classifieur KNN & Clustering K-Means Vectorisé (From Scratch)

> **Stack :** Pure NumPy Vectorization • Matplotlib

---

## 1. Contexte & Description du Problème
La plupart des algorithmes d'apprentissage automatique s'appuient sur des calculs géométriques dans des espaces à haute dimension. Comprendre le fonctionnement interne d'un algorithme nécessite d'être capable de le coder sans frameworks de haut niveau, tout en optimisant les performances grâce au calcul matriciel vectorisé.

---

## 2. Énoncé des Objectifs
Coder l'algorithme des K-Plus Proches Voisins (KNN) ou du Clustering K-Means sans utiliser de boucles `for` d'itération sur les échantillons :

- Standardiser les données d'entrée via une transformation Z-score matricielle.
- Calculer la matrice des distances euclidiennes entre tous les points en exploitant le **Broadcasting N-dimensionnel**.
- Extraire les indices des plus proches voisins et attribuer les classes majoritaires ou réallouer les centroïdes.
- Évaluer la précision de la classification ou l'inertie du clustering sur un jeu de test.
- Tracer les frontières de décision 2D ou le regroupement des clusters à l'aide de Matplotlib.

> ⚠️ **Contraintes d'implémentation :**
> - Interdiction stricte d'importer `sklearn`.
> - Aucune boucle `for` autorisée lors du calcul des distances inter-échantillons (calcul 100% vectorisé en mémoire via NumPy).
> - **Développement 100% autonome :** Aucune assistance ni génération de code par IA n'a été utilisée pour résoudre ce problème.

---

## 3. Critères de Validation
1. Précision ou convergence identique à celle offerte par les bibliothèques standards.
2. Temps d'exécution quasi-instantané grâce à la vectorisation.
3. Visualisation claire des régions de décision ou de la trajectoire des centroïdes.
