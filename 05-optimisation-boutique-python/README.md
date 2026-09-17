# Optimisation des données d’une boutique avec Python

## Contexte / besoin métier

La gestion des ventes et des stocks repose initialement sur des fichiers Excel et des traitements manuels, ce qui rend l’analyse complexe, chronophage et sujette aux erreurs. L’objectif est de passer à une analyse structurée, automatisée et fiable afin d’améliorer la qualité des données, le pilotage des stocks et l’analyse des performances commerciales.

## Données et outils

Trois sources sont consolidées : **ERP** (produits, prix, coûts, stocks), **LIAISON** (`product_id` ↔ `id_web`) et **WEB** (SKU, ventes, attributs produits).

Outils : `Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Plotly Express`

## Démarche

1. Contrôle de cohérence entre quantité et statut de stock.
2. Identification et exclusion des stocks et prix négatifs avec conservation des anomalies pour la traçabilité.
3. Comparaison du prix de vente HT au coût d’achat et exclusion des incohérences économiques.
4. Nettoyage des doublons SKU et des lignes sans identifiant exploitable.
5. Identification de **91 produits ERP** sans correspondance Web.
6. Consolidation via jointures internes pour le jeu final et jointures externes de contrôle pour identifier les non-correspondances.
7. Analyses statistiques sur les prix, les ventes, les stocks, les marges et les corrélations.

## Résultats clés

- Chiffre d’affaires total : **143 324,1 €**.
- **31 produits**, soit **4,35 % du catalogue**, sont détectés comme valeurs atypiques en prix ; après vérification, ils correspondent à des produits premium et sont conservés.
- **433 articles (61 % du catalogue)** sont nécessaires pour générer 80 % du chiffre d’affaires : la règle de Pareto 20/80 n’est donc pas vérifiée.
- Les durées d’écoulement observées pour certains surstocks vont d’environ **14 à plus de 30 mois**, avec une présence importante du champagne.
- Les taux de marge observés vont d’environ **29 % à 91 %** après nettoyage.
- Corrélation Stock ↔ Ventes : environ **0,45** ; Prix ↔ Ventes : environ **-0,52** ; Prix ↔ Stock : environ **-0,10**.

## Recommandations métier

- Automatiser les règles de contrôle sur les stocks, prix et statuts.
- Fiabiliser la liaison ERP–Web et l’unicité des SKU.
- Intégrer la saisonnalité dans la gestion des stocks.
- Suivre directement dans l’ERP la rotation de stock, le chiffre d’affaires et les marges.
- Utiliser l’ERP comme outil d’aide à la décision commerciale et logistique.

## Limites et prochaines pistes

Approfondir la saisonnalité, suivre les indicateurs sur plusieurs mois et automatiser les contrôles qualité dans le pipeline.

## Compétences démontrées

`Python` `Pandas` `Data cleaning` `Jointures` `Analyse statistique` `Corrélation` `Gestion des stocks` `Data quality`

## 📁Livrables

- 📊 [Consulter la présentation du projet](./05_presentation_optimisation_boutique.pdf)
- 📓 [Consulter le notebook Python](https://github.com/fodilkarima/fodilkarima/blob/main/05-optimisation-boutique-python/05_optimisation_boutique.ipynb)
