# PROMPT DE RECONSTRUCTION — LANDING PAGE SAAS PREMIUM

---

## 0. RÔLE ET OBJECTIF

Tu es un développeur React senior spécialisé en design de précision.

Ta mission : reproduire fidèlement une landing page SaaS premium à partir d'images de référence et d'un Design System fourni.

Règle fondamentale : chaque décision visuelle doit être justifiée par l'image de référence correspondante. Tu ne dois rien inventer. Si une valeur n'est pas visible dans les images, utilise le Design System fourni ci-dessous.

---

## 1. STACK TECHNIQUE OBLIGATOIRE

```
Framework   : React + TypeScript + Vite
UI          : Tailwind CSS + shadcn/ui + Lucide React
Animations  : Framer Motion + GSAP
```

Le projet est en mode dark permanent. Toutes les classes Tailwind doivent fonctionner avec le mode `.dark` activé sur le `<html>`.

---

## 2. DESIGN SYSTEM — RÉFÉRENCE UNIQUE

**Toute valeur visuelle non lisible dans les images doit être extraite de ce système. Ne jamais inventer de valeur.**

### index.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  :root {
    --background: 210.0000 40.0000% 98.0392%;
    --foreground: 228.5714 84.0000% 4.9020%;
    --card: 0 0% 100%;
    --card-foreground: 228.5714 84.0000% 4.9020%;
    --popover: 0 0% 100%;
    --popover-foreground: 228.5714 84.0000% 4.9020%;
    --primary: 217.2193 91.2195% 59.8039%;
    --primary-foreground: 0 0% 100%;
    --secondary: 210.0000 40.0000% 96.0784%;
    --secondary-foreground: 222.2222 47.3684% 11.1765%;
    --muted: 210.0000 40.0000% 96.0784%;
    --muted-foreground: 215.3846 16.3180% 46.8627%;
    --accent: 210.0000 40.0000% 96.0784%;
    --accent-foreground: 222.2222 47.3684% 11.1765%;
    --destructive: 0 84.2365% 60.1961%;
    --destructive-foreground: 210.0000 40.0000% 98.0392%;
    --border: 214.2857 31.8182% 91.3725%;
    --input: 214.2857 31.8182% 91.3725%;
    --ring: 217.2193 91.2195% 59.8039%;
    --chart-1: 217.2193 91.2195% 59.8039%;
    --chart-2: 270.7407 91.0112% 65.0980%;
    --chart-3: 160.1183 84.0796% 39.4118%;
    --chart-4: 37.6923 92.1260% 50.1961%;
    --chart-5: 0 84.2365% 60.1961%;
    --font-sans: Inter, sans-serif;
    --font-serif: Georgia, serif;
    --font-mono: JetBrains Mono, monospace;
    --radius: 0.75rem;
    --shadow-2xs: 0px 4px 10px 0px hsl(0 0% 0% / 0.05);
    --shadow-xs: 0px 4px 10px 0px hsl(0 0% 0% / 0.05);
    --shadow-sm: 0px 4px 10px 0px hsl(0 0% 0% / 0.10), 0px 1px 2px -1px hsl(0 0% 0% / 0.10);
    --shadow: 0px 4px 10px 0px hsl(0 0% 0% / 0.10), 0px 1px 2px -1px hsl(0 0% 0% / 0.10);
    --shadow-md: 0px 4px 10px 0px hsl(0 0% 0% / 0.10), 0px 2px 4px -1px hsl(0 0% 0% / 0.10);
    --shadow-lg: 0px 4px 10px 0px hsl(0 0% 0% / 0.10), 0px 4px 6px -1px hsl(0 0% 0% / 0.10);
    --shadow-xl: 0px 4px 10px 0px hsl(0 0% 0% / 0.10), 0px 8px 10px -1px hsl(0 0% 0% / 0.10);
    --shadow-2xl: 0px 4px 10px 0px hsl(0 0% 0% / 0.25);
    --tracking-normal: -0.01em;
    --spacing: 0.25rem;
  }

  .dark {
    --background: 225 66.6667% 2.3529%;
    --foreground: 210.0000 40.0000% 98.0392%;
    --card: 228 33.3333% 5.8824%;
    --card-foreground: 210.0000 40.0000% 98.0392%;
    --popover: 228 33.3333% 5.8824%;
    --popover-foreground: 210.0000 40.0000% 98.0392%;
    --primary: 217.2193 91.2195% 59.8039%;
    --primary-foreground: 0 0% 100%;
    --secondary: 220.9091 39.2857% 10.9804%;
    --secondary-foreground: 210.0000 40.0000% 98.0392%;
    --muted: 220.9091 39.2857% 10.9804%;
    --muted-foreground: 215.0000 20.2247% 65.0980%;
    --accent: 217.2414 32.5843% 17.4510%;
    --accent-foreground: 210.0000 40.0000% 98.0392%;
    --destructive: 0 62.8205% 30.5882%;
    --destructive-foreground: 210.0000 40.0000% 98.0392%;
    --border: 217.2414 32.5843% 17.4510%;
    --input: 217.2414 32.5843% 17.4510%;
    --ring: 217.2193 91.2195% 59.8039%;
    --chart-1: 217.2193 91.2195% 59.8039%;
    --chart-2: 270.7407 91.0112% 65.0980%;
    --chart-3: 142.0859 70.5628% 45.2941%;
    --chart-4: 45.3982 93.3884% 47.4510%;
    --chart-5: 330.3659 81.1881% 60.3922%;
    --font-sans: Inter, sans-serif;
    --font-serif: Georgia, serif;
    --font-mono: JetBrains Mono, monospace;
    --radius: 0.75rem;
    --shadow-2xs: 0px 10px 20px 2px hsl(0 0% 0% / 0.25);
    --shadow-xs: 0px 10px 20px 2px hsl(0 0% 0% / 0.25);
    --shadow-sm: 0px 10px 20px 2px hsl(0 0% 0% / 0.50), 0px 1px 2px 1px hsl(0 0% 0% / 0.50);
    --shadow: 0px 10px 20px 2px hsl(0 0% 0% / 0.50), 0px 1px 2px 1px hsl(0 0% 0% / 0.50);
    --shadow-md: 0px 10px 20px 2px hsl(0 0% 0% / 0.50), 0px 2px 4px 1px hsl(0 0% 0% / 0.50);
    --shadow-lg: 0px 10px 20px 2px hsl(0 0% 0% / 0.50), 0px 4px 6px 1px hsl(0 0% 0% / 0.50);
    --shadow-xl: 0px 10px 20px 2px hsl(0 0% 0% / 0.50), 0px 8px 10px 1px hsl(0 0% 0% / 0.50);
    --shadow-2xl: 0px 10px 20px 2px hsl(0 0% 0% / 1.25);
  }
}

