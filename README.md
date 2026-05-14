# 🏠 README — Projet BI Immobilier Marocain avec Power BI

---

# 📌 Présentation du Projet

Ce projet consiste à développer une solution de **Business Intelligence (BI)** permettant l’analyse du marché immobilier marocain à partir des données extraites du site **Avito.ma**.

L’objectif principal est de transformer les données brutes en tableaux de bord interactifs et dynamiques afin d’aider à la compréhension des tendances du marché immobilier au Maroc.

Le projet exploite uniquement le schéma décisionnel :

```bash
bi_schema
```

Le schéma :

```bash
ml_schema
```

est réservé aux traitements **Machine Learning** et n’est pas utilisé dans cette partie.

---

# 🏗️ Architecture du Projet

Le Data Warehouse est organisé selon une architecture décisionnelle composée :

## 📂 Tables de Dimensions

### 🔹 dim_localisations

Contient :

- ville
- quartier

---

### 🔹 dim_temps

Contient :

- année

---

### 🔹 dim_caracteristiques

Contient :

- chambres
- étage
- salles de bain

---

## 📂 Table de Faits

### 🔹 fact_annonce

Contient :

- prix
- prix_m2
- surface
- lien annonce

Cette table centralise les mesures principales du système.

---

# 🛠️ Technologies Utilisées

| Outil | Utilisation |
|---|---|
| Power BI | Visualisation & Dashboards |
| Power Query | Nettoyage et transformation |
| DAX | Création des mesures et KPIs |
| PostgreSQL / SQL | Data Warehouse |
| Avito.ma Dataset | Source des données |

---

# 🔄 Étapes Réalisées

## 1️⃣ Connexion au Data Warehouse

- Connexion de Power BI à la base de données
- Importation des tables du schéma :

```bash
bi_schema
```

- Vérification des relations entre les tables

---

## 2️⃣ Préparation des Données avec Power Query

Les opérations suivantes ont été réalisées :

- Vérification des types de données
- Nettoyage des incohérences
- Filtrage des valeurs aberrantes
- Optimisation du modèle
- Création des colonnes calculées

### Exemple :

```DAX
prix_m2 = prix / surface
```

---

## 3️⃣ Création des Mesures DAX

Les principales mesures créées :

- Nombre total d’annonces
- Prix moyen
- Prix moyen par ville
- Prix moyen par m²
- Surface moyenne
- Taux de croissance
- Evolution temporelle

---

# 📊 Dashboards Réalisés

## 📈 Dashboard 1 — Vue Globale

### Contient :

- Nombre total d’annonces
- Prix moyen du marché
- Prix moyen/m²
- Répartition des annonces par ville
- Evolution des annonces dans le temps

### Visualisations utilisées :

- KPI Cards
- Line Chart
- Bar Chart
- Donut Chart

---

## 💰 Dashboard 2 — Analyse des Prix

### Contient :

- Distribution des prix
- Relation surface/prix
- Prix moyen par ville
- Prix total par quartier

### Visualisations utilisées :

- Scatter Plot
- Gauge
- Treemap
- Histogram

---

## 🌍 Dashboard 3 — Analyse Géographique

### Contient :

- Carte des prix par ville
- Classement des villes
- Analyse géographique du marché

### Visualisations utilisées :

- Map
- Table
- Bar Chart

---

## 📉 Dashboard 4 — Analyse des Tendances

### Contient :

- Evolution des prix
- Evolution des annonces
- Analyse temporelle

### Visualisations utilisées :

- Area Chart
- Line Chart
- Combo Chart

---

# 🎛️ Filtres Interactifs

Les dashboards utilisent des slicers dynamiques :

- Ville
- Quartier
- Surface
- Prix
- Année
- Nombre de chambres

Tous les graphiques sont interactifs et synchronisés.

---

# 📌 KPIs Principaux

| KPI | Description |
|---|---|
| Nombre_Annonces | Nombre total des annonces |
| Prix_Moyen | Prix moyen du marché |
| Prix_Moyen_m2 | Prix moyen par m² |
| Surface_Moyenne | Surface moyenne |
| Nombre_Villes | Nombre total des villes |

---

# 📈 Résultats du Projet

Cette solution permet :

- Une analyse dynamique du marché immobilier marocain
- L’identification des villes les plus chères
- Le suivi des tendances immobilières
- Une meilleure aide à la décision

---

# 🚀 Perspectives d’Amélioration

Possibilités futures :

- Intégration du Machine Learning
- Prédiction des prix immobiliers
- Analyse des tendances avancées
- Mise à jour automatique des données
- Déploiement Cloud

---

# 👩‍💻 Réalisé par

## Salma EL Yamani

Projet BI & Data Analytics — 2026.

---
