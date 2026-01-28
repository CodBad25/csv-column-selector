# Sélecteurs CSV - Notes de projet

*Dernière mise à jour : 29 janvier 2026*

## Déploiement

- **URL en ligne** : https://codbad25.github.io/csv-column-selector/
- **Repo GitHub** : https://github.com/CodBad25/csv-column-selector
- **Hébergement** : GitHub Pages (branche main)

## Description

Application web de sélection et traitement de colonnes CSV. Traitement 100% côté client (pas de serveur).

## Fichiers actuels

| Fichier | Description | Lignes |
|---------|-------------|--------|
| `csv-column-selector.html` | Version basique | ~1 732 |
| `csv-column-selector-improved.html` | Version améliorée (architecture modulaire) | ~1 732 |
| `csv-column-selector-advanced.html` | Version complète (recommandée) | ~2 426 |
| `*-backup.html` | Sauvegardes (à supprimer si Git) | - |

## Stack technique

- **HTML5 / CSS / JavaScript** (vanilla, pas de framework)
- **Tailwind CSS v3** (CDN)
- **PapaParse v5.4.1** (CDN) - parsing CSV

## Fonctionnalités (version avancée)

- Upload drag & drop
- Sélection/désélection de colonnes
- Détection automatique du délimiteur
- Détection des types de données (email, téléphone, URL, date, nombre)
- Détection d'anomalies (encodage, caractères invalides)
- Nettoyage des données encodées
- Export : CSV, JSON, Excel, Rapport
- Dark mode
- Historique des actions
- Filtrage des colonnes par nom/type
- Raccourcis clavier (Ctrl+S, Ctrl+J, Ctrl+D, Ctrl+H)
- Préférences persistantes (localStorage)

## Limites configurées

- Taille max : 100 Mo
- Lignes max : 500 000
- Colonnes max : 500
- Prévisualisation : 50 lignes

---

## Améliorations à faire

### Organisation

- [ ] Initialiser un dépôt Git
- [ ] Supprimer les fichiers backup (redondants avec Git)
- [ ] Décider : garder uniquement la version avancée ?

### Fonctionnalités

- [ ] Fusion de plusieurs fichiers CSV
- [ ] Réordonner les colonnes par drag & drop
- [ ] Sauvegarder/charger des profils de sélection
- [ ] Recherche dans les données (pas seulement les colonnes)
- [ ] Prévisualisation du fichier de sortie avant téléchargement

### Performance

- [ ] Web Workers pour le parsing de très gros fichiers

### UX / Accessibilité

- [ ] Améliorer les contrastes en dark mode
- [ ] Ajouter le dark mode aux autres versions (ou les abandonner)

### Technique (si évolution majeure prévue)

- [ ] Migrer vers un projet structuré (Vite + modules ES)
- [ ] Séparer JS/CSS/HTML en fichiers distincts

---

## Notes

- Version recommandée pour utilisation : `csv-column-selector-advanced.html`
- Pas de dépendances npm, pas de build nécessaire
- Ouvrir directement le fichier HTML dans un navigateur