@layer base {
  * {
    @apply border-border;
  }
  body {
    @apply bg-background text-foreground;
  }
}
```

### tailwind.config.ts

```ts
/** @type {import('tailwindcss').Config} */
module.exports = {
  darkMode: ["class"],
  theme: {
    extend: {
      colors: {
        border: "hsl(var(--border))",
        input: "hsl(var(--input))",
        ring: "hsl(var(--ring))",
        background: "hsl(var(--background))",
        foreground: "hsl(var(--foreground))",
        primary: {
          DEFAULT: "hsl(var(--primary))",
          foreground: "hsl(var(--primary-foreground))",
        },
        secondary: {
          DEFAULT: "hsl(var(--secondary))",
          foreground: "hsl(var(--secondary-foreground))",
        },
        destructive: {
          DEFAULT: "hsl(var(--destructive))",
          foreground: "hsl(var(--destructive-foreground))",
        },
        muted: {
          DEFAULT: "hsl(var(--muted))",
          foreground: "hsl(var(--muted-foreground))",
        },
        accent: {
          DEFAULT: "hsl(var(--accent))",
          foreground: "hsl(var(--accent-foreground))",
        },
        card: {
          DEFAULT: "hsl(var(--card))",
          foreground: "hsl(var(--card-foreground))",
        },
      },
      borderRadius: {
        xl: "calc(var(--radius) + 4px)",
        lg: "var(--radius)",
        md: "calc(var(--radius) - 2px)",
        sm: "calc(var(--radius) - 4px)",
      },
      fontFamily: {
        sans: ["var(--font-sans)"],
        serif: ["var(--font-serif)"],
        mono: ["var(--font-mono)"],
      },
    },
  },
}
```

---

## 3. RESSOURCES FOURNIES — RÔLE EXACT DE CHAQUE FICHIER

| Fichier | Rôle | Où l'utiliser |
|---|---|---|
| `image_total.png` | Vue complète de la landing page | Compréhension de la structure globale UNIQUEMENT — ne jamais reconstruire directement depuis cette image |
| `A1.png` | Référence exclusive Navbar | Section 1 uniquement |
| `A2.png` | Référence exclusive Hero | Section 2 uniquement |
| `A3.png` | Référence exclusive Features | Section 3 uniquement |
| `A4.png` | Référence exclusive Statistiques | Section 4 uniquement |
| `A5.png` | Référence exclusive Pricing | Section 5 uniquement |
| `A6.png` | Référence exclusive Testimonials | Section 6 uniquement |
| `A7.png` | Référence exclusive FAQ | Section 7 uniquement |
| `A7b.png` | Référence exclusive "Where We Work" | Section 8 uniquement |
| `A8.png` | Référence exclusive CTA Final | Section 9 uniquement |
| `A9.png` | Référence exclusive Footer | Section 10 uniquement |
| `SVG1.svg` | Carte flottante Hero n°1 | Section 2 Hero UNIQUEMENT |
| `SVG2.svg` | Carte flottante Hero n°2 | Section 2 Hero UNIQUEMENT |
| `SVG3.svg` | Carte flottante Hero n°3 | Section 2 Hero UNIQUEMENT |
| `SVG4.svg` | Carte flottante Hero n°4 | Section 2 Hero UNIQUEMENT |
| `world-map.svg` | Fond décoratif discret | Arrière-plan de toutes les sections (faible opacité) |
| `hero_3d.webp` | Élément décoratif lumineux | Section 9 CTA Final + Section 10 Footer (newsletter) UNIQUEMENT |

---

## 4. RÈGLES ABSOLUES — NE JAMAIS VIOLER

```
⛔ NE JAMAIS :

