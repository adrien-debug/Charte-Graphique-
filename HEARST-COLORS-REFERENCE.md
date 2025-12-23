# 🎨 HEARST - Référence Couleurs Officielles

## Palette Principale

### Couleurs Brand HEARST

```css
/* Couleurs Officielles HEARST */
--hearst-black: #000000;   /* Noir - Fond principal (dark mode) */
--hearst-grey: #525866;    /* Gris - Texte secondaire */
--hearst-green: #00C00C;   /* Vert - Couleur d'accent principale */
--hearst-white: #FFFFFF;   /* Blanc - Texte principal (light mode) */
```

### Variantes Vert HEARST

```css
--accent-green-light: #00ff15;  /* Vert Clair - Hover states */
--accent-green-dark: #009909;   /* Vert Foncé - Active states */
```

---

## Mode Dark (Défaut)

### Backgrounds
```css
--bg-primary: #000000;      /* Fond principal - Noir pur */
--bg-secondary: #0a0a0a;    /* Fond secondaire - Noir légèrement plus clair */
--bg-tertiary: #151515;     /* Fond tertiaire - Inputs, cards */
--bg-hover: #1a1a1a;        /* Hover state */
--border-color: #2a2a2a;    /* Bordures */
```

### Textes
```css
--text-primary: #FFFFFF;    /* Texte principal - Blanc pur */
--text-secondary: #a0a0a0;  /* Texte secondaire - Gris clair */
--text-muted: #525866;      /* Texte discret - Gris HEARST */
```

### Accents
```css
--accent-primary: #00C00C;  /* Vert HEARST - Accent principal */
--accent-green: #00C00C;    /* Vert HEARST */
--accent-red: #ff3366;      /* Rouge - Erreurs, alertes */
--accent-orange: #ff9500;   /* Orange - Warnings */
--accent-blue: #0066ff;     /* Bleu - Info */
--accent-cyan: #00ccff;     /* Cyan - Secondaire */
```

### Ombres
```css
--shadow: 0 4px 12px rgba(0, 0, 0, 0.6);
--shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.8);
--shadow-green: 0 0 20px rgba(0, 192, 12, 0.3);  /* Glow vert HEARST */
```

---

## Mode Light

### Backgrounds
```css
--bg-primary: #FFFFFF;      /* Fond principal - Blanc pur */
--bg-secondary: #f5f5f5;    /* Fond secondaire - Gris très clair */
--bg-tertiary: #e8e8e8;     /* Fond tertiaire */
--bg-hover: #d0d0d0;        /* Hover state */
--border-color: #d0d0d0;    /* Bordures */
```

### Textes
```css
--text-primary: #000000;    /* Texte principal - Noir pur */
--text-secondary: #525866;  /* Texte secondaire - Gris HEARST */
--text-muted: #808080;      /* Texte discret */
```

### Ombres
```css
--shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
--shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.15);
```

---

## Utilisation des Couleurs

### Buttons

#### Primary Button (Vert HEARST)
```css
background: var(--hearst-green);  /* #00C00C */
color: var(--hearst-black);       /* #000000 */
border: 1px solid var(--hearst-green);
```

**Hover:**
```css
background: var(--accent-green-light);  /* #00ff15 */
box-shadow: var(--shadow-green);
```

#### Secondary Button
```css
background: var(--bg-tertiary);
color: var(--text-primary);
border: 1px solid var(--border-color);
```

**Hover:**
```css
border-color: var(--hearst-green);
box-shadow: var(--shadow-green);
```

### Badges

#### Success Badge (Vert HEARST)
```css
background: rgba(0, 192, 12, 0.2);  /* Vert HEARST avec transparence */
color: var(--hearst-green);
border: 1px solid var(--hearst-green);
```

#### Warning Badge
```css
background: rgba(255, 149, 0, 0.2);
color: var(--accent-orange);
border: 1px solid var(--accent-orange);
```

#### Error Badge
```css
background: rgba(255, 51, 102, 0.2);
color: var(--accent-red);
border: 1px solid var(--accent-red);
```

