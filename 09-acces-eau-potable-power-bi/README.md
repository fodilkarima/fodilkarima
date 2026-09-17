# Accès à l'eau potable dans le monde — Power BI

## Contexte / besoin métier

L'association **DWFA (Drinking Water For All)** souhaite améliorer l'accès à l'eau potable dans les pays les plus en difficulté.

L'objectif de la mission est d'identifier **2 à 3 pays prioritaires** à partir de plusieurs indicateurs : accès à l'eau potable, mortalité liée à l'eau insalubre, population concernée et stabilité politique.

Les interventions envisagées couvrent trois domaines :

1. création de services d'accès à l'eau potable ;
2. modernisation des infrastructures existantes ;
3. consulting auprès des administrations et gouvernements.

## Outil

`Power BI`

## Démarche

### 1. Prétraitement

- import des fichiers sources ;
- conversion des nombres décimaux selon le format régional adapté ;
- nettoyage et renommage des colonnes ;
- fusion des tables sur `Country`, `Year` et `Granularity` ;
- jointure externe gauche afin de conserver la table Population ;
- conversion des données de population ;
- remplacement des régions manquantes par « Non classé » ;
- création des dimensions Pays, Année et Granularité ;
- mise en place du modèle relationnel.

### 2. Conception du dashboard

La conception passe par :

- un **blueprint** ;
- un **mockup** ;
- plusieurs vues Power BI destinées à passer d'une lecture mondiale à une lecture plus ciblée.

Les vues couvrent notamment :

- la situation générale de l'accès à l'eau ;
- l'impact sanitaire de l'eau insalubre ;
- la stabilité politique ;
- l'identification des pays prioritaires ;
- l'analyse détaillée des pays candidats.

## Résultats et recommandation

Deux pays sont analysés en priorité : **Zambie** et **Bénin**.

### Création de nouveaux services
La **Zambie** est privilégiée car sa population est plus élevée et son accès de base à l'eau potable est plus faible.

### Modernisation des infrastructures
Le **Bénin** est retenu pour la modernisation : l'accès de base y est plus élevé, mais l'accès sécurisé reste à améliorer.

### Consulting institutionnel
Le **Bénin** est également retenu pour le consulting, en raison d'un taux de mortalité WASH plus élevé dans l'analyse présentée.

## Valeur métier

Le dashboard permet de transformer plusieurs indicateurs internationaux en un outil d'aide à la décision afin de prioriser les interventions selon le type de besoin.

## Limites et prochaines pistes

- documenter plus précisément la date de référence de chaque indicateur ;
- enrichir l'analyse avec les coûts d'intervention ;
- intégrer des indicateurs de faisabilité opérationnelle ;
- formaliser un score multicritère pour classer les pays.

## Compétences démontrées

`Power BI` `Power Query` `Modélisation` `DAX` `Dashboard` `Analyse multicritère` `Aide à la décision`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./09_presentation_acces_eau_potable.pdf)
- 📓 [Télécharger le dashboard](./09_acces_eau_potable.pbix)