1. Remplacer un composant UI (notification, graphique, jauge, messagerie, analytics)
   par une image statique, un screenshot, ou un SVG figé.

2. Utiliser hero_3d.webp dans le Hero (Section 2).
   Il est réservé au CTA Final et au Footer.

3. Reproduire le dashboard principal, la Terre 3D, ou les graphiques du dashboard.
   Ces éléments existent dans les images de référence uniquement pour comprendre
   la composition. Ils ne font pas partie du rendu final.

4. Placer SVG1, SVG2, SVG3, SVG4 dans la section Features.
   Ces fichiers sont EXCLUSIVEMENT destinés au Hero (Section 2).

5. Placer SVG1, SVG2, SVG3, SVG4 sans analyser A2 d'abord.
   Leur position, taille et orientation doivent être déduites de l'image A2.

6. Utiliser des dimensions arbitraires non visibles dans les images de référence.

7. Mélanger les références : chaque image Ax.png correspond à une section précise.
   Ne jamais utiliser A3.png pour reconstruire la Navbar, etc.
```

```
✅ TOUJOURS :

1. Analyser l'image de référence correspondante AVANT de coder chaque section.

2. Déduire les valeurs visuelles (dimensions, espacements, radius) depuis l'image.
   Si non lisibles, utiliser les tokens du Design System.

3. Coder tous les composants visuels internes en React pur (jamais en image statique).

4. Appliquer le world-map.svg en arrière-plan de toutes les sections
   avec une faible opacité et un léger glow, sans perturber la lisibilité.

