# 🌍 Analyse du risque de catastrophes naturelles en France

## Projet complet de Data Management et Machine Learning

## 1 - Présentation

Ce projet illustre l'ensemble du cycle de vie de la donnée à travers un cas d'usage inspiré du secteur de l'assurance.

L'objectif est de construire une chaîne complète de traitement des données, depuis leur collecte jusqu'à la création d'un Risk Score permettant d'**évaluer l'exposition des communes françaises aux catastrophes naturelles.**

Ce projet met en œuvre les principales étapes d'un projet de Data Management :

- Collecte et intégration de données
- Contrôle qualité
- Nettoyage et transformation
- Architecture Bronze / Silver / Gold
- Modélisation d'un Data Warehouse
- Gouvernance des données
- Analyse exploratoire
- Machine Learning
- Construction d'un indicateur métier (Risk Score)

### Problématique métier

Les compagnies d'assurance doivent évaluer le niveau d'exposition des territoires afin de :

- mieux comprendre les risques naturels ;
- adapter leur politique de souscription ;
- anticiper les coûts futurs des sinistres ;
- améliorer leur prise de décision.

**La problématique étudiée est la suivante :** 

*Quelles communes françaises sont les plus exposées aux catastrophes naturelles et peut-on prédire leur niveau d'exposition à partir de leurs caractéristiques démographiques et géographiques ?*


## 2 - Architecture du projet

<img width="405" height="505" alt="image" src="https://github.com/user-attachments/assets/c614ac4e-3e03-46f1-9bb1-7f59e9d0e584" />

                
## 3 - Organisation du projet

<img width="208" height="406" alt="image" src="https://github.com/user-attachments/assets/eaddae72-8167-4d2a-a017-2967c6192f38" />


## 4 - Sources de données

Le projet exploite plusieurs jeux de données Open Data :

- Informations sur les communes françaises (Population, Altitude, Superficie, Densité) : 
- Événements CatNat (GASPAR) : 
- Nombre d'arrêtés de catastrophe naturelle : 


## 5 - Technologies utilisées

- Data Engineering
- Python
- Pandas
- DuckDB
- Parquet
- Pydantic
- Data Management
- ETL / ELT
- Contrôle qualité
- Validation des données
- Architecture Bronze / Silver / Gold
- Data Warehouse
- Modèle en étoile
- Data Science
- Scikit-Learn
- SHAP
- Random Forest
- Gradient Boosting
- Régression Logistique
- Visualisation
- Matplotlib
- Power BI


## 6 - Pipeline de données

- Bronze
- Import des fichiers CSV / Excel
- Validation des schémas avec Pydantic
- Contrôle des types
- Stockage au format Parquet
- Contrôle qualité

Les données sont vérifiées selon plusieurs dimensions :
- Complétude
- Unicité
- Cohérence métier
- Intégrité référentielle
- Contrôle des formats
- Silver

Transformation des données :
- suppression des doublons ;
- gestion des valeurs manquantes ;
- harmonisation des formats ;
- enrichissement des données ;
- création des premiers indicateurs.
- Gold

Construction d'un Data Warehouse orienté décisionnel.
- Tables de dimensions
- Commune
- Temps
- Type de catastrophe
- Table de faits
- Événements CatNat


## 7 - Indicateurs métier

Le projet produit notamment les indicateurs suivants :

- nombre de catastrophes naturelles par commune ;
- CatNat pour 1 000 habitants ;
- CatNat par km² ;
- durée moyenne des événements ;
- niveau d'exposition des communes ;
- Risk Score.


# 8 - Machine Learning

Deux approches sont développées.

### Classification

Objectif :
*Prédire si une commune est fortement exposée aux catastrophes naturelles.*

Modèles comparés :
- Régression Logistique
- Random Forest
- Gradient Boosting

Évaluation :
- Accuracy
- Precision
- Recall
- F1-score
- ROC AUC

### Régression

Objectif :
*Prédire le nombre attendu de catastrophes naturelles.*

Évaluation :
- MAE
- RMSE
- R²


## 9 - Interprétabilité

Les modèles sont expliqués grâce à :
- Feature Importance
- Permutation Importance
- SHAP Values
- Partial Dependence Plot

# 10 - Risk Score

Un score de risque territorial est construit en combinant :

- l'historique des catastrophes naturelles ;
- la densité d'événements ;
- la population ;
- la densité de population ;
- la probabilité prédite par le modèle de Machine Learning.

Ce score permet de classer les communes selon plusieurs niveaux de risque.

## 11 - Gouvernance des données

Le projet comprend également :

- un dictionnaire de données ;
- les métadonnées ;
- les règles métier ;
- un rapport qualité ;
- la traçabilité des données (Data Lineage) ;
- des conventions de nommage.


## 12 - Pour lancer le projet

**Installer les dépendances :**
pip install -r requirements.txt

**Exécuter les pipelines :**
python bronze_pipeline.py
python silver_pipeline.py
python gold_pipeline.py

**Lancer les modèles :**
python train.py


## 13 - Perspectives d'amélioration
Automatisation avec Airflow ;
Transformation avec dbt ;
Conteneurisation Docker ;
Suivi des expérimentations avec MLflow ;
Déploiement d'une API avec FastAPI ;
Hébergement sur Azure ou AWS.

