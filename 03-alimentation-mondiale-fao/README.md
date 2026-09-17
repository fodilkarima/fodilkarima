# Étude de l'alimentation mondiale — FAO

## Contexte / besoin métier

L'objectif est d'analyser la disponibilité et l'utilisation des ressources alimentaires mondiales à partir de données de la **FAO**.

L'étude cherche notamment à mesurer l'ampleur de la sous-nutrition, à comparer la quantité de nourriture disponible aux besoins de la population et à étudier l'utilisation des ressources alimentaires.

## Données

Quatre fichiers CSV sont exploités :

- `dispo_alimentaire.csv` : disponibilité alimentaire et utilisations par pays et produit ;
- `sous_nutrition.csv` : population en sous-alimentation ;
- `population.csv` : population par pays et année ;
- `aide_alimentaire.csv` : aide alimentaire reçue entre 2013 et 2016.

Les données comprennent des variables quantitatives — population, production, disponibilité, pertes, aide alimentaire — et qualitatives — pays, produit, origine et type d'utilisation.

## Démarche

1. Import des fichiers CSV.
2. Harmonisation des noms de colonnes.
3. Conversion des unités et création de nouvelles variables.
4. Calcul de proportions et d'indicateurs.
5. Fusion des tables avec `merge()` sur les clés pertinentes.
6. Agrégation avec `groupby()`.
7. Visualisation à l'aide de graphiques en barres, courbes, secteurs et nuages de points.

### Outils

`Python` `Pandas` `Matplotlib` `Google Colaboratory`

## Résultats clés

- Population mondiale étudiée en 2017 : **7,54 milliards** d'habitants.
- Population en situation de sous-nutrition : **535,7 millions**, soit environ **7,1 %**.
- La disponibilité calorique mondiale correspond théoriquement à la nourriture nécessaire pour environ **8,37 milliards** de personnes sur la base de 2 500 kcal/jour.
- Les ressources végétales représenteraient théoriquement de quoi nourrir environ **6,9 milliards** de personnes.
- L'analyse met en évidence des écarts importants entre disponibilité globale et accès effectif à l'alimentation.
- Pour la Thaïlande, environ **83,41 %** du manioc étudié est exporté alors qu'une partie de la population reste en situation de sous-nutrition.
- Le nuage de points entre aide alimentaire et sous-nutrition ne met pas en évidence de relation linéaire forte.

## Interprétation métier

Les résultats suggèrent que la disponibilité alimentaire globale ne suffit pas à expliquer la faim dans le monde. La répartition, l'accès économique, les pertes, l'utilisation des céréales et la distribution de l'aide jouent également un rôle important.

## Recommandations

- améliorer la répartition des ressources alimentaires ;
- réduire les pertes ;
- mieux coordonner l'aide humanitaire ;
- surveiller l'écart entre disponibilité alimentaire nationale et accès réel des populations.

## Limites et prochaines pistes

- Une partie importante de l'analyse de disponibilité repose sur l'année **2017**.
- Les données d'aide alimentaire couvrent **2013 à 2016**.
- Une analyse temporelle plus longue permettrait de mieux mesurer les évolutions.
- L'intégration d'indicateurs économiques et climatiques permettrait d'enrichir l'explication des écarts observés.

## Compétences démontrées

`Python` `Pandas` `Matplotlib` `Data cleaning` `Merge` `GroupBy` `Analyse exploratoire`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./03_presentation_alimentation_mondiale_fao.pdf)
- 📓 [Consulter le notebook Python](./03_alimentation_mondiale_fao.ipynb)