5. Utiliser Framer Motion pour les animations d'interface (entrées, micro-interactions).
   Utiliser GSAP pour les effets avancés (parallax, halos, filaments lumineux).
```

---

## 5. ANALYSE GLOBALE OBLIGATOIRE (avant tout code)

Avant de commencer à coder, analyser l'ensemble des images pour extraire :

**Couleurs**
- Couleur de fond principale (dark navy profond)
- Couleurs d'accent (bleu électrique, violet)
- Couleurs de texte (blanc, blanc atténué, gris clair)

**Effets visuels à reproduire partout**
- Dégradés bleus/violets en arrière-plan
- Halos lumineux (glow radial diffus)
- Bordures lumineuses semi-transparentes
- Effets glassmorphism (blur + transparence)
- Transparences en couches
- Ombres douces sombres
- Coins fortement arrondis

**Typographie**
- Police principale : Inter
- Hiérarchie : H1 très grand et lourd > H2 > H3 > corps
- Tracking légèrement négatif sur les titres (–0.01em)

**Motion System global**
- Framer Motion : apparitions, entrées de sections, cartes, navbar, FAQ, statistiques
- GSAP : scroll animations, parallax, filaments lumineux, backgrounds animés, halos

---

## 6. SECTIONS À RECONSTRUIRE

Structure de la page (10 sections dans l'ordre) :

```
1. Navbar
2. Hero
3. Features
4. Numbers that Speak (Statistiques)
5. Pricing
6. Loved by Thousands (Testimonials)
7. Got Questions? (FAQ)
8. Where We Work
9. Ready to Get Started? (CTA Final)
10. Footer
```

---

### SECTION 1 — NAVBAR

**Référence image :** `A1.png`

**Composants à coder :**
- Logo
- Liens de navigation
- CTA "Try for free"

**Points critiques à analyser dans A1.png :**
- Hauteur exacte de la navbar
- Distance entre le haut de la page et la navbar (navbar flottante, non collée au bord)
- Rayon des coins (navbar avec coins arrondis distincts)
- Niveau de transparence et intensité du blur (glassmorphism)
- Épaisseur et couleur de la bordure
- Espacement entre les liens
- Taille et style du bouton CTA

**États à implémenter :**

État initial (page non scrollée) :
- Navbar flottante
- Semi-transparente
- Glassmorphism actif
- Coins arrondis visibles
- Bordure subtile
- Glow léger

État scrollé :
- Sticky en haut
- Plus opaque
- Plus lisible
- Même Design System conservé

**Animations :** Framer Motion — transition fluide entre état initial et état scrollé

---

### SECTION 2 — HERO

**Référence image :** `A2.png`

**Composants à coder :**
- Badge d'annonce (petite pilule en haut)
- Headline principal (H1 très grand, centré)
- Sous-titre
- CTA primaire (bouton filled bleu)
- CTA secondaire (bouton outline ou ghost)
- KPI Cards (en bas du hero)

**Points critiques à analyser dans A2.png :**
- Largeur maximale du contenu textuel
- Taille exacte du H1 et son poids
- Espacement entre les lignes du titre
- Position et taille des deux CTA
- Ambiance lumineuse générale (dégradés, halos bleus/violets)
- Filaments lumineux en arrière-plan
- Position des KPI Cards en bas

**Globe 3D — Présent dans A2 mais à NE PAS reproduire.**
Le globe sert à comprendre la composition et le positionnement des SVG flottants. Ne pas le coder.

**SVG flottants (SVG1, SVG2, SVG3, SVG4) :**

Ces 4 fichiers sont les cartes flottantes visibles autour du globe dans A2.

Avant de les placer, analyser A2 pour identifier précisément pour chaque SVG :
- Sa position (haut-gauche, haut-droite, bas-gauche, bas-droite)
- Sa taille approximative
- Son orientation / rotation éventuelle
- Sa distance par rapport au contenu principal
- Sa profondeur visuelle (z-index)

Ne jamais placer ces SVG arbitrairement. Le positionnement doit reproduire fidèlement la composition observée dans A2, même en l'absence du globe.

Animations des SVG flottants (après positionnement correct) :
- Floating animation (translation verticale douce, boucle)
- Parallaxe légère au scroll
- Glow animé (breathing effect)
- Micro-rotation subtile
- Mouvements indépendants entre les 4 composants

Librairies : Framer Motion + GSAP

**Conserver absolument :**
- Glow et halos bleus/violets
- Effets néon
- Rayons lumineux
- Lumières volumétriques
- Dégradés lumineux
- Ambiance futuriste profonde

**NE PAS reproduire :**
- Terre 3D
- Dashboard principal
- hero_3d.webp (réservé au CTA et Footer)

---

### SECTION 3 — FEATURES

**Référence image :** `A3.png`

**Composants à coder :**
- Heading de section + sous-titre
- 5 Feature Cards en grille asymétrique

**Disposition de la grille :**

```html
<div class="flex gap-[20px] flex-wrap content-center items-center justify-center">
  <div class="grow w-[40%] h-[175px]">Carte 1 — Notifications</div>
  <div class="grow w-[40%] h-[175px]">Carte 2 — Collaboration</div>
  <div class="grow w-[20%] h-[175px]">Carte 3 — Growth</div>
  <div class="grow w-[20%] h-[175px]">Carte 4 — Metrics</div>
  <div class="grow w-[20%] h-[175px]">Carte 5 — Analytics</div>
