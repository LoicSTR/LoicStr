# Design — README GitHub personnel (Loïc Souêtre)

**Date :** 2026-05-13  
**Statut :** Approuvé

---

## Contexte

Refonte du README GitHub personnel (`LoicStr/LoicStr`). L'objectif est de se démarquer visuellement tout en restant lisible et professionnel, dans une optique de recherche de poste (CDI ou mission freelance).

---

## Décisions clés

| Critère | Choix retenu |
|---|---|
| Objectif | Trouver un poste / mission |
| Style visuel | Expressif / Signature |
| Langue | Français |
| Approche | Carte de visite — compact, centré, tout dit en peu d'espace |
| Disponibilité | Septembre (CDI ou freelance) |

---

## Structure du README

### 1. Header centré

- Nom en grand : `Loïc Souêtre.` (le point final en bleu via `<font color="#58a6ff">.</font>` — GitHub autorise l'attribut `color` sur `<font>`, pas les `style` inline)
- Sous-titre sur une ligne : `fullstack dev · sensibilité design · passé en communication`
- Badge de disponibilité immédiatement visible : `🟡 Disponible en septembre — CDI ou freelance`

### 2. Séparateur `<hr>`

Ligne fine (`---`) pour délimiter visuellement le header du corps.

### 3. Accroche courte

Deux lignes centrées, en italique ou couleur atténuée, qui résument la singularité du profil :

> Je viens de la communication. Ça se voit dans le code que j'écris,  
> les interfaces que je conçois et la façon dont j'explique mes choix.

Pas plus de 2 lignes. Pas de liste, pas de bullet points.

### 4. Stack — badges colorés

Section centrée, label `STACK` en uppercase petit.  
Badges en style pill (border-radius élevé), chacun avec une couleur propre à la techno :

- **Nuxt** → vert `#00DC82`
- **Next.js** → blanc/gris neutre
- **Svelte** → orange `#FF3E00`
- **TypeScript** → bleu `#3178C6`
- **Tailwind** → cyan `#06B6D4`

Implémentation : shields.io avec `style=flat-square` (léger, propre). Le style `for-the-badge` est plus imposant — à éviter ici pour conserver la compacité.  
Note : GitHub filtre les `style` CSS inline — les badges auront la forme shields.io standard (pas de "pill" CSS). C'est acceptable dans ce format.  
Pas de section "Outils" séparée — trop de badges noie le message.

### 5. Projets notables

2 projets maximum. Format : une ligne par projet, avec nom + stack + description courte.  
Pas de tableau HTML lourd — une liste ou un format simple suffit.

Projets à conserver du README existant :
- **ProjectAlpha** — Nuxt · Tailwind — Dashboard analytique temps réel
- **ui-components** — Vue · Storybook — Composants accessibles & documentés

### 6. Séparateur

Deuxième `---` avant les liens.

### 7. Liens de contact

Ligne centrée, séparés par des `·` :

```
LinkedIn · Portfolio · email (optionnel)
```

Badges shields.io ou liens Markdown simples — pas de tableau.

### 8. GitHub stats (optionnel)

Si inclus : compact, thème `github_dark`, `hide_border=true`.  
À placer en bas, après les liens. Ne pas mettre en avant — c'est un détail, pas l'argument principal.

---

## Ce qu'on supprime du README actuel

- Le tableau HTML à deux colonnes (Stack / Outils) — remplacé par les badges centrés
- La section "Outils" séparée (Vite, Vitest, Figma, Vercel, Git) — trop détaillé pour ce format
- Le tableau de projets avec 3 lignes — réduit à 2 projets maximum

---

## Contraintes techniques

- Le README doit fonctionner sans JavaScript (GitHub ne l'exécute pas)
- Pas de HTML complexe avec `<table>` imbriqués — préférer des balises HTML simples ou du Markdown pur
- Les images shields.io sont hébergées externement — elles peuvent être lentes à charger ; en limiter le nombre
- Le centrage se fait via `<div align="center">` (attribut HTML, pas CSS inline — GitHub filtre les styles)

---

## Périmètre exclu

- Animations (gif, typing effect) — alourdissent la page et peuvent paraître démodées
- Section "En ce moment / Currently learning" — inutile pour une cible recruteurs
- Compteur de visites — déconseillé (gadget, peu crédible)
- Section contributions heatmap — incluse via github-readme-stats si stats activées

---

## Résultat attendu

Un README d'une page, lisible en 10 secondes, qui communique :
1. Qui je suis (nom + identité)
2. Ma singularité (accroche)
3. Ma disponibilité (badge visible)
4. Ce que je sais faire (stack)
5. Ce que j'ai fait (2 projets)
6. Comment me contacter (liens)
