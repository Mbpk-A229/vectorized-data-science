# 📌 Projet 01 : Traitement d'Images & Segmentation de Formes

> **Stack :** NumPy • SciPy (ndimage) • Matplotlib

## 1. Contexte & Description du Problème
Dans de nombreux domaines d'ingénierie et de recherche scientifique, l'analyse manuelle d'images pour dénombrer des objets ou calculer des métriques physiques est une tâche fastidieuse et sujette aux erreurs humaines. L'objectif de ce projet est de concevoir un pipeline automatisé d'analyse d'images basé uniquement sur des opérations matricielles et morphologiques.

## 2. Énoncé des Objectifs
À partir d'une image d'entrée présentant du bruit d'acquisition et des variations de luminosité, l'algorithme doit accomplir les tâches suivantes sans recourir à des bibliothèques haut niveau (comme OpenCV) :
- Convertir et structurer l'image sous forme de matrice bidimensionnelle d'intensité.
- Isoler les structures d'intérêt du fond via une technique d'indexation booléenne adaptée.
- Éliminer les artefacts et le bruit de fond au moyen d'opérations de morphologie mathématique.
- Identifier chaque objet indépendant, déduire le nombre total d'éléments et calculer la surface moyenne en pixels.
- Générer un rapport visuel complet comparant l'état initial et la segmentation finale.

> ⚠️ **Contraintes d'implémentation :**
> - Aucune boucle explicite pour le traitement des pixels.
> - Utilisation exclusive des masques booléens NumPy et des fonctions morphologiques SciPy.

## 3. Critères de Validation
1. L'image segmentée ne doit contenir aucun bruit parasite résiduel.
2. Le décompte des objets doit correspondre exactement au nombre réel d'éléments distincts.
3. L'affichage graphique final doit présenter de manière claire la carte des labels et l'histogramme des surfaces calculées.