#### Info Badge
```css
background: rgba(0, 102, 255, 0.2);
color: var(--accent-blue);
border: 1px solid var(--accent-blue);
```

### Cards

#### Stats Card (Mining Operations)
```css
background: var(--bg-secondary);
border: 1px solid var(--border-color);
border-radius: 8px;
```

**Valeur positive (Vert HEARST):**
```css
color: var(--hearst-green);
```

**Container Online:**
```css
border: 2px solid var(--hearst-green);
```

**Container Warning:**
```css
border: 2px solid var(--accent-orange);
```

### Graphiques

#### Line Chart (Hashrate)
```css
borderColor: '#00C00C';              /* Vert HEARST */
backgroundColor: 'rgba(0, 192, 12, 0.2)';
```

#### Gauge (Efficiency)
```css
stroke: var(--hearst-green);         /* Vert HEARST */
```

#### Container Grid
```css
/* Online */
border: 2px solid var(--hearst-green);
color: var(--hearst-green);

/* Warning */
border: 2px solid var(--accent-orange);
color: var(--accent-orange);
```

---

## Gradients HEARST

### Gradient Vert Principal
```css
background: linear-gradient(135deg, var(--hearst-green), var(--accent-green-light));
/* #00C00C → #00ff15 */
```

### Gradient Header Title
```css
background: linear-gradient(135deg, var(--hearst-green), var(--accent-green-light));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
text-shadow: var(--shadow-green);
```

### Gradient Executive Dashboard
```css
/* Card 1 - Vert HEARST */
background: linear-gradient(135deg, var(--hearst-green), var(--accent-green-dark));
/* #00C00C → #009909 */
color: black;

/* Card 2 - Bleu */
background: linear-gradient(135deg, var(--accent-blue), var(--accent-cyan));
/* #0066ff → #00ccff */
color: white;
```

---

## Animations avec Couleurs HEARST

### Glow Effect
```css
@keyframes glow {
    0%, 100% {
        box-shadow: 0 0 5px var(--hearst-green), 0 0 10px var(--hearst-green);
    }
    50% {
        box-shadow: 0 0 20px var(--hearst-green), 0 0 30px var(--hearst-green), 0 0 40px var(--hearst-green);
    }
}
```

### Pulse Effect
```css
@keyframes hearstPulse {
    0%, 100% {
        box-shadow: 0 0 0 0 rgba(0, 192, 12, 0.7);
    }
    50% {
        box-shadow: 0 0 0 10px rgba(0, 192, 12, 0);
    }
}
```

### Neon Text
```css
@keyframes neonGlow {
    0%, 100% {
        text-shadow: 0 0 10px var(--hearst-green), 0 0 20px var(--hearst-green);
    }
    50% {
        text-shadow: 0 0 20px var(--hearst-green), 0 0 30px var(--hearst-green), 0 0 40px var(--hearst-green);
    }
}
```

---

## Exemples d'Application

### 1. Mining Operations Dashboard

**Titre:**
```css
color: var(--hearst-green);
font-weight: 700;
```

**Stats Cards:**
```css
/* Active Containers */
color: var(--hearst-green);  /* 56/58 */

/* Efficiency Optimal */
color: var(--hearst-green);  /* 68.2 J/TH */
```

**Container Grid (58 containers):**
```css
/* Online (96.5%) */
border: 2px solid var(--hearst-green);
background: var(--bg-secondary);

/* Warning (3.5%) */
border: 2px solid var(--accent-orange);
```

### 2. Bloomberg Terminal

**KPI Cards:**
```css
/* BTC Price */
color: var(--hearst-green);  /* $43,250 */

/* Total Hashrate */
color: var(--hearst-green);  /* 5.98 EH/s */

/* Revenue 24h */
color: var(--hearst-green);  /* $125K */
```

### 3. Hero Landing Page

**Titre Principal:**
```css
font-size: 56px;
color: var(--hearst-green);
font-weight: 700;
```

**Stats:**
```css
/* 5.98 EH/s, 17,864, 96.5% */
color: var(--hearst-green);
font-size: 36px;
font-weight: 700;
```

### 4. Pricing Table

