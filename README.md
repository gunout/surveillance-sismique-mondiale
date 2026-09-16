# 🌍 Surveillance Sismique Mondiale · Dashboard Temps Réel

Dashboard interactif de surveillance sismique mondiale en temps réel, alimenté par les données ouvertes de l'**USGS**. Visualisation cartographique multi-fonds, analyse statistique, alertes tsunami et système de diagnostic intégré.

[![Licence MIT](https://img.shields.io/badge/Licence-MIT-ED2939?style=for-the-badge)](LICENSE)
[![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=for-the-badge&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)](https://github.com/gunout)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://github.com/gunout/surveillance-sismique-mondiale)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://github.com/gunout/surveillance-sismique-mondiale)
[![Leaflet](https://img.shields.io/badge/Leaflet-1.9-199900?style=flat-square&logo=leaflet&logoColor=white)](https://leafletjs.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)](https://www.chartjs.org/)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-en_ligne-222?style=flat-square&logo=githubpages&logoColor=white)](https://gunout.github.io/surveillance-sismique-mondiale/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/gunout/surveillance-sismique-mondiale/pulls)
[![Open Data](https://img.shields.io/badge/Open_Data-USGS-ff6f00?style=flat-square)](https://earthquake.usgs.gov)
[![Temps réel](https://img.shields.io/badge/Temps_réel-60s-0055A4?style=flat-square)](https://earthquake.usgs.gov/earthquakes/feed/v1.0/)

---

## 📑 Sommaire

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Démo](#-démo)
- [Installation](#-installation)
- [Déploiement GitHub Pages](#-déploiement-github-pages)
- [Modules d'analyse](#-modules-danalyse)
- [Filtres et recherche](#-filtres-et-recherche)
- [Raccourcis clavier](#-raccourcis-clavier)
- [Architecture technique](#-architecture-technique)
- [Sources de données](#-sources-de-données)
- [Cartographie](#-cartographie)
- [Résolution de problèmes](#-résolution-de-problèmes)
- [Personnalisation](#-personnalisation)
- [Compatibilité](#-compatibilité)
- [Accessibilité](#-accessibilité)
- [Limitations](#-limitations)
- [Feuille de route](#-feuille-de-route)
- [Contribuer](#-contribuer)
- [Références](#-références)
- [Licence](#-licence)
- [Remerciements](#-remerciements)

---

## 🔎 Aperçu

Un fichier HTML unique, sans build ni dépendance npm, qui implémente un **dashboard interactif de surveillance sismique mondiale en temps réel**, alimenté par l'**API publique USGS GeoJSON**.

L'outil combine cartographie multi-fonds, analyse statistique multidimensionnelle, système d'alertes (tsunami, magnitude, USGS) et diagnostic de connexion automatique. Il est destiné aux analystes en géophysique, chercheurs en sciences de la Terre, étudiants en géologie, journalistes scientifiques et curieux.

L'application est **100 % côté client** : aucune donnée n'est envoyée à un serveur, aucun compte n'est requis, aucune clé API n'est nécessaire.

> ⚠️ **Outil académique et pédagogique** — Ne constitue pas une source officielle d'alerte sismique. En situation d'urgence, consultez les autorités officielles (USGS, EMSC, CSEM).

---

## ✨ Fonctionnalités

### 📊 6 modules d'analyse

1. **Carte Mondiale** — Visualisation interactive avec 3 modes d'affichage
2. **Séismes** — Liste détaillée des événements avec filtres
3. **Analyse** — 6 graphiques statistiques (magnitude, activité, régions, énergie...)
4. **Alertes** — Système d'alertes M ≥ 5.5, tsunami, niveau USGS
5. **Favoris** — Sauvegarde locale des séismes d'intérêt
6. **À propos** — Documentation intégrée

### 🗺️ Cartographie interactive

- **4 fonds de carte gratuits** : OpenStreetMap, Satellite (ESRI), Topographique (OpenTopoMap), Relief (ESRI)
- **3 modes d'affichage** : Marqueurs individuels, Clusters (regroupement), Heatmap (carte de chaleur)
- **Popups enrichis** : magnitude, profondeur, date, lien USGS
- **Plein écran** natif (plugin Leaflet Fullscreen)
- **Filtre CSS automatique** pour un rendu sombre élégant sur OSM

### 🔍 Comparaison et analyse

- **5 métriques clés** : nombre de séismes, magnitude max/moyenne, alertes tsunami, énergie totale libérée
- **6 graphiques** : distribution des magnitudes, activité quotidienne, top 10 régions, magnitude vs profondeur, énergie libérée par jour, répartition horaire (UTC)
- **Équivalent TNT** calculé pour chaque séisme

### 🚨 Alertes et notifications

- **Bannière d'urgence** pulsante pour M ≥ 7.0
- **Onglet Alertes** : M ≥ 5.5, tsunami, alertes USGS (vert/jaune/orange/rouge)
- **Alertes sonores** (Web Audio API) pour nouveaux séismes M ≥ 5.5
- **Toasts** empilables avec types (success, error, warning)
- **Badges de compteurs** sur les onglets

### 🎨 Interface

- **Design sobre** avec bandeau tricolore 🇫🇷
- **Thème clair/sombre** avec bascule automatique
- **Responsive** — mobile, tablette, desktop, ultra-wide
- **Drawer latéral** sur mobile (< 1000 px)
- **Bottom sheet** pour les modales sur mobile
- **Skeleton loaders** pendant le chargement

### 🛡️ Robustesse

- **4 sources USGS en cascade** : direct → AllOrigins → CorsProxy.io → ThingProxy
- **Fallback automatique** si une source échoue
- **Cache localStorage** : mode hors ligne opérationnel
- **Panneau de diagnostic** intégré en cas de problème
- **Détection en ligne/hors ligne** en temps réel
- **Timeout adaptatif** (30 s direct, 45 s proxy)

---

## 🚀 Démo

### 🌐 Application en ligne

👉 [**https://gunout.github.io/surveillance-sismique-mondiale/**](https://gunout.github.io/surveillance-sismique-mondiale/)

Aucune installation, aucune inscription. Ouvrez le lien dans un navigateur moderne.

---

## 📦 Installation

### Utilisation directe (recommandée)

git clone https://github.com/gunout/surveillance-sismique-mondiale.git
cd surveillance-sismique-mondiale
# Ouvrez index.html dans votre navigateur

Aucune dépendance, aucun `npm install`, aucun build.

### Serveur local (recommandé pour éviter les restrictions CORS)

Certains navigateurs bloquent les requêtes `fetch` depuis `file://`. Servez le fichier via HTTP :

# Python 3
python -m http.server 8000

# ou Node.js
npx serve .

# ou PHP
php -S localhost:8000

Puis ouvrez `http://localhost:8000/index.html`.

---

## 🌐 Déploiement GitHub Pages

L'application est **déjà déployée** à l'adresse :

**🔗 [https://gunout.github.io/surveillance-sismique-mondiale/](https://gunout.github.io/surveillance-sismique-mondiale/)**

### Déployer sur votre propre fork

1. **Forkez** le dépôt : [github.com/gunout/surveillance-sismique-mondiale](https://github.com/gunout/surveillance-sismique-mondiale)
2. Le fichier `index.html` doit être **à la racine** du dépôt
3. Allez dans **Settings → Pages**
4. Sous **Build and deployment** :
   - **Source** : `Deploy from a branch`
   - **Branch** : `main` / `(root)`
5. Cliquez sur **Save**
6. Attendez 1-2 minutes

Votre site sera accessible à : `https://<votre-compte>.github.io/<votre-repo>/`

### Ajouter un fichier `.nojekyll`

Pour éviter tout traitement Jekyll inutile et accélérer le déploiement :

touch .nojekyll
git add .nojekyll
git commit -m "chore: add .nojekyll"
git push

---

## 📋 Modules d'analyse

### 1. Carte Mondiale

- Carte Leaflet interactive centrée sur le monde
- 3 modes : Marqueurs, Clusters, Heatmap
- 4 fonds : OSM, Satellite, Topographique, Relief
- Sélecteur de fond (haut droite) et plein écran
- Popups détaillés avec lien vers la fiche USGS

### 2. Séismes

- Liste paginée (100 premiers résultats)
- Cartes individuelles par événement
- Badge de magnitude coloré
- Tags : Nouveau, Alerte tsunami, Alerte rouge/orange/jaune
- Actions rapides : Ajouter aux favoris, Voir sur USGS

### 3. Analyse

- **Distribution des magnitudes** (histogramme)
- **Activité quotidienne** (courbe)
- **Top 10 régions** (barres horizontales)
- **Magnitude vs Profondeur** (scatter plot)
- **Énergie libérée par jour** (barres)
- **Répartition horaire** (24h UTC)

### 4. Alertes

- Filtrage automatique : M ≥ 5.5, tsunami, niveau USGS
- Tri par sévérité (rouge > orange > jaune > vert)
- Bannière d'urgence pulsante pour M ≥ 7.0

### 5. Favoris

- Sauvegarde locale (localStorage)
- Persistance entre sessions
- Suppression individuelle ou globale

### 6. À propos

- Documentation intégrée
- Raccourcis clavier
- Formules utilisées
- Avertissement pédagogique

---

## 🔍 Filtres et recherche

| Filtre | Type | Description |
|--------|------|-------------|
| **Période** | Boutons 1h / 24h / 7j / 30j | Fenêtre temporelle |
| **Recherche** | Champ texte | Lieu, région, type |
| **Magnitude min.** | Slider 0 → 8 | Seuil minimal |
| **Profondeur max.** | Slider 10 → 700 km | Seuil maximal |
| **Région** | Menu déroulant | Sélection dynamique |
| **Tsunami uniquement** | Case à cocher | Séismes avec alerte tsunami |
| **Significatifs** | Case à cocher | M ≥ 4.5 |
| **Tri** | Case à cocher | Récent / Magnitude |

Les filtres actifs apparaissent sous forme de **chips** supprimables individuellement dans la barre dédiée.

---

## ⌨️ Raccourcis clavier

| Raccourci | Action |
|-----------|--------|
| <kbd>/</kbd> | Focus sur la recherche |
| <kbd>R</kbd> | Rafraîchir les données |
| <kbd>T</kbd> | Basculer thème clair/sombre |
| <kbd>1</kbd> – <kbd>6</kbd> | Naviguer entre les onglets |
| <kbd>F</kbd> | Ajouter/retirer un favori (modale ouverte) |
| <kbd>Échap</kbd> | Fermer la modale ou le drawer |

> Les raccourcis sont désactivés lorsque le focus est dans un champ de saisie.

---

## 🏗️ Architecture technique

### Stack

- **HTML5 / CSS3 / JavaScript ES2022** — aucune dépendance build
- **Leaflet.js** — cartographie interactive
- **Leaflet.markercluster** — regroupement de marqueurs
- **Leaflet.heat** — carte de chaleur
- **Leaflet.fullscreen** — mode plein écran
- **Chart.js** — graphiques statistiques
- **API USGS GeoJSON** — données sismiques

### Pipeline de données

USGS API (GeoJSON)
       │
       ▼
┌──────────────────┐
│ Fetch multi-     │  → Direct / AllOrigins / CorsProxy.io / ThingProxy
│ sources en       │
│ cascade          │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ Parsing +        │  → Normalisation, extraction région, calcul énergie
│ transformation   │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ Filtrage         │  → Magnitude, profondeur, région, texte, tsunami
└────────┬─────────┘
         ▼
┌──────────────────┐
│ Rendu            │  → Carte, liste, alertes, graphiques, métriques
└──────────────────┘

### Stockage local

| Clé `localStorage` | Contenu |
|--------------------|---------|
| `seismo_theme_v4` | Thème actif (dark / light) |
| `seismo_favorites_v4` | IDs des séismes favoris |
| `seismo_sound_v4` | État des alertes sonores |
| `seismo_cache_v4` | 500 derniers séismes (offline) |
| `seismo_range_v4` | Fenêtre temporelle préférée |
| `seismo_basemap_v4` | Fond de carte préféré |

### Synchronisation URL

L'état complet est encodé dans le query string :

?range=week&mag=4&depth=300&region=Japan&q=tokyo&tsunami=1&sig=1

Rechargez ou partagez le lien : l'état est restauré automatiquement.

---

## 📡 Sources de données

### API USGS

- **Base** : `https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/`
- **Documentation** : [earthquake.usgs.gov/earthquakes/feed/v1.0/](https://earthquake.usgs.gov/earthquakes/feed/v1.0/)
- **Format** : GeoJSON
- **Fréquence de mise à jour** : toutes les minutes
- **Licence** : domaine public (US Government)

### Flux utilisés

| Plage | Endpoint |
|-------|----------|
| 1 heure | `all_hour.geojson` |
| 24 heures | `all_day.geojson` |
| 7 jours | `all_week.geojson` |
| 30 jours | `all_month.geojson` |

### Fallback multi-sources

En cas de blocage CORS ou réseau, les proxies suivants sont tentés en cascade :

1. **Direct USGS** — accès natif
2. **AllOrigins** — `api.allorigins.win/raw`
3. **CorsProxy.io** — `corsproxy.io`
4. **ThingProxy** — `thingproxy.freeboard.io`

Un **panneau de diagnostic** s'affiche automatiquement si toutes les sources échouent.

---

## 🗺️ Cartographie

Tous les fonds de carte sont **gratuits et sans API key** :

| Fond | Fournisseur | Type | Zoom max | Attribution |
|------|-------------|------|----------|-------------|
| 🌍 **OpenStreetMap** | Communauté OSM | Raster | 19 | © OSM contributors |
| 🛰️ **Satellite** | ESRI World Imagery | Raster | 19 | © Esri, Maxar, Earthstar |
| 🗺️ **Topographique** | OpenTopoMap | Raster + relief | 17 | © OSM, SRTM, OpenTopoMap |
| 🏔️ **Relief** | ESRI World Terrain | Raster terrain | 13 | © Esri |

### Astuce thème sombre

Pour un rendu sombre sans dépendre de fournisseur externe, le fond OSM est **filtré en CSS** :

[data-theme="dark"] .leaflet-tile-pane.osm-dark-filter {
  filter: invert(1) hue-rotate(180deg) brightness(0.85) contrast(1.15) saturate(0.9);
}

Le filtre s'active/désactive automatiquement lors du basculement de thème.

---

## 🧪 Résolution de problèmes

### La carte affiche « API KEY REQUIRED »

Ce problème venait de **CartoDB** (résolu dans la version actuelle). Si vous voyez encore ce message, vérifiez que votre fichier utilise bien les URLs OSM/ESRI/OpenTopoMap et non `basemaps.cartocdn.com`.

### Le dashboard ne se connecte pas à l'USGS

**Causes possibles** :

1. **Fichier ouvert en `file://`** → Chrome/Edge bloquent les `fetch` cross-origin.
   - **Solution** : servez via `python -m http.server 8000`
2. **Bloqueur de pub** (uBlock, Privacy Badger, Brave Shields) bloque `earthquake.usgs.gov`.
   - **Solution** : désactivez temporairement les extensions
3. **Réseau d'entreprise restreint**.
   - **Solution** : utilisez un autre réseau ou un VPN
4. **Timeout** sur connexion lente.
   - **Solution** : le fallback automatique passe aux proxies

En cas d'échec, un **panneau de diagnostic** s'affiche avec :
- L'état de chaque source (✅ OK / ❌ KO)
- La latence en millisecondes
- Le nombre de séismes reçus
- Des conseils de résolution

### Test manuel rapide

Ouvrez dans un nouvel onglet :

👉 https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson

- ✅ Si vous voyez du JSON → l'USGS est accessible, le souci vient du fichier local ou d'une extension
- ❌ Si erreur → votre réseau bloque l'USGS

---

## ⚙️ Personnalisation

### Modifier la plage temporelle par défaut

Dans `state` :

timeRange: 'week'  // 'hour' | 'day' | 'week' | 'month'

### Modifier la fréquence de rafraîchissement

const REFRESH_INTERVAL = 60000;  // millisecondes

### Modifier le seuil d'alerte sonore

const newMajor = state.earthquakes.filter(e =>
  !previousIds.has(e.id) && e.mag >= 5.5  // Seuil modifiable
);

### Modifier le nombre de séismes affichés

const display = list.slice(0, 100);  // Nombre de cartes affichées

### Changer les couleurs

Modifiez les variables CSS dans `:root` :

:root {
  --blue: #0055A4;
  --deep-blue: #002395;
  --red: #EF4135;
  /* ... */
}

---

## 🌐 Compatibilité

| Navigateur | Version minimale |
|-----------|------------------|
| Chrome / Edge | 90+ |
| Firefox | 88+ |
| Safari | 14+ |
| Opera | 76+ |

**Non supporté** : Internet Explorer.

### Responsive

| Breakpoint | Adaptation |
|-----------|------------|
| > 1900 px | Layout ultra-wide (max 2000 px) |
| 1200 – 1900 px | Desktop standard |
| 1000 – 1200 px | Tablette paysage |
| 768 – 1000 px | Tablette portrait (sidebar en drawer) |
| 640 – 768 px | Mobile paysage |
| 480 – 640 px | Mobile portrait |
| 380 – 480 px | Petits mobiles |
| < 380 px | Très petits mobiles |

---

## ♿ Accessibilité

Ce projet vise la conformité **WCAG 2.1 niveau AA** :

- Structure sémantique HTML5 (`<header>`, `<main>`, `<nav>`, `<article>`, `<aside>`)
- Régions `aria-live` pour les mises à jour dynamiques
- Lien d'évitement « Aller au contenu principal »
- Tous les contrôles accessibles au clavier
- Contraste texte/fond ≥ 4.5:1
- Focus visibles et personnalisés (`:focus-visible`)
- Rôles ARIA (`tablist`, `tabpanel`, `dialog`, `alert`, `status`)
- Support `prefers-reduced-motion`
- Safe areas iPhone (`env(safe-area-inset-*)`)

Les retours et signalements de problèmes d'accessibilité sont bienvenus via les [issues](https://github.com/gunout/surveillance-sismique-mondiale/issues).

---

## ⚠️ Limitations

- **Dépendance à l'API USGS** : si toutes les sources échouent, seules les données en cache sont disponibles
- **Cache limité à 500 séismes** (quota localStorage)
- **Pas de service worker** : le mode offline fonctionne uniquement après un premier chargement
- **Pas d'index inversé** : la recherche est linéaire (O(n)), acceptable pour quelques milliers d'événements
- **Données en mémoire** : ~2 Mo pour une semaine complète
- **Pas de géolocalisation** : la carte s'ouvre centrée sur le monde
- **Pas de filtre par pays** : les régions sont extraites de la chaîne `place` de l'USGS

---

## 🗺️ Feuille de route

- [ ] Service worker pour un vrai mode offline (PWA)
- [ ] Notifications push pour les séismes majeurs
- [ ] Filtre par pays / continent
- [ ] Comparaison temporelle (semaine vs semaine précédente)
- [ ] Timeline interactive
- [ ] Export PDF avec graphiques
- [ ] Thème « haute visibilité » pour daltoniens
- [ ] Internationalisation (EN, ES, DE)
- [ ] Tests unitaires (Vitest) et E2E (Playwright)
- [ ] Intégration EMSC et Seismic Portal

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

1. Forkez le dépôt : [https://github.com/gunout/surveillance-sismique-mondiale/fork](https://github.com/gunout/surveillance-sismique-mondiale/fork)
2. Créez une branche : `git checkout -b feature/ma-fonctionnalite`
3. Committez : `git commit -m "feat: ajout de X"`
4. Poussez : `git push origin feature/ma-fonctionnalite`
5. Ouvrez une Pull Request : [https://github.com/gunout/surveillance-sismique-mondiale/pulls](https://github.com/gunout/surveillance-sismique-mondiale/pulls)

### Conventions de commit

Ce projet suit [Conventional Commits](https://www.conventionalcommits.org/fr/) :

- `feat:` nouvelle fonctionnalité
- `fix:` correction de bug
- `docs:` documentation
- `style:` formatage
- `refactor:` refactoring
- `perf:` performance
- `test:` tests
- `chore:` maintenance

### Signaler un bug

Ouvrez une issue sur [https://github.com/gunout/surveillance-sismique-mondiale/issues](https://github.com/gunout/surveillance-sismique-mondiale/issues) en précisant :
- Navigateur et version
- Étapes de reproduction
- Comportement attendu vs observé
- Captures d'écran si pertinent
- Sortie de la console (F12) si erreur JS

---

## 📚 Références

- **USGS** (2024), *Earthquake Hazards Program*, United States Geological Survey
- **EMSC** (2024), *Euro-Mediterranean Seismological Centre*
- **Seismic Portal** (2024), *European Plate Observing System*
- **Gutenberg & Richter** (1956), *Magnitude and Energy of Earthquakes*
- **OpenStreetMap** (2024), *Collaborative Mapping Project*
- **ESRI** (2024), *World Imagery and Terrain Services*
- **OpenTopoMap** (2024), *Topographic Map Layer*

---

## 📄 Licence

Ce projet est distribué sous licence **MIT** — voir le fichier [LICENSE](https://github.com/gunout/surveillance-sismique-mondiale/blob/main/LICENSE) pour plus de détails.

MIT License

Copyright (c) 2026 gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 🙏 Remerciements

- **USGS Earthquake Hazards Program** — production et diffusion des données sismiques mondiales
- **OpenStreetMap** — fond de carte collaboratif
- **ESRI** — imagerie satellite et terrain gratuites
- **OpenTopoMap** — fond topographique collaboratif
- **Leaflet** — bibliothèque cartographique open-source
- **Chart.js** — bibliothèque de graphiques
- **EMSC** et **Seismic Portal** — sources alternatives
  
---

📊 Outil pédagogique non officiel — Non affilié à l'USGS ni à l'État français

Données USGS (domaine public)

Fait pour la communauté sismologique open source.

---

