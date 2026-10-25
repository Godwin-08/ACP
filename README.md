# Analyse en composantes principales (ACP) sur les indicateurs socio-économiques des pays

## 1. Présentation du projet

Ce projet a pour objectif d’appliquer l’analyse en composantes principales (ACP) à un jeu de données contenant des indicateurs socio-économiques de plusieurs pays. L’ACP permet de réduire la dimension d’un ensemble de variables corrélées afin de repérer les structures principales et les oppositions entre observations.

Le jeu de données contient des variables telles que :
- mortalité infantile
- exportations
- dépenses de santé
- importations
- revenu
- inflation
- espérance de vie
- fécondité
- PIB par habitant

L’objectif principal est de comprendre comment les pays se distinguent selon leur niveau de développement économique et social.

## 2. Données utilisées

Le fichier utilisé est :
- donnees_pays.csv

Il contient :
- le nom des pays
- plusieurs variables quantitatives représentant des indicateurs économiques et sociaux

Les données sont issues de sources internationales et regroupent un ensemble de pays pour une analyse comparative.

## 3. Objectif de l’analyse

L’ACP permet de :
- synthétiser les informations contenues dans plusieurs variables
- repérer les dimensions principales de différence entre les pays
- visualiser les relations entre les variables
- identifier les pays les plus similaires ou les plus opposés

Dans cette étude, l’intérêt est surtout de voir si les pays peuvent être organisés selon un axe de développement économique et sanitaire.

## 4. Méthodologie

### 4.1. Nettoyage des données

Avant l’analyse, les lignes contenant des valeurs manquantes sont supprimées afin d’éviter les erreurs de calcul.

### 4.2. Standardisation des variables

Les variables n’ont pas les mêmes unités et ne sont pas directement comparables. Pour cette raison, on centre et on réduit les données.

La formule utilisée est :

z_ij = (x_ij - x̄_j) / σ_j

Cela transforme chaque variable pour qu’elle ait :
- une moyenne de 0
- un écart-type de 1

### 4.3. Matrice de corrélation

Ensuite, on calcule la matrice de corrélation entre les variables. Cette matrice montre les relations entre les données. Par exemple :
- si deux variables sont fortement corrélées, elles évoluent dans le même sens
- si elles sont corrélées négativement, elles varient dans des directions opposées

### 4.4. Valeurs propres et vecteurs propres

L’ACP repose sur le calcul des valeurs propres et des vecteurs propres de la matrice de corrélation.

Les valeurs propres représentent l’inertie expliquée par chaque composante principale.

### 4.5. Composantes principales

Les composantes principales sont définies comme :
- F1, F2, F3, ...
- elles sont construites à partir des variables initiales
- chaque axe correspond à une combinaison linéaire des variables

## 5. Résultats de l’ACP

Les résultats montrent que :
- F1 explique environ 47,25 % de l’inertie totale
- F2 explique environ 16,61 %
- la combinaison F1 + F2 explique environ 63,86 %

Cela signifie que les deux premiers axes capturent une grande partie de la structure des données.

## 6. Interprétation des axes

### Axe F1 : développement socio-économique et sanitaire

L’axe F1 est le plus important. Il oppose :
- les pays ayant un niveau de vie élevé
- aux pays ayant un niveau de vie plus faible

Les variables fortement associées à F1 sont :
- espérance de vie
- revenu
- PIB par habitant
- mortalité infantile
- fécondité

Interprétation :
- Les pays à droite sur F1 ont :
  - une espérance de vie élevée
  - un revenu élevé
  - un PIB par habitant important
  - une mortalité infantile plus faible
- Les pays à gauche sur F1 ont :
  - un revenu plus faible
  - une espérance de vie plus courte
  - une mortalité infantile plus élevée
  - une fécondité plus élevée

Ainsi, F1 représente clairement le niveau de développement.

### Axe F2 : ouverture commerciale

L’axe F2 est principalement porté par :
- exportations
- importations

Il traduit surtout le degré d’ouverture commerciale des économies. Certains pays sont plus orientés vers le commerce international, tandis que d’autres le sont moins.

## 7. Interprétation des figures

### 7.1. Matrice de corrélation

La matrice de corrélation montre les liens entre les variables. Par exemple :
- mortalité infantile et fécondité sont très corrélées
- espérance de vie est corrélée négativement avec mortalité infantile
- revenu et PIB par habitant sont fortement liés
- les variables liées au développement sont globalement opposées aux indicateurs de pauvreté

### 7.2. Plan factoriel F1 x F2

Ce plan permet de visualiser les pays dans un espace réduit. Les pays situés à droite ont souvent un meilleur niveau de développement. Les pays situés à gauche sont généralement moins développés.

Les pays très développés, comme :
- la France
- les États-Unis
- la Norvège

se situent souvent du côté positif de F1. En revanche, des pays comme :
- l’Afghanistan
- le Nigeria
- le Togo

sont généralement situés du côté négatif.

### 7.3. Cercle des corrélations

Le cercle des corrélations permet de voir les relations entre les variables et les axes. Les variables proches les unes des autres sont fortement associées. Les variables opposées sont négativement corrélées.

Par exemple :
- la mortalité infantile et la fécondité sont proches
- l’espérance de vie est opposée à ces deux variables
- le revenu est lié à l’espérance de vie et au PIB par habitant

## 8. Qualité de représentation des variables

La qualité de représentation mesure dans quelle mesure une variable est bien expliquée par les axes du plan. Une variable est bien représentée si elle est proche de l’axe factoriel.

Les variables les mieux représentées sur le plan F1 x F2 sont :
- exportations
- espérance de vie
- mortalité infantile

D’autres variables sont plus faiblement représentées, comme :
- dépenses de santé
- inflation

Cela signifie qu’une partie de leur information est portée par d’autres axes, pas seulement par F1 et F2.

## 9. Contribution des variables aux axes

La contribution permet de savoir quelles variables participent le plus à la construction d’un axe.

Les variables qui contribuent le plus à F1 sont :
- espérance de vie
- mortalité infantile
- fécondité
- revenu
- PIB par habitant

Cela confirme que F1 représente surtout le niveau de développement.

## 10. Conclusion générale

L’ACP permet de conclure que les pays se distinguent surtout selon leur niveau de développement économique et social.

Le premier axe factoriel oppose :
- les pays développés, avec une forte espérance de vie, un revenu élevé et un PIB élevé
- aux pays moins développés, avec une mortalité infantile élevée et une fécondité plus forte

Le deuxième axe, quant à lui, est davantage lié à l’ouverture commerciale et aux échanges internationaux.

Cette analyse fournit ainsi une vue synthétique et très utile de la structure des données. Elle permet de résumer de nombreuses informations dans quelques axes interprétables.

## 11. Outils utilisés

Le projet a été réalisé avec :
- Python
- pandas
- numpy
- matplotlib
- seaborn
- Jupyter Notebook

## 12. Prérequis

Pour exécuter le projet, il faut installer :
- Python 3
- Jupyter Notebook ou JupyterLab
- pandas
- numpy
- matplotlib
- seaborn

Exemple d’installation :

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## 13. Utilisation

Ouvrir le notebook :
- ACP.ipynb

Puis exécuter les cellules dans l’ordre.

## 14. Résumé rapide

L’ACP montre que :
- F1 représente le développement
- F2 représente l’ouverture commerciale
- la plupart des variables de développement sont fortement corrélées
- les pays se répartissent clairement selon leur niveau de richesse et de santé

---

## 15. Fichier associé

- ACP.ipynb : notebook principal contenant le code et les visualisations
- donnees_pays.csv : fichier de données
