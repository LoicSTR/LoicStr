# README GitHub Personnel — Plan d'implémentation

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Réécrire `README.md` selon le design "Carte de visite" — compact, centré, expressif — orienté recherche de poste.

**Architecture:** Un seul fichier `README.md` réécrit de zéro. Pas de dépendances externes hormis shields.io (badges) et github-readme-stats (stats). Tout le HTML utilisé est compatible avec le filtre GitHub (pas de `style` inline, centrage via `align="center"`, couleur via `<font color>`).

**Tech Stack:** Markdown GitHub-flavored, HTML subset autorisé par GitHub, shields.io, github-readme-stats

---

## Fichiers

| Action | Fichier | Responsabilité |
|---|---|---|
| Modifier | `README.md` | L'unique fichier à réécrire |

---

### Task 1 : Header centré — nom, sous-titre, badge de disponibilité

**Files:**
- Modify: `README.md`

- [ ] **Step 1 : Remplacer le contenu de README.md par le header seul**

Remplacer l'intégralité du fichier `README.md` par :

```markdown
<h1 align="center">Loïc Souêtre<font color="#58a6ff">.</font></h1>

<p align="center">
  <strong>fullstack dev &nbsp;·&nbsp; sensibilité design &nbsp;·&nbsp; passé en communication</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/%F0%9F%9F%A1_Disponible-Septembre_2025-d2a922?style=flat-square" alt="Disponible en septembre" />
</p>
```

Notes :
- `<h1 align="center">` est plus fiable que `# heading` à l'intérieur d'un `<div>` — GitHub rend les headings Markdown dans les divs de façon inconsistante
- `<font color="#58a6ff">` est autorisé par GitHub (contrairement à `style` inline)
- L'emoji 🟡 est encodé en URL (`%F0%9F%9F%A1`) pour être compatible avec shields.io

- [ ] **Step 2 : Vérifier le rendu localement**

Ouvrir `README.md` dans un prévisualiseur Markdown (VS Code : `Cmd+Shift+V`) et vérifier :
- Le nom est grand et centré
- Le point final est visible (la couleur bleue peut ne pas s'afficher dans VS Code — c'est normal, GitHub la respecte)
- Le badge jaune `🟡 Disponible — Septembre 2025` est visible

- [ ] **Step 3 : Commit**

```bash
git add README.md
git commit -m "feat: add centered header with availability badge"
```

---

### Task 2 : Séparateur et accroche

**Files:**
- Modify: `README.md`

- [ ] **Step 1 : Ajouter le séparateur et l'accroche après le header**

Ajouter après le bloc `</div>` du header :

```markdown

---

<div align="center">

*Développeur fullstack avec un œil design et une plume.*  
*Je construis des interfaces que les utilisateurs comprennent — et que les équipes maintiennent.*

</div>
```

L'italique (`*...*`) donne un ton soigné sans être trop formel. Les deux lignes restent sur la même `<div>` centrée.

- [ ] **Step 2 : Vérifier**

Dans le prévisualiseur :
- Les deux lignes sont centrées et en italique
- Le séparateur `---` est une ligne fine au-dessus

- [ ] **Step 3 : Commit**

```bash
git add README.md
git commit -m "feat: add pitch accroche below header"
```

---

### Task 3 : Stack — badges colorés

**Files:**
- Modify: `README.md`

- [ ] **Step 1 : Ajouter la section stack après l'accroche**

Ajouter après le bloc accroche :

```markdown

---

<div align="center">

<sub>STACK</sub>

![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Svelte](https://img.shields.io/badge/Svelte-FF3E00?style=flat-square&logo=svelte&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

</div>
```

Notes :
- `<sub>STACK</sub>` donne un label petit et centré sans CSS
- Les couleurs correspondent aux couleurs officielles de chaque techno
- `style=flat-square` est le plus sobre — cohérent avec le format carte de visite

- [ ] **Step 2 : Vérifier**

Dans le prévisualiseur :
- Les 5 badges sont sur la même ligne (ou wrappés proprement si fenêtre étroite)
- Chaque badge a la bonne couleur de fond et le logo

- [ ] **Step 3 : Commit**

```bash
git add README.md
git commit -m "feat: add colored stack badges"
```

---

### Task 4 : Projets notables

**Files:**
- Modify: `README.md`

- [ ] **Step 1 : Ajouter la section projets après la stack**

Ajouter après le bloc stack :

```markdown

---

<div align="center"><sub>PROJETS NOTABLES</sub></div>

**[ProjectAlpha](https://github.com/loic/ProjectAlpha)** — Nuxt · Tailwind &nbsp;·&nbsp; Dashboard analytique temps réel pour équipes product

**[ui-components](https://github.com/loic/ui-components)** — Vue · Storybook &nbsp;·&nbsp; Bibliothèque de composants accessibles, documentée sous Storybook
```

