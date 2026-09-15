# Tableau de bord dynamique Power BI — Pilotage de projets

## Contexte / besoin métier

Dans le cadre d’une mission ESN Data chez Sanitoral, l’objectif est de concevoir un tableau de bord Power BI pour piloter l’avancement de projets IT et Marketing selon trois axes : **délais, budgets et livrables**.

## Données et outil

Les données couvrent la période **2018 à début 2022** et proviennent d’une note de cadrage, d’extractions d’un logiciel de gestion de projets et d’un dictionnaire de données.

Outil principal : `Power BI Desktop`

## Démarche

### 1. Recueil des besoins avec un Product Strategy Canvas

- **Directeur général** : budget total, dépassements, projets en retard, alerte au-delà de 15 %, arbitrage IT/Marketing.
- **Directeur régional** : pays en difficulté, carte des retards, informations détaillées via info-bulles.
- **Directeur pays** : suivi des phases dans le temps, diagramme de Gantt et boîte Q&A.

### 2. Préparation dans Power Query

Suppression des lignes et colonnes vides, promotion des en-têtes, correction des types, fusion des requêtes et désactivation du chargement des tables intermédiaires.

### 3. Modélisation

Le modèle repose sur un **schéma en étoile** : table de faits `Projects_plans` à la granularité Projet + Phase, dimensions Pays/Régions, Phases et Types de projets. Les relations sont organisées principalement en un-à-plusieurs, avec une table de liaison `Projects_Locations`. Les indicateurs sont calculés via des mesures DAX.

### 4. Conception du dashboard

Des vues distinctes sont créées pour la direction générale, régionale et pays, afin d’adapter le niveau de détail au besoin décisionnel de chaque utilisateur.

## Valeur métier

Le tableau de bord permet d’identifier rapidement les projets à risque, de surveiller les dépassements budgétaires, d’analyser les retards et de faciliter les arbitrages à plusieurs niveaux de management.

## Limites et prochaines pistes

Automatiser davantage le rafraîchissement, enrichir les alertes et mesurer l’usage du dashboard par profil utilisateur.

## Compétences démontrées

`Power BI` `Power Query` `DAX` `Data modelling` `Schéma en étoile` `Dashboard` `Data storytelling`