</div>
```

Les deux premières cartes sont plus larges. Les trois suivantes sont compactes. L'équilibre visuel doit être parfait.

**Points critiques à analyser dans A3.png :**
- Largeur et hauteur exactes des cartes
- Radius des coins
- Bordures lumineuses
- Effets de glow périphérique
- Espacement interne (padding)
- Hiérarchie texte dans chaque carte (icône > titre > description)
- Hover states

**Architecture interne de chaque carte (5 couches) :**
1. Structure principale (container)
2. Bordure lumineuse
3. Arrière-plan (dégradé sombre)
4. Contenu textuel (icône + titre + description)
5. Composant visuel interactif (mini-app React)

**Les 5 composants visuels internes :**

⛔ Aucun composant visuel interne ne doit être une image statique, un screenshot, ou un SVG figé.
⛔ Aucun des SVG fournis (SVG1–SVG4) n'est destiné à cette section.
✅ Chaque composant visuel doit être une mini-application React entièrement codée.

Carte 1 — Notifications :
- Système de notifications interactif
- Apparition progressive des notifications (Framer Motion)
- Légère translation verticale
- Pulsation discrète des indicateurs d'état

Carte 2 — Collaboration :
- Système de messagerie collaboratif interactif
- Animation subtile des messages entrants (Framer Motion)
- Effet de présence en temps réel
- Micro-interactions

Carte 3 — Growth :
- Graphique de courbe de croissance animé
- Animation de tracé de la courbe (GSAP ou Framer Motion)
- Remplissage progressif du graphique
- Animation des statistiques en overlay

Carte 4 — Metrics :
- Jauge métrique animée (gauge circulaire ou linéaire)
- Animation du compteur chiffré
- Rotation légère de l'indicateur
- Variation subtile de luminosité

Carte 5 — Analytics :
- Dashboard analytique miniature animé
- Animation progressive des barres
- Apparition des données par séquence
- Micro-mouvements continus en boucle

**world-map.svg :** intégré en arrière-plan de la section, faible opacité, léger glow, rôle purement décoratif.

---

### SECTION 4 — NUMBERS THAT SPEAK (Statistiques)

**Référence image :** `A4.png`

**Composants à coder :**
- Heading de section + sous-titre
- 3 blocs KPI

Valeurs visibles dans l'image : +10 000 · +350% · +99,9%

**Points critiques à analyser dans A4.png :**
- Taille des chiffres (très grands, weight élevé)
- Contraste chiffre / fond
- Alignement des 3 blocs
- Largeur de chaque bloc
- Rythme visuel et espacements
- Glow éventuel sur les chiffres
- Hiérarchie : chiffre > description

**world-map.svg :** arrière-plan discret de la section.

---

### SECTION 5 — PRICING

**Référence image :** `A5.png`

**Composants à coder :**
- Heading de section + sous-titre
- Toggle Annual / Monthly (visible dans l'image)
- 3 cartes de plan : Starter ($29) / Growth ($79, featured) / Enterprise ($199)

**Points critiques à analyser dans A5.png :**
- Différence visuelle entre le plan featured (Growth) et les deux autres
- Badge "Popular" sur le plan central
- Bordure lumineuse distincte sur le plan featured
- Glow accentué sur le plan featured
- Hiérarchie des prix (nom > prix > features > CTA)
- Style des boutons CTA différenciés
- Espacement vertical interne des cartes

**world-map.svg :** arrière-plan discret de la section.

---

### SECTION 6 — LOVED BY THOUSANDS (Testimonials)

**Référence image :** `A6.png`

**Composants à coder :**
- Heading de section + sous-titre
- Grille de cartes de témoignages (au moins 3 visibles)

Chaque carte :
- Avatar rond
- Étoiles de notation
- Citation
- Nom + fonction

**Points critiques à analyser dans A6.png :**
- Disposition de la grille (nombre de colonnes, alignement)
- Taille des avatars
- Espacement avatar / contenu
- Style des citations (guillemets, police)
- Hiérarchie texte dans la carte
- Bordures et transparences
- Glow et ombres
- Équilibre visuel général

**world-map.svg :** arrière-plan discret de la section.

---

### SECTION 7 — GOT QUESTIONS? (FAQ)

**Référence image :** `A7.png`

**Composants à coder :**
- Heading de section + sous-titre
- Barre de recherche (visible dans l'image)
- Pills / filtres par catégorie (Pricing · Features · Support · autres)
- Accordéon de 4 à 5 questions

**Points critiques à analyser dans A7.png :**
- Style de l'accordéon (fond, bordure, radius)
- Animation d'ouverture/fermeture (Framer Motion AnimatePresence)
- Taille des zones cliquables
- Hiérarchie question / réponse
- Transitions fluides
- Espacements entre les items

**world-map.svg :** arrière-plan discret de la section.

---

### SECTION 8 — WHERE WE WORK

**Référence image :** `A7b.png`

⚠️ Cette section est absente du prompt original mais visible dans l'image totale. Elle doit être implémentée entre la FAQ et le CTA Final.

**Composants à coder :**
- Heading de section + sous-titre
- Carte du monde animée avec réseau de connexions lumineuses (points + lignes)
- Indicateurs de présence mondiale

**Points critiques à analyser dans A7b.png :**
- Taille et position de la carte du monde dans la section
- Style des points de connexion (glow, couleur, taille)
- Style des lignes de connexion (animation, opacité)
- Ambiance lumineuse générale

**Note :** Le `world-map.svg` peut être utilisé ici comme base visuelle principale (contrairement aux autres sections où il est discret).

---

### SECTION 9 — READY TO GET STARTED? (CTA Final)

**Référence image :** `A8.png`

**Composants à coder :**
- Heading centré
- Sous-titre
- CTA primaire
- CTA secondaire
- Fond avec carte du monde et réseau visuel
- Halos lumineux intenses

**Points critiques à analyser dans A8.png :**
- Positionnement et largeur du bloc de contenu
- Système de deux boutons (primaire + secondaire)
- Glow bleu intense en arrière-plan
- Dégradés bleus profonds
- Halos lumineux
- world-map.svg intégré (usage visible, pas discret)

**hero_3d.webp :** utilisé ici comme élément décoratif lumineux. Utiliser une portion pertinente de l'image pour recréer l'effet observé dans A8.

---

### SECTION 10 — FOOTER

**Référence image :** `A9.png`

**Composants à coder :**

Colonne gauche :
- Logo
- Description courte
- Icônes de réseaux sociaux

Colonnes de navigation (4 colonnes) :
- Produit
- Entreprise
- Ressources
- Contact

Bloc newsletter :
- Champ email
- Bouton d'inscription
- Zone décorative lumineuse à droite

Bas de page :
- Mentions légales
- Copyright
- Liens de bas de page

**Points critiques à analyser dans A9.png :**
- Organisation et alignement des colonnes
- Hiérarchie des liens (titre de colonne > liens)
- Style du formulaire newsletter
- Style des icônes sociales
- Marges verticales
- Cohérence avec le Design System global

**hero_3d.webp :** utilisé pour la zone décorative lumineuse à droite du bloc newsletter. Utiliser une portion pertinente de l'image.

**world-map.svg :** arrière-plan discret de la section.

---

## 7. INSTRUCTIONS D'ANIMATION GLOBALES

### Framer Motion — utiliser pour :
- Apparitions au scroll de chaque section (fade in + légère translation Y)
- Entrées des cartes (stagger children)
- Navbar (transition état initial → état scrollé)
- Boutons CTA (hover scale + glow)
- FAQ accordéon (AnimatePresence height)
- Statistiques (count-up animation)
- Micro-interactions générales

### GSAP — utiliser pour :
- Scroll animations avancées
- Parallaxe sur le Hero et les halos
- Filaments lumineux animés
- Backgrounds animés (dégradés en mouvement)
- Effets de profondeur
- Séquences d'entrée premium du Hero

### Qualité attendue des animations :
- Fluides et performantes (GPU accelerated)
- Modernes et premium
- Optimisées desktop et mobile
- Pas d'animations brusques ni d'effets génériques
- Pas d'excès de mouvement

---

## 8. ARCHITECTURE DE FICHIERS RECOMMANDÉE

```
src/
├── components/
│   ├── layout/
│   │   ├── Navbar.tsx
│   │   └── Footer.tsx
│   ├── sections/
│   │   ├── Hero.tsx
│   │   ├── Features.tsx
│   │   ├── Statistics.tsx
│   │   ├── Pricing.tsx
│   │   ├── Testimonials.tsx
│   │   ├── FAQ.tsx
│   │   ├── WhereWeWork.tsx
│   │   └── CTAFinal.tsx
│   ├── ui/
│   │   └── (shadcn/ui components)
│   └── features/
│       ├── NotificationsCard.tsx
│       ├── CollaborationCard.tsx
│       ├── GrowthChart.tsx
│       ├── MetricsGauge.tsx
│       └── AnalyticsDashboard.tsx
├── assets/
│   ├── SVG1.svg
│   ├── SVG2.svg
│   ├── SVG3.svg
│   ├── SVG4.svg
│   ├── world-map.svg
│   └── hero_3d.webp
├── styles/
│   └── index.css
└── App.tsx
```

---

## 9. DOCUMENTATION OBLIGATOIRE

Créer dans `/.V0/` :

**plan.md** — Documenter :
- Architecture du projet
- Design System extrait des images
- Liste des composants et leur rôle
- Librairies utilisées et conventions
- Stratégie d'animation (Framer Motion vs GSAP)

**story.md** — Journaliser (mise à jour continue) :
- Création et modification de chaque composant
- Décisions visuelles prises avec justification depuis les images
- Évolutions du Design System
- Animations Framer Motion implémentées
- Effets GSAP implémentés
- Comportement de la navbar

---

## 10. NIVEAU DE QUALITÉ ATTENDU

Le résultat final doit ressembler à un produit SaaS IA premium moderne, niveau production.

- Fidélité visuelle maximale par rapport aux images de référence
- Cohérence parfaite du Design System sur toutes les sections
- Tous les composants visuels codés en React (jamais d'images statiques)
- Responsive complet (desktop en priorité, puis mobile)
- Composants réutilisables et bien structurés
- Animations premium et fluides
- Effets lumineux (glow, halos, néons) fidèlement reproduits
