# Projet_chlordecone
Etude de la chlordecone aux antilles françaises

![Python Version](https://img.shields.io/badge/python-3.9+-blue.svg)
![Status](https://img.shields.io/badge/Status-Projet_de_Recherche-orange.svg)
![Year](https://img.shields.io/badge/Année-2026-brightgreen)
## 🌍 Contexte et Enjeux
La **Chlordécone** est un pesticide qui a été utilisé dans les antilles françaises plus particulièrement en Guadeloupe et en Martinique, dans les années 1900 pour lutter contre le charançon du bananier. Pour autant ses propriétés physico-chimique lui ont permis de se stabiliser dans cet environnement d'où sa persistance aujourd'hui dans les sols, l'environnement, la faune et la flore. Ceci avec bien sûr une incidence sur la population antillaise qui est aujourd'hui victime de ce pertubateur endocrinien. Ce dernier pourrait selon des études impacter la fertilité, le développement psychomoteur ou encore la fonction thyroïdienne, ce qui en fait une **problématique de santé publique**.

C'est dans ce contexte, et dans l'optique de mettre en oeuvres des politiques adaptés que des prélèvements ont été réalisé sur différentes partielles agricoles afin d'**analyser sa teneur** et de **classer les denrées végétales selon leur sensibilité au transfert de chlordécone.**

---

## 🛠️ Méthodologie Data Science
1.  **Analyse Préliminaire** : Identification du typage des variables et étude des distributions.
2.  **Analyse Exploratoire (EDA)** : Nettoyage des données, gestion des valeurs aberrantes et recodage des modalités (normalisation des noms de communes via `unicodedata` et `re`).
3.  **Data Preparation** : 
    * Imputation des données manquantes via l'algorithme **KNN** (K-Nearest Neighbors).
    * Test de conformité aux seuils réglementaires.
4.  **Analyse Statistique Multivariée** :
    * **ACP** (Analyse en Composantes Principales) pour la réduction de dimension.
    * **CAH** (Classification Ascendante Hiérarchique) via `scipy.cluster` pour segmenter les niveaux de risques.

## 📍 Cartographie Interactive
L'aboutissement visuel de ce projet est une carte dynamique (Folium) qui superpose deux niveaux de lecture :
* **Couche Communale** : Coloration des fonds de communes selon le risque majoritaire.
* **Couche Ponctuelle** : Visualisation de chaque prélèvement réel avec infobulles détaillées (Taux, Type de sol, Préconisations).
  
## 📂 Structure du Dépôt
```text
├── BaseCLD2026/               # Données brutes (Prélèvements)
├── Documentation/                # Dictionnaire des données
├── carto/                   # fichiers (shp)
├── results/          # Cartes HTML et graphiques exportés
└── README.md           # Documentation

---
projet réalisé en 2026