Notes :
- Pas de tableau HTML — deux lignes simples, lisibles et maintenables
- `&nbsp;·&nbsp;` donne un séparateur visuel avec espacement sans CSS
- Les noms de projets sont des liens cliquables vers les vrais repos
- **Remplacer les URLs** par les vraies URLs des repos GitHub de Loïc

- [ ] **Step 2 : Remplacer les URLs placeholder**

Vérifier que `https://github.com/loic/ProjectAlpha` et `https://github.com/loic/ui-components` pointent vers les bons repos. Corriger si besoin.

- [ ] **Step 3 : Vérifier**

Dans le prévisualiseur :
- Les noms de projets sont en gras et cliquables
- La ligne est lisible en un coup d'œil (nom · stack · description)

- [ ] **Step 4 : Commit**

```bash
git add README.md
git commit -m "feat: add notable projects section"
```

---

### Task 5 : Liens de contact

**Files:**
- Modify: `README.md`

- [ ] **Step 1 : Ajouter les liens de contact en bas**

Ajouter après la section projets :

```markdown

---

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/loic)
&nbsp;
[![Portfolio](https://img.shields.io/badge/Portfolio-111827?style=flat-square&logo=vercel&logoColor=white)](https://loic.dev)

</div>
```

Notes :
- Badges shields.io avec logo pour LinkedIn et Portfolio — plus visuels qu'un lien texte brut
- `&nbsp;` entre les badges pour un espacement propre
- **Remplacer les URLs** par les vraies URLs LinkedIn et portfolio de Loïc

- [ ] **Step 2 : Remplacer les URLs placeholder**

- `https://linkedin.com/in/loic` → vraie URL LinkedIn
- `https://loic.dev` → vrai portfolio

- [ ] **Step 3 : Vérifier**

Dans le prévisualiseur :
- Les deux badges sont côte à côte, centrés
- Les logos LinkedIn et Vercel sont visibles

- [ ] **Step 4 : Commit**

```bash
git add README.md
git commit -m "feat: add contact links"
```

---

### Task 6 : GitHub Stats (optionnel)

**Files:**
- Modify: `README.md`

> Cette tâche est optionnelle. Les stats GitHub sont un "nice to have" — à inclure seulement si le profil GitHub est actif et représentatif.

- [ ] **Step 1 : Décider d'inclure ou non**

Si le profil a des contributions visibles → inclure.  
Si le profil est peu actif publiquement → sauter cette tâche.

- [ ] **Step 2 (si inclus) : Ajouter les stats après les liens**

Ajouter après le bloc contact :

```markdown

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=LoicStr&show_icons=true&theme=github_dark&hide_border=true&count_private=true&hide_title=true)

</div>
```

Notes :
- Remplacer `LoicStr` par le vrai username GitHub de Loïc
- `hide_title=true` retire le titre redondant "Loïc's GitHub Stats"
- `count_private=true` inclut les contributions privées
- `theme=github_dark` s'harmonise avec le fond sombre du header mockup

- [ ] **Step 3 : Vérifier**

Ouvrir l'URL suivante dans un navigateur pour confirmer que les stats se chargent correctement (remplacer `LoicStr` par le vrai username) :

```
https://github-readme-stats.vercel.app/api?username=LoicStr&show_icons=true&theme=github_dark&hide_border=true&count_private=true&hide_title=true
```

- [ ] **Step 4 : Commit**

```bash
git add README.md
git commit -m "feat: add github stats (optional)"
```

---

### Task 7 : Relecture finale et push

**Files:**
- Modify: `README.md` (corrections mineures si besoin)

- [ ] **Step 1 : Relire le README complet**

Lire `README.md` d'un seul tenant et vérifier :
- [ ] Le nom et le point bleu sont corrects
- [ ] Le badge de disponibilité est visible et à jour
- [ ] L'accroche tient en 2 lignes max
- [ ] Les 5 badges stack sont présents avec les bonnes couleurs
- [ ] Les 2 projets ont leurs vraies URLs
- [ ] Les liens LinkedIn et Portfolio ont leurs vraies URLs
- [ ] Pas de contenu résiduel de l'ancien README

- [ ] **Step 2 : Vérifier sur GitHub (rendu réel)**

Pusher sur la branche principale et vérifier le rendu sur `github.com/LoicStr/LoicStr` :

```bash
git push origin main
```

Ouvrir `https://github.com/LoicStr` et confirmer que le profil affiche le nouveau README.

- [ ] **Step 3 : Vérifications finales sur GitHub**

- [ ] Le centrage fonctionne (GitHub peut rendre différemment des prévisualiseurs locaux)
- [ ] La couleur du point final `<font color>` s'affiche en bleu
- [ ] Les badges shields.io se chargent (peuvent être lents la première fois)
- [ ] Les liens projets et contact sont cliquables et pointent aux bons endroits
