# Analyse et Visualisation du Marché Immobilier avec Power BI

Un rapport Power BI interactif dédié à l'analyse et la visualisation du marché immobilier. Il permet d'explorer les prix, les volumes d'annonces, la répartition géographique et les tendances temporelles à travers quatre pages thématiques.

---

## Aperçu du rapport

| Info | Détail |
|---|---|
| **Outil** | Microsoft Power BI (Cloud) |
| **Version Power BI** | 2.153.777.0 (release 2026.04) |
| **Format fichier** | `.pbix` (version 1.28) |
| **Nombre de pages** | 4 |
| **Compression données** | XPress9 |

---

## Structure du rapport

### Page 1 — Vue Globale du Marché

Vue d'ensemble synthétique du marché immobilier.

**Indicateurs clés (KPI cards) :**
- Prix total agrégé
- Nombre total d'annonces
- Prix moyen

**Visualisations :**
- Graphique en barres — Prix moyen par ville (`city` × `Prix_Moyen`)
- Histogramme — Distribution des annonces par tranche de prix (`price (compartiments)` × `Total Annonces`)
- Graphique en anneau (donut) — Répartition luxury vs non-luxury (`is_luxury` × `Total Annonces`)
- Treemap — Volume d'annonces par ville (`city` × `Total Annonces`)

**Filtres interactifs (slicers) :**
- Ville (`city`)
- Surface (`surface`)
- Prix (`price`)

---

### Page 2 — Analyse des Prix

Analyse approfondie de la structure et de la distribution des prix.

**Indicateurs clés (KPI cards) :**
- Prix total
- Prix moyen
- Prix moyen au m²

**Visualisations :**
- Histogramme groupé — Nombre d'annonces par tranche de prix (`price (compartiments)` × `Total Annonces`)
- Graphique en barres — Prix moyen au m² par ville (`city` × `Prix Moyen m2`)
- Treemap — Croisement catégorie de surface / statut luxury (`is_luxury` × `Total Annonces` × `surface_category`)

**Filtres interactifs (slicers) :**
- Ville (`city`)
- Statut luxury (`is_luxury`)

---

### Page 3 — Analyse Géographique

Exploration cartographique et géographique du marché.

**Indicateurs clés (KPI cards) :**
- Prix moyen
- Total annonces

**Visualisations :**
- Carte interactive — Bulles géolocalisées par ville avec superposition de plusieurs métriques : prix total, prix moyen, statut luxury, prix moyen au m², nombre d'annonces
- Graphique en barres — Prix moyen au m² par ville
- Treemap — Répartition du volume d'annonces par ville

**Filtres interactifs (slicers) :**
- Statut luxury (`is_luxury`)
- Catégorie de surface (`surface_category`)

---

### Page 4 — Analyse des Tendances

Suivi de l'évolution temporelle du marché.

**Visualisations :**
- Courbe — Évolution du nombre d'annonces dans le temps (`loaded_at`)
- Courbe — Évolution du prix moyen dans le temps (`Prix_Moyen` × `loaded_at`)
- Graphique en aire — Volume d'annonces cumulé (`Total Annonces` × `loaded_at`)

**Filtres interactifs (slicers) :**
- Ville (`city`)
- Statut luxury (`is_luxury`)

---

## Modèle de données

Les champs identifiés dans le modèle de données sont :

| Champ | Description |
|---|---|
| `city` | Ville du bien immobilier |
| `price` | Prix du bien |
| `surface` | Surface du bien (m²) |
| `surface_category` | Catégorie de surface (petite / moyenne / grande) |
| `is_luxury` | Indicateur bien de luxe (booléen) |
| `loaded_at` | Date/heure de chargement de l'annonce |
| `Prix_Moyen` | Mesure — Prix moyen calculé |
| `Prix Total` | Mesure — Somme des prix |
| `Prix Moyen m2` | Mesure — Prix moyen au mètre carré |
| `Avg_Price_m2` | Mesure — Prix moyen au m² (variante) |
| `Total Annonces` | Mesure — Nombre total d'annonces |

---

## Prérequis

- **Microsoft Power BI Desktop** (version ≥ 2026.04) ou accès à **Power BI Service** (cloud)
- Droits d'accès à la source de données d'origine pour actualiser les données

---

## Utilisation

1. Ouvrir le fichier `.pbix` dans Power BI Desktop ou le publier sur Power BI Service.
2. Naviguer entre les quatre pages via les onglets en bas de l'écran.
3. Utiliser les slicers (filtres) présents sur chaque page pour affiner l'analyse par ville, surface, gamme de prix ou segment luxury.
4. Survoler les visuels pour accéder aux infobulles détaillées.
5. Pour actualiser les données, configurer les identifiants de connexion à la source dans **Accueil > Transformer les données > Paramètres de la source de données**.

---

## Auteur

Projet créé via Power BI Cloud — release **2026.04**.