**Plan Professional (Popular):**
```css
background: linear-gradient(135deg, var(--hearst-green), var(--accent-green-dark));
color: black;
box-shadow: var(--shadow-green);
transform: scale(1.05);
```

**Badge "POPULAR":**
```css
background: rgba(0, 0, 0, 0.3);
color: white;
```

---

## Contraste & Accessibilité

### Ratios de Contraste (WCAG AA)

#### Mode Dark
- **Blanc sur Noir** : 21:1 ✅ (AAA)
- **Vert HEARST sur Noir** : 7.2:1 ✅ (AA Large)
- **Gris sur Noir** : 4.8:1 ✅ (AA)

#### Mode Light
- **Noir sur Blanc** : 21:1 ✅ (AAA)
- **Vert HEARST sur Blanc** : 3.1:1 ⚠️ (AA Large uniquement)
- **Gris HEARST sur Blanc** : 6.5:1 ✅ (AA)

### Recommandations

1. **Texte principal** : Toujours utiliser `--text-primary` (blanc/noir)
2. **Vert HEARST** : Réserver pour accents, titres, stats importantes
3. **Gris HEARST** : Texte secondaire, labels, descriptions
4. **Bordures** : Utiliser `--border-color` pour subtilité

---

## Palette Complète (Hex)

```
HEARST BRAND
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
#000000  ████████  Noir HEARST
#525866  ████████  Gris HEARST
#00C00C  ████████  Vert HEARST (Principal)
#FFFFFF  ████████  Blanc HEARST

VARIANTES VERT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
#00ff15  ████████  Vert Clair (Hover)
#009909  ████████  Vert Foncé (Active)

ACCENTS SECONDAIRES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
#ff3366  ████████  Rouge (Error)
#ff9500  ████████  Orange (Warning)
#0066ff  ████████  Bleu (Info)
#00ccff  ████████  Cyan (Secondaire)
#8866ff  ████████  Violet (Optionnel)

BACKGROUNDS (Dark Mode)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
#000000  ████████  Primary
#0a0a0a  ████████  Secondary
#151515  ████████  Tertiary
#1a1a1a  ████████  Hover
#2a2a2a  ████████  Border

TEXTS (Dark Mode)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
#FFFFFF  ████████  Primary
#a0a0a0  ████████  Secondary
#525866  ████████  Muted (Gris HEARST)
#707070  ████████  Disabled
```

---

## Export pour Design Tools

### Figma
```json
{
  "hearst-black": "#000000",
  "hearst-grey": "#525866",
  "hearst-green": "#00C00C",
  "hearst-white": "#FFFFFF",
  "accent-green-light": "#00ff15",
  "accent-green-dark": "#009909"
}
```

### Sketch
```swift
// HEARST Colors
let hearstBlack = UIColor(hex: "000000")
let hearstGrey = UIColor(hex: "525866")
let hearstGreen = UIColor(hex: "00C00C")
let hearstWhite = UIColor(hex: "FFFFFF")
```

### Tailwind Config
```js
module.exports = {
  theme: {
    extend: {
      colors: {
        'hearst-black': '#000000',
        'hearst-grey': '#525866',
        'hearst-green': '#00C00C',
        'hearst-white': '#FFFFFF',
        'hearst-green-light': '#00ff15',
        'hearst-green-dark': '#009909',
      }
    }
  }
}
```

---

## Utilisation Recommandée

### DO ✅
- Utiliser **Vert HEARST** (#00C00C) comme couleur d'accent principale
- Utiliser **Noir** (#000000) comme fond en mode dark
- Utiliser **Blanc** (#FFFFFF) comme texte principal en mode dark
- Utiliser **Gris HEARST** (#525866) pour textes secondaires
- Ajouter glow/shadow vert pour éléments interactifs

### DON'T ❌
- Ne pas utiliser d'autres nuances de vert
- Ne pas mélanger trop de couleurs d'accent
- Ne pas utiliser vert HEARST sur fond blanc (contraste insuffisant)
- Ne pas oublier les états hover/active
- Ne pas ignorer le mode light

---

**HEARST Brand Colors - Version 1.0**  
Décembre 2024

