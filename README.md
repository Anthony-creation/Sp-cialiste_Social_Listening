# Base de données — Spécialistes du Social Listening

> Référentiel vivant des meilleurs profils du Social Listening (consultants, analystes, fondateurs, formateurs).  
> Fichier principal : **`blabla.xlsx`**

![Status](https://img.shields.io/badge/status-live-brightgreen)
![Format](https://img.shields.io/badge/format-XLSX-blue)
![MAJ](https://img.shields.io/badge/MAJ-continue-orange)

## 🎯 Objectif
Identifier rapidement des experts par **marché**, **langue**, **expertise**, **plateformes** et **disponibilité** (mission, speaking, advisory).

## 📁 Contenu du dépôt
- `blabla.xlsx` — base maîtresse (1 ligne = 1 spécialiste)
- `LICENSE` — licence du projet
- `CONTRIBUTING.md` — règles de contribution *(optionnel)*

## 🧱 Schéma des données (recommandé)
> Adapte si tes colonnes diffèrent, mais garde ces intentions.

| Colonne | Description |
|---|---|
| `name` | Nom complet |
| `country` | Pays / région |
| `languages` | Langues (fr, en, es…) |
| `expertise` | Mots-clés (crisis, insights, NLP…) |
| `industries` | Secteurs (FMCG, telco…) |
| `platforms_tools` | Outils (Brandwatch, Talkwalker, Sprinklr, Meltwater…) |
| `company_type` | Indépendant / Agence / Vendor / In-house |
| `availability` | Consulting, Speaking, Training, Advisory |
| `email_public` | Email (si public) |
| `website` | Site / portfolio |
| `x_handle` | Compte X |
| `linkedin_url` | Profil LinkedIn |
| `audience_size` | Ordre de grandeur audience |
| `influence_score` | Score perso (si utilisé) |
| `rates_note` | Note tarifs (optionnel) |
| `notes` | Contexte libre |
| `sources` | Lien(s) de vérification |
| `last_verified_at` | Dernière vérif (YYYY-MM-DD) |

## ⚡ Démarrage rapide

### Ouvrir / filtrer (Python + pandas)
```python
import pandas as pd
df = pd.read_excel("blabla.xlsx")

# Exemples de filtres
fr = df[df["languages"].str.contains("fr", case=False, na=False)]
brandwatch = df[df["platforms_tools"].str.contains("brandwatch", case=False, na=False)]
speaking = df[df["availability"].str.contains("speaking", case=False, na=False)]
