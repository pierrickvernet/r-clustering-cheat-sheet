# R Clustering Fiche de Révision

[Fiche K-means HTML](https://pierrickvernet.github.io/r-clustering-cheat-sheet/fiche_Kmeans.html).

## 1. INTRODUCTION
- **Cadre de réalisation :** Aide-mémoire technique, théorique et méthodologique de statistique computationelle.
- **Présentation du sujet :** Ce dépôt rassemble un guide technique et théorique dédié au partitionnement de données (*clustering*) géométrique et à la réduction de dimension sous R. Il combine démonstrations mathématiques, bonnes pratiques de code et implémentations R autonomes.
- **Intérêt et cas d'usage :** Permettre aux analystes et recruteurs d'appréhender le fonctionnement interne des algorithmes d'apprentissage non supervisé, de maîtriser la décomposition de l'inertie et d'éviter les biais d'implémentation fréquents sous R (gestion de la variance, métriques de distance, paramètres d'agrégation).

---

## 2. SOURCES ET DONNÉES
- **Origine des données :** Structures matricielles, jeux de données synthétiques et cas pratiques manipulés directement dans l'environnement R.
- **Périmètre et caractéristiques :**
  - Traitement des données quantitatives continues et des jeux de données mixtes (combinaison de variables numériques et catégorielles).
  - Couverture des approches applicables des petits échantillons aux architectures de pré-clustering pour volumes de données plus importants.

---

## 3. MÉTHODOLOGIE ET DÉTAILS TECHNIQUES

### Pipeline d'analyse et fondements mathématiques
1. **Géométrie des données et prétraitement :**
   - **Décomposition de l'inertie :** Application du théorème de Huygens ($Inertie\ Totale = Inertie\ Intra-classe + Inertie\ Inter-classe$).
   - **Standardisation :** Comparaison entre centrage-réduction ($Z$-score) et normalisation Min-Max. Prise en compte du calcul de la variance empirique ($\sigma$) par rapport à la variance corrigée ($s^2$) dans les fonctions natives R.
   - **Espaces métriques :** Mesure des dissimilarités via les distances de Minkowski ($L_p$ : Euclidienne, Manhattan, Tchebychev).
2. **Algorithmes de classification :**
   - **$k$-means :** Minimisation de l'inertie intra-classe et gestion de la convergence vers un optimum local via le paramètre `nstart`.
   - **Classification Ascendante Hiérarchique (CAH) :** Minimisation du coût de fusion selon le critère de Ward et manipulation des matrices de distances au carré.
   - **Réduction de dimension & Données mixtes :** Prise en charge des variables hybrides via l'Analyse en Composantes Principales (ACP) et les méthodes factorielles du package `PCAmixdata`.
3. **Évaluation et validation des partitions :**
   - Méthode du coude (optimisation de l'inertie).
   - Indice de Silhouette moyen.
   - Statistique du Gap.
   - Caractérisation des classes par la valeur-test ($V$-test) pour identifier les variables significativement discriminantes.

### Technologies et bibliothèques (Environnement R)
- **R Markdown / HTML :** `knitr`, `rmarkdown` pour la génération des fiches interactives.
- **Fonctions natives R (`stats`) :** `kmeans()`, `hclust()`, `dist()`, `scale()`, `prcomp()`.
- **Packages spécialisés :**
  - `FactoMineR` : Interprétation et description des groupes via `catdes()`.
  - `PCAmixdata` : Traitement factoriel des jeux de données mixtes.

---

## 4. CONCLUSION ET RÉSULTATS CLÉS
- **Apports du projet :** Documentation claire assurant le lien entre l'économétrie/statistique multivariée et la mise en œuvre pratique sous R.
- **Consultation directe :** Un support interactif complet est accessible en ligne : [Fiche K-means HTML](https://pierrickvernet.github.io/r-clustering-cheat-sheet/fiche_Kmeans.html).
- **Limites et perspectives :** Extension possible vers la modélisation par mélange de gaussiennes (GMM) et les algorithmes fondés sur la densité (DBSCAN).

---

## 5. STRUCTURE DU DÉPÔT

```text
.
├── .gitattributes         # Configuration des attributs Git
├── README.md              # Documentation du dépôt
├── fiche_Kmeans.Rmd       # Code source RMarkdown du guide interactif
└── fiche_Kmeans.html      # Version HTML compilée et interactive

```

---

