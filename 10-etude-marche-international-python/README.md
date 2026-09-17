# Étude de marché internationale — La Poule qui Chante

## Contexte / besoin métier

**La Poule qui Chante**, entreprise française spécialisée dans le poulet issu de l'agriculture biologique, souhaite identifier les marchés internationaux les plus intéressants pour son développement.

L'objectif est de sélectionner des pays présentant un potentiel favorable pour l'exportation à partir d'indicateurs alimentaires, économiques, commerciaux, sociodémographiques et technologiques.

## Sources

- **FAO**
- **Banque mondiale**

## Variables étudiées

Parmi les variables retenues :

- disponibilité en protéines ;
- importations ;
- exportations ;
- production ;
- population totale ;
- PIB par habitant ;
- taux d'urbanisation ;
- taux d'utilisation d'Internet ;
- score Doing Business / commerce.

Les variables sont sélectionnées selon leur pertinence, leur taux de valeurs manquantes et leur redondance. Les indicateurs Banque mondiale sont mobilisés selon une logique proche de **PESTEL**.

## Démarche

1. collecte et préparation des données ;
2. fusion des sources FAO et Banque mondiale ;
3. traitement des valeurs manquantes ;
4. standardisation des variables ;
5. analyse exploratoire par **ACP** ;
6. segmentation par **CAH** ;
7. segmentation par **K-means** ;
8. comparaison des méthodes ;
9. sélection finale des pays.

## Préparation des données

- remplacement des valeurs manquantes commerciales par 0 ;
- remplacement des valeurs manquantes socio-économiques par la médiane ;
- suppression progressive des variables peu pertinentes ou redondantes ;
- constitution d'un tableau final au niveau pays ;
- centrage-réduction avant ACP et clustering.

## Analyse en composantes principales

Les pays sont initialement décrits par **9 variables standardisées**.

Les axes **F1 et F2 expliquent ensemble 57,04 % de l'information**.

L'interprétation proposée est :

- **F1** : attractivité et ouverture du marché ;
- **F2** : volume productif et commercial.

Les pays situés vers la droite de F1 apparaissent comme plus attractifs, tandis qu'un F2 négatif peut correspondre à des marchés moins dominés par une forte production/exportation locale.

## Clustering

### CAH
Une segmentation en **4 clusters** est retenue.

Le cluster 2 regroupe les marchés considérés comme les plus attractifs dans l'analyse.

### K-means
La méthode du coude met en évidence une cassure autour de `k = 3`, mais **4 clusters** sont conservés afin d'obtenir une segmentation plus détaillée.

Le cluster 0 contient **27 pays** considérés comme les plus attractifs.

## Sélection finale

Le croisement des résultats CAH et K-means permet de retenir un groupe cohérent de marchés attractifs.

Une sélection complémentaire selon la proximité avec la France fait notamment ressortir :

- Allemagne
- Autriche
- Belgique
- Danemark
- Espagne
- Finlande
- Irlande
- Luxembourg
- Norvège
- Pays-Bas
- Royaume-Uni
- Suisse
- Suède

Des marchés secondaires plus petits, comme l'Islande et Malte, sont également identifiés.

## Valeur métier

La combinaison de l'ACP et de deux méthodes de clustering permet de transformer un ensemble complexe d'indicateurs internationaux en une segmentation exploitable pour orienter une stratégie d'exportation.

## Limites et prochaines pistes

- intégrer des données de prix, concurrence et coûts logistiques ;
- actualiser les données économiques ;
- ajouter des critères spécifiques au marché du bio ;
- construire un score de priorité final par pays ;
- réaliser une étude qualitative des marchés sélectionnés.

## Compétences démontrées

`Python` `ACP` `CAH` `K-means` `Standardisation` `Clustering` `Analyse de marché` `Segmentation`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./10_presentation_etude_marche_internationale.pdf)
- 📓 [Consulter le notebook K-means](./10_etude_marche_international_K_means.ipynb)
- 📓 [Consulter le notebook CAH](./10_etude_marche_internationale_CAH.ipynb)
