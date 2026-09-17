# Base de données — Assurance habitation

## Contexte / besoin métier

Ce projet vise à structurer une base de données d'assurance habitation afin de rendre les informations sur les contrats facilement interrogeables et exploitables.

Le besoin consiste à organiser les données contractuelles et géographiques dans une structure relationnelle claire, puis à répondre à des questions métier à l'aide de requêtes SQL.

## Données

Deux ensembles principaux sont organisés :

### REGION
Informations géographiques :

- code commune / département ;
- région ;
- académie ;
- département ;
- commune.

### CONTRAT
Informations liées aux contrats :

- identifiant du contrat ;
- adresse ;
- surface ;
- type de local ;
- occupation ;
- type de contrat ;
- formule ;
- valeur déclarée des biens ;
- prix de cotisation mensuel.

## Démarche

1. Construction d'un **dictionnaire de données**.
2. Conception d'un **schéma relationnel**.
3. Création des tables SQL `REGION` et `CONTRAT`.
4. Mise en place d'une clé étrangère reliant les contrats à leur zone géographique.
5. Développement de requêtes SQL permettant de répondre à différents besoins métier.

## Exemples d'analyses SQL

- contrats et surfaces pour la commune de Caen ;
- maisons du département 71 selon le type de contrat et la formule ;
- liste des régions françaises ;
- cinq contrats disposant des surfaces les plus élevées ;
- prix moyen de la cotisation mensuelle ;
- nombre de contrats par valeur déclarée des biens ;
- nombre de formules « Integral » en Pays de la Loire ;
- surface moyenne des contrats à Paris ;
- classement des dix départements où la cotisation moyenne est la plus élevée ;
- communes ayant au moins 150 contrats ;
- nombre de contrats par région.

## Résultat / valeur métier

La base relationnelle permet de centraliser les informations et de produire rapidement des analyses par contrat, commune, département ou région.

Elle constitue une structure plus fiable pour répondre à des questions métier récurrentes sans retraitement manuel des données.

## Limites et prochaines pistes

Prochaines améliorations possibles :

- ajouter des contrôles automatiques de qualité ;
- optimiser les performances sur une volumétrie plus importante ;
- créer des vues SQL dédiées aux indicateurs les plus utilisés ;
- connecter la base à un outil de visualisation.

## Compétences démontrées

`SQL` `Modélisation relationnelle` `JOIN` `GROUP BY` `Agrégations` `Data modelling`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./02_presentation_bdd_assurance_habitation)
