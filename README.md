# 🛠️ R Clustering Cheat Sheet

[![R-Version](https://img.shields.io/badge/R-%3E%3D%204.0.0-blue.svg)](https://www.r-project.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Guide technique, théorique et méthodologique du clustering géométrique sous R. Ce dépôt rassemble les implémentations autonomes, les démonstrations mathématiques et les bonnes pratiques pour maîtriser l'apprentissage non supervisé tout en évitant les pièges algorithmiques classiques.

🌐 **Version HTML interactive :** [https://pierrickvernet.github.io/r-clustering-cheat-sheet/fiche_Kmeans.html](https://pierrickvernet.github.io/r-clustering-cheat-sheet/fiche_Kmeans.html)

---

## 📌 Aperçu du Projet

En data science, le partitionnement de données (*clustering*) et la réduction de dimension reposent sur des fondements géométriques stricts. Ce dépôt propose une synthèse de niveau Master (Statistiques Multivariées) pour appréhender les coulisses mathématiques des algorithmes et leur comportement exact sous R.

### 🎯 Objectifs
* **Rigueur Théorique :** Comprendre la décomposition de l'inertie (Théorème de Huygens), les métriques de Minkowski, et le critère de Ward.
* **Sécurisation du Code :** Identifier et contourner les comportements par défaut de R (biais de variance avec `scale()`, remplissage de `matrix()`, argument `d` de `hclust()`).
* **Autonomie :** Fournir des blocs de code R reproductibles, sans dépendances externes complexes, applicables du jeu de données jouet aux *Big Data*.

---

## 🗺️ Sommaire Analytique

1. **Théorie : Apprentissage et Structures de Données**
   * Différences fondamentales avec le supervisé ($k$-NN, SVM).
   * Représentation matricielle et piège du remplissage ligne/colonne.
2. **Métriques, Variances et Standardisation**
   * Choix méthodologique : Z-score vs Min-Max.
   * Correction de la variance empirique non corrigée ($\sigma$) vs variance estimée ($s^2$).
3. **Espaces Métriques & Dissimilarités**
   * Distances d'Euclide, de Manhattan et de Tchebychev ($L_p$).
4. **Algorithme des K-Means**
   * Optimisation locale et gestion du paramètre `nstart`.
5. **Classification Ascendante Hiérarchique (CAH)**
   * Coût de fusion de Ward et ajustement rigoureux des distances au carré.
6. **Validation de la Partition**
   * Méthode du coude, score de silhouette moyen et statistique du Gap.
7. **Stratégies Avancées & Analyse Factorielle**
   * Pré-clustering pour données massives, traitement des données mixtes (`PCAmix`) et ACP.


## 🛠️ Technologies & Packages Utilisés

L'ensemble des scripts s'appuie principalement sur les fonctions natives de R pour garantir une pérennité maximale du code. Les extensions suivantes sont exploitées pour les besoins avancés :

* **FactoMineR** : Pour l'interprétation des classes via le V-test (`catdes()`).
* **PCAmixdata** : Pour le codage et l'analyse factorielle des variables mixtes.

---

## ✍️ Auteur

* **Pierrick Vernet** – Master IREF (Université de Bordeaux)
* GitHub : [@pierrickvernet](https://github.com/pierrickvernet)

---

## 📄 License

Ce projet est sous licence MIT. N'hésitez pas à l'utiliser, le fork ou l'enrichir pour vos propres révisions ou projets.
