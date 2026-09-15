# Analyse des ventes d'une librairie — Lapage

## Contexte / besoin métier

Lapage est une librairie disposant historiquement de points de vente physiques et ayant développé un site de vente en ligne.

L'objectif de la mission est d'analyser les principaux indicateurs commerciaux afin de comprendre la performance de l'activité, d'identifier les profils clients et les catégories de produits les plus contributrices, puis de proposer des pistes d'action pour améliorer le chiffre d'affaires.

## Outil

`Python`

## Démarche

L'analyse est structurée en deux volets complémentaires.

### 1. Analyse descriptive des ventes

Les indicateurs étudiés portent sur :

- l'évolution du chiffre d'affaires ;
- le nombre de clients ;
- le nombre de transactions ;
- les meilleurs clients ;
- les produits les plus et les moins contributeurs ;
- la répartition du chiffre d'affaires par catégorie ;
- le profil d'âge des clients ;
- la concentration du chiffre d'affaires via une courbe de Lorenz et l'indice de Gini.

### 2. Analyse bivariée des comportements clients

Plusieurs relations sont étudiées statistiquement :

- genre ↔ catégorie de livres achetés ;
- âge ↔ montant total des achats ;
- âge ↔ fréquence d'achat ;
- âge ↔ panier moyen ;
- âge ↔ catégorie de livres achetés.

Les tests utilisés incluent :

- **Chi-2** pour l'association entre deux variables qualitatives ;
- **Spearman** pour les relations monotones non linéaires ;
- **Shapiro-Wilk** pour contrôler la normalité ;
- **Kruskal-Wallis** pour comparer les distributions d'âge entre catégories.

## Résultats clés

- L'activité reste globalement stable, avec des pics autour d'**octobre 2021** et **mars 2022**.
- La **catégorie 1** est la plus contributrice au chiffre d'affaires.
- La **catégorie 2** présente des prix plus élevés mais contribue moins au chiffre d'affaires.
- Les **35–55 ans** constituent le cœur de clientèle.
- Les **moins de 35 ans** ont un panier moyen plus élevé.
- Quatre clients se distinguent fortement et ont été considérés comme des profils **BtoB**.
- Après retrait de ces quatre clients, l'indice de Gini passe de **0,44 à 0,40**, indiquant une répartition plus homogène du CA en BtoC.
- Le test du Chi-2 met en évidence une dépendance statistiquement significative entre genre et catégorie achetée.
- Les analyses montrent également une relation significative entre âge et comportement d'achat.
- La catégorie 2 se distingue par une clientèle plus jeune.

## Recommandations métier

- renforcer la visibilité et la mise en avant de la catégorie 1 ;
- mieux valoriser la catégorie 2 afin d'accroître son volume de ventes ;
- fidéliser davantage les 35–55 ans ;
- cibler les moins de 35 ans avec des offres à plus forte valeur ;
- différencier la gestion commerciale des clients BtoB et BtoC ;
- revoir le positionnement ou la visibilité des produits les moins contributeurs.

## Limites et prochaines pistes

- approfondir la saisonnalité des pics observés ;
- isoler davantage les comportements BtoB dans les analyses ;
- intégrer des données de campagnes marketing ou de promotions ;
- suivre la rentabilité produit en complément du chiffre d'affaires.

## Compétences démontrées

`Python` `Analyse statistique` `Chi-2` `Spearman` `Kruskal-Wallis` `Segmentation client` `Data storytelling`
