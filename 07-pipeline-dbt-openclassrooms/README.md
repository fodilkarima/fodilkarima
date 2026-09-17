# Pipeline de transformation avec dbt — Analyse sociodémographique

## Contexte / besoin métier

L’objectif est d’analyser l’évolution du profil sociodémographique des étudiants inscrits aux parcours Data d’OpenClassrooms sur quatre ans, afin d’identifier des tendances et d’alimenter les réflexions sur l’accessibilité et l’égalité des chances.

## Données et outils

Sources : données internes des étudiants de **2022 à 2025** et données démographiques publiques de l’**INSEE**.

Outils : `Snowflake` `dbt` `SQL` `Excel` `GitHub`

## Respect du RGPD

Les identifiants étudiants sont pseudonymisés dans la couche staging. Aucune donnée directement identifiable n’est utilisée et les analyses sont conduites sur des variables agrégées comme l’âge, le genre et la région.

## Architecture du pipeline

Le projet suit une logique **ELT** : collecte → chargement Snowflake → transformation dbt → analyse.

### Staging

Conversion de valeurs texte en numériques, suppression de caractères inutiles, normalisation des régions, gestion des valeurs manquantes et pseudonymisation.

### Intermediate

`UNPIVOT` des colonnes d’âge, regroupement des tranches d’âge, agrégation de la population et union des tables 2022 à 2025.

### Marts

Création de la table finale d’analyse permettant de comparer les étudiants à la population générale et de calculer les indicateurs. Des tests de qualité sont intégrés au pipeline.

## Résultats clés

- Effectifs : **1 696** étudiants en 2022, **1 150** en 2023, **850** en 2024 et **951** en 2025.
- Répartition globale indiquée : **1 057 femmes** et **2 344 hommes**.
- Forte représentation des **25–39 ans**.
- L’Île-de-France concentre le plus grand nombre d’étudiants en valeur absolue.
- Les proportions par genre restent relativement stables, avec une majorité masculine chaque année.
- La comparaison à la population met en évidence des différences de participation entre régions.

## Interprétation

Le support associe la présence importante des 25–39 ans à des parcours possibles de reconversion ou d’évolution professionnelle et relève un déséquilibre de genre persistant. Les causes avancées restent des hypothèses qui nécessiteraient des données complémentaires pour être confirmées.

## Recommandations

- Renforcer l’accès aux formations dans les régions les moins représentées.
- Encourager une plus grande diversité des profils.
- Poursuivre le suivi des indicateurs dans le temps.
- Adapter l’offre de formation aux évolutions observées.

## Limites et prochaines pistes

Approfondir les causes de la baisse des effectifs, ajouter des variables socio-économiques et automatiser le suivi via le pipeline dbt.

## Compétences démontrées

`Snowflake` `dbt` `SQL` `ELT` `Data pipeline` `RGPD` `Data quality` `Analyse sociodémographique`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./07_presentation_pipeline_dbt.pdf)
- 🧹 [Consulter les modèles Staging](https://github.com/fodilkarima/fodilkarima/tree/main/07-pipeline-dbt-openclassrooms/models/staging)
- ⚙️ [Consulter la configuration dbt](./dbt_project.yml)
