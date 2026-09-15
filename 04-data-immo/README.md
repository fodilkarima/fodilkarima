# DATA Immo — Analyse et structuration de données immobilières

## Contexte / besoin métier

Le marché immobilier nécessite des données fiables pour analyser les écarts de prix et mieux accompagner les décisions des agences et de leurs clients.

Le projet consiste à nettoyer, structurer et exploiter des données de transactions immobilières afin de produire des analyses fiables et de préparer une base utilisable pour une future estimation du prix de vente.

## Sources de données

- **Demandes de Valeurs Foncières (DVF)** : transactions immobilières en France ;
- **Référentiel géographique** issu de `data.gouv.fr` ;
- **Données communales de l'INSEE**, notamment démographiques.

## Qualité des données

Plusieurs problèmes sont identifiés dans les données initiales :

- colonnes entièrement vides ;
- informations clés absentes sur certaines lignes ;
- formats non conformes ;
- virgules dans les valeurs numériques ;
- dates à normaliser ;
- codes géographiques nécessitant parfois un zéro initial.

## Démarche

1. Nettoyage et normalisation des fichiers.
2. Transformation des colonnes dans des formats cohérents.
3. Création d'un dictionnaire de données.
4. Construction d'un schéma relationnel normalisé.
5. Création et chargement des tables.
6. Vérification du nombre de lignes, des clés et des jointures.
7. Production de requêtes SQL destinées à répondre à des questions immobilières concrètes.

## Prise en compte du RGPD

Le projet prévoit notamment :

- la suppression des informations personnelles inutiles ;
- l'utilisation de données publiques et anonymisées ;
- une conservation limitée aux besoins du projet ;
- l'absence de réutilisation hors du cadre défini.

## Exemples d'analyses

- nombre total d'appartements vendus au premier semestre 2020 ;
- ventes par région ;
- proportion des ventes selon le nombre de pièces ;
- dix départements où le prix au mètre carré est le plus élevé ;
- prix moyen au mètre carré d'une maison en Île-de-France ;
- dix appartements les plus chers ;
- évolution des ventes entre le premier et le second trimestre 2020 ;
- classement régional du prix au mètre carré des appartements de plus de quatre pièces ;
- communes comptant au moins 50 ventes au premier trimestre ;
- comparaison du prix au mètre carré entre appartements de deux et trois pièces ;
- communes ayant le plus de transactions pour 1 000 habitants.

## Résultat / valeur métier

Le projet transforme plusieurs sources hétérogènes en une base structurée permettant de produire des analyses immobilières reproductibles et de répondre à des questions métier précises.

## Limites et prochaine étape

Le support partagé montre principalement la préparation des données, la structuration de la base et les analyses SQL. La prochaine étape logique consiste à exploiter cette base pour construire et évaluer un **modèle d'estimation du prix de vente**, conformément à l'objectif initial du projet.

## Compétences démontrées

`SQL` `Data cleaning` `Modélisation` `Qualité des données` `RGPD` `Analyse immobilière`
