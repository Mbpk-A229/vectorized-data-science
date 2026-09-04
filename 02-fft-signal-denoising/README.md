# 📌 Projet 02 : Réduction du Bruit Signal par Transformée de Fourier (FFT)

> **Stack :** NumPy • SciPy (`fftpack`, `signal`) • Matplotlib

---

## 1. Contexte & Description du Problème
Les signaux physiques (acoustiques, capteurs IoT, séries temporelles financières) sont fréquemment corrompus par du bruit haute fréquence ou des dérivées de basse fréquence. Pour extraire l'information fondamentale d'une mesure, il est indispensable de manipuler le signal dans le domaine fréquentiel.

---

## 2. Énoncé des Objectifs
Construire un algorithme complet de filtrage fréquentiel à partir d'une série temporelle fortement parasitée par un bruit aléatoire et affectée d'une tendance linéaire :

- Supprimer la composante continue et la tendance globale du signal d'origine.
- Projeter le signal temporel dans le domaine fréquentiel en calculant sa Transformée de Fourier Rapide (FFT).
- Analyser le spectre d'amplitude et isoler les fréquences dominantes via un filtre à seuillage vectoriel.
- Reconstruire le signal purifié dans le domaine temporel au moyen de la Transformée de Fourier Inverse (IFFT).
- Comparer la fidélité du signal reconstruit par rapport au signal initial.

> ⚠️ **Contraintes d'implémentation :**
> - Le filtrage des fréquences parasites doit s'effectuer exclusivement par masquage d'un tableau NumPy dans le spectre de Fourier.
> - Représentation graphique obligatoire du spectre fréquentiel avant et après filtrage.
> - **Développement 100% autonome :** Aucune assistance ni génération de code par IA n'a été utilisée pour résoudre ce problème.

---

## 3. Critères de Validation
1. Atténuation spectrale d'au moins 90% du bruit haute fréquence.
2. Conservation exacte de la fréquence fondamentale et de l'amplitude du signal d'origine.
3. Superposition claire sur un même graphique du signal bruité et du signal filtré.
