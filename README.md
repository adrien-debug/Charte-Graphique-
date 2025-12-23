# Design System IPO-Ready

> Système de design complet pour société de Bitcoin mining institutionnelle.  
> **Version:** 1.0.0  
> **Status:** Production  
> **Theme:** Dark-first

---

## 📐 Vue d'ensemble

Ce design system a été construit pour une **société de Bitcoin mining destinée à être cotée en bourse**. Il respecte des standards institutionnels stricts :

- ✅ **Thème sombre par défaut** (surface noire profonde #0B0D0E)
- ✅ **Accessibilité WCAG AAA** (ratios de contraste calculés)
- ✅ **Typographie financière** (Inter + IBM Plex Mono, tabular-nums)
- ✅ **Composants IPO-ready** (tableaux financiers, KPI, panels data)
- ✅ **Hero impact** (typographie massive avec contour, dégradés optionnels)
- ✅ **Tokens structurés** (JSON exploitable par dev/design/motion/3D)
- ✅ **Zero fantaisie** (stabilité, puissance, contrôle, fiabilité)

---

## 📦 Structure

```
/
├── design-tokens.json          # Tokens complets (couleurs, typo, grilles, motion, 3D)
├── ds.css                      # Variables CSS + composants
├── index.html                  # Hub Design System (navigation interactive)
├── preview-hero.html           # Preview interactif hero (style Qatar Bitcoin)
├── components-preview.html     # Galerie de tous les composants
└── README.md                   # Documentation (ce fichier)
```

---

## 🚀 Démarrage rapide

### 1. Ouvrir le hub principal

```bash
# Servir localement (exemple avec Python)
python3 -m http.server 8881

# Puis ouvrir dans le navigateur
open http://localhost:8881/
```

### 2. Intégrer dans un projet

```html
<!doctype html>
<html lang="fr">
<head>
  <link rel="stylesheet" href="ds.css" />
</head>
<body>
  <button class="ds-btn ds-btn--primary">Action primaire</button>
</body>
</html>
```

---

## 🎨 Couleurs

### Palette dark-first

| Token | Hex | Usage |
|-------|-----|-------|
| **Canvas** | `#0B0D0E` | Fond principal |
| **Surface 1** | `#121518` | Cards, panels |
| **Surface 2** | `#171B1F` | Headers, élévation |
| **White** | `#F6F7F8` | Texte principal |
| **Green 500** | `#18A957` | Accent sur fond sombre |
| **Green 800** | `#05512A` | Liens sur fond clair (WCAG AAA) |
| **Green 300** | `#6FE3A5` | Stats accent |

### Règles d'usage

#### ✅ **Autorisé**
- Texte principal: `#F6F7F8` sur `#0B0D0E` (ratio 18.17 — AAA)
- Liens sur fond sombre: `green-500` (#18A957)
- Liens sur fond clair: `green-800` (#05512A) **uniquement**
- CTA primaire: fond `green-700`, texte `white`
- Accents data/stats: `green-300` (#6FE3A5) sur fond sombre
- Dégradés: hero H1/H2 **uniquement** (optionnel)

#### ❌ **Interdit**
- Texte `green-500` sur fond clair (ratio 2.86 insuffisant)
- Dégradés décoratifs hors hero
- Saturation élevée hors tokens définis
- Ombres floues multiples (max 2 niveaux)
- Icônes décoratives non informatives

---

## 🔤 Typographie

### Familles

- **Sans-serif:** Inter (UI, titres, texte courant)
- **Monospace:** IBM Plex Mono (données financières, tableaux)

### Échelle

| Style | Taille | Poids | Usage |
|-------|--------|-------|-------|
| **Hero** | clamp(44px, 6.2vw, 88px) | 800 | Titre hero landing |
| **H1** | 40px | 700 | Titre principal |
| **H2** | 32px | 700 | Titre section |
| **H3** | 28px | 600 | Sous-titre |
| **Body** | 16px | 400 | Texte courant |
| **Data** | 13px | 400 (mono) | Tableaux financiers |
| **Label** | 12px | 600 | Headers, métadonnées |

### Règles

- **Chiffres:** police mono + `tabular-nums`
- **Titres:** tracking léger négatif (H1-H3)
- **UI labels:** uppercase + `letter-spacing: 0.06em`
- **Densité dashboard:** 13px/14px max, interlignage `snug`
- **Interdit:** italique pour données, corps < 12px en contexte IPO

---

## 🧩 Composants

### Buttons

```html
<button class="ds-btn ds-btn--primary">Action primaire</button>
<button class="ds-btn ds-btn--secondary">Action secondaire</button>
<button class="ds-btn ds-btn--primary" disabled>Disabled</button>
<button class="ds-btn ds-btn--pill">Pill variant →</button>
```

### Cards

```html
<div class="ds-card">
  <h3>Card Title</h3>
  <p>Contenu de la carte.</p>
</div>
```

### KPI / Stats

```html
<div class="ds-kpi">
  <div class="ds-kpi__label">Hashrate</div>
  <div class="ds-kpi__value">5.98 EH/s</div>
  <div class="ds-kpi__meta">MAJ 10:32 UTC</div>
</div>
```

### Tables financières

```html
<table class="ds-table">
  <thead>
    <tr>
      <th>Poste</th>
      <th class="is-num">USD</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>CAPEX – Mineurs</td>
      <td class="is-num">80,000,000</td>
    </tr>
  </tbody>
</table>
```

**Règles tableaux :**
- Libellés: `align-left`
- Valeurs numériques: `align-right` + `tabular-nums`
- Lignes alternées très faibles (white / offwhite)
- Gridlines fines

### Panels dark (monitoring)

```html
<div class="ds-panel-dark">
  <div class="ds-panel-dark__title">Panneau exploitation</div>
  <div class="ds-panel-dark__line">
    <div class="ds-panel-dark__key">Temp. entrée</div>
    <div class="ds-panel-dark__value">24.6°C</div>
  </div>
</div>
```

---

## 📐 Grilles

### Responsive

| Breakpoint | Colonnes | Gutter | Marges |
|------------|----------|--------|--------|
| **Desktop** (≥1200px) | 12 | 24px | 32px |
| **Tablet** (768-1199px) | 8 | 20px | 24px |
| **Mobile** (<768px) | 4 | 16px | 16px |

### Usage

```html
<div class="ds-container">
  <div class="ds-grid">
    <div style="grid-column: span 4;">Column 1</div>
    <div style="grid-column: span 4;">Column 2</div>
    <div style="grid-column: span 4;">Column 3</div>
  </div>
</div>
```

### Layouts spécialisés

- **Dashboard:** `.ds-dashboard` (grille 12 cols, gap 16px)
- **Rapports financiers:** `.ds-report` (5fr texte + 7fr data)
- **Slides investisseurs:** `.ds-slide` (16:9, padding 6%)

---

## 🎬 Hero System

### Typographie massive avec contour

**Option A — Contour plein (recommandé):**
```html
<h1 class="heroTitle">
  <span class="heroTitle__row">
    <span class="outlineA">Qatar Bitcoin</span>
  </span>
  <span class="heroTitle__row">
    <span class="outlineA gradClip gradGreenCyan">Strategic Reserve</span>
  </span>
</h1>
```

**Option B — Contour creux (impact tech):**
```html
<span class="outlineB">Strategic Reserve</span>
```

### Dégradés (optionnels, hero uniquement)

```html
<!-- Dégradé vert techno (ligne 2) -->
<span class="gradClip gradGreenCyan">Strategic Reserve</span>

<!-- Dégradé white→pink (ligne 1, optionnel) -->
<span class="gradClip gradWhiteRose">Qatar Bitcoin</span>
```

**⚠️ Règle stricte :** dégradés autorisés **uniquement** sur H1/H2 hero. Interdit ailleurs.

---

## ⚡ Motion

### Durées

| Token | Valeur | Usage |
|-------|--------|-------|
| `--ds-dur-fast` | 140ms | Hover, press |
| `--ds-dur-base` | 220ms | Transitions standard |
| `--ds-dur-slow` | 360ms | Modals, panels |

### Easing

- **Standard:** `cubic-bezier(0.2, 0.0, 0.0, 1.0)` (défaut)
- **Emphasized:** `cubic-bezier(0.2, 0.0, 0.0, 1.2)` (overshoot léger)

### Règles

- 1 propriété animée principale par interaction (`opacity` OU `transform`)
- Pas de stacking décoratif, bounce, glow
- Entrées UI: `opacity + translateY(6px)` max

---

## 🎨 3D & Rendering

### Matériaux PBR

| Material | Base Color | Metallic | Roughness | Usage |
|----------|------------|----------|-----------|-------|
| **Painted Metal Dark** | #1F2429 | 0.0 | 0.55 | Containers |
| **Anodized Aluminum** | #6B727A | 0.8 | 0.35 | Châssis |
| **Rubber** | #121518 | 0.0 | 0.90 | Joints |
| **Glass UI** | #F6F7F8 | 0.0 | 0.08 | Panels UI |
| **Emissive Green** | #18A957 | — | — | LEDs, indicateurs |

### Lighting (3-point)

- **Key:** 5600K, intensity 1.0
- **Fill:** 5600K, intensity 0.35
- **Rim:** 6500K, intensity 0.55
- **Ambient:** intensity 0.12

### Règles intégration UI dans 3D

#### ✅ **Autorisé**
- UI en panneau plan, angle ≤ 15° par rapport caméra
- Contraste texte ≥ 4.5:1 maintenu (scrim vidéo si nécessaire)
- Border hairline + elevation

#### ❌ **Interdit**
- Néons, bloom, aberration chromatique
- Dégradés décoratifs sur UI
- Texte vert sur fond clair

---

## 📹 Vidéo / Overlays

### Safe areas

- **Title safe:** 10% marges (x: 0.10, y: 0.10, w: 0.80, h: 0.80)
- **Action safe:** 5% marges (x: 0.05, y: 0.05, w: 0.90, h: 0.90)

### Scrim overlay

```css
background: rgba(11,13,14,0.72);  /* Scrim fort */
background: rgba(11,13,14,0.54);  /* Scrim léger */
border-top: 1px solid rgba(246,247,248,0.16);  /* Hairline */
```

### Lower thirds

- **Fond:** `rgba(11,13,14,0.72)`
- **Padding:** 24px (x), 16px (y)
- **Entry anim:** opacity + translateY(6px), 360ms
- **Exit anim:** opacity, 220ms

---

## 📤 Export

### Design Tokens (JSON)

```bash
design-tokens.json
```

Format conforme [Design Tokens Community Group](https://design-tokens.github.io/community-group/format/).

### CSS Variables

```bash
ds.css
```

Toutes les variables CSS prêtes à l'emploi.

### Composants HTML

```bash
components-preview.html  # Galerie complète
preview-hero.html        # Hero interactif
index.html               # Hub Design System
```

---

## 🔒 Versioning

- **Current:** `1.0.0-ipo-ready`
- **Status:** Production
- **Breaking changes:** Major version bump
- **Features:** Minor version bump
- **Fixes:** Patch version bump

---

## ✅ Checklist IPO

- [x] Accessibilité WCAG AAA (ratios calculés)
- [x] Thème sombre institutionnel
- [x] Typographie financière (tabular-nums)
- [x] Composants tableaux financiers
- [x] Hero impact (outline + dégradés optionnels)
- [x] Tokens structurés (JSON exploitable)
- [x] Motion contrôlé (pas de fantaisie)
- [x] 3D/PBR matériaux industriels
- [x] Documentation complète
- [x] Zéro branding "crypto casino"

---

## 📞 Support

Pour toute question ou contribution :

1. Consultez le **hub interactif** : `index.html`
2. Testez le **hero preview** : `preview-hero.html`
3. Explorez la **galerie composants** : `components-preview.html`

---

## 📜 Licence

Propriétaire — Bitcoin Mining Corporation IPO-Ready  
**Version:** 1.0.0  
**Date:** 2025






