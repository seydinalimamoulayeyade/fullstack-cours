# 🌐 Formation Développement Web Full Stack

> Série de 4 modules pour maîtriser le développement web front-end, du balisage HTML à l'application interactive en Vanilla JavaScript — avec un projet portfolio fil conducteur.

[![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat&logo=html5&logoColor=white)](cours-html.html)
[![CSS3](https://img.shields.io/badge/CSS3-264DE4?style=flat&logo=css3&logoColor=white)](cours-css.html)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)](cours-tailwind.html)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](cours-javascript-v2.html)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222?style=flat&logo=github&logoColor=white)](https://VOTRE-USERNAME.github.io/fullstack-cours)

---

## 📚 Modules

| # | Module | Durée | Niveau | Fichier |
|---|--------|-------|--------|---------|
| 01 | **HTML5** — Structure & contenu | 6 h | Débutant | [`cours-html.html`](cours-html.html) |
| 02 | **CSS3** — Mise en forme & Flexbox | 8 h | Débutant | [`cours-css.html`](cours-css.html) |
| 03 | **Tailwind CSS** — Utility-First Framework | 8 h | Intermédiaire | [`cours-tailwind.html`](cours-tailwind.html) |
| 04 | **JavaScript ES2024** — Vanilla JS & SPA | 10 h | Intermédiaire | [`cours-javascript-v2.html`](cours-javascript-v2.html) |

---

## 🗂️ Structure du projet

```
fullstack-cours/
├── index.html                   ← Page d'accueil (hub des modules)
├── cours-html.html              ← Module 01 — HTML5
├── cours-css.html               ← Module 02 — CSS3
├── cours-tailwind.html          ← Module 03 — Tailwind CSS
├── cours-javascript-v2.html     ← Module 04 — JavaScript
├── README.md                    ← Ce fichier
└── portfolio-spa/               ← Projet final SPA
    ├── index.html               ← Application SPA page unique
    ├── db.json                  ← Base de données json-server
    ├── package.json             ← Dépendances npm
    ├── js/
    │   └── portfolio.js         ← Logique JS complète
    └── images/                  ← Images des projets
```

---

## 🚀 Lancer le projet portfolio SPA

### Prérequis
- [Node.js](https://nodejs.org) (v16+)
- npm (inclus avec Node.js)

### Installation

```bash
# 1. Cloner le dépôt
git clone https://github.com/VOTRE-USERNAME/fullstack-cours.git
cd fullstack-cours/portfolio-spa

# 2. Installer json-server
npm install

# 3. Lancer le serveur API (port 3000)
npm start
# ou directement :
npx json-server --watch db.json --port 3000

# 4. Ouvrir index.html dans le navigateur
# (avec Live Server VS Code ou en double-cliquant)
```

### Endpoints API disponibles

| Méthode | Endpoint | Description |
|---------|----------|-------------|
| `GET` | `/projets` | Liste tous les projets |
| `GET` | `/projets/:id` | Détail d'un projet |
| `POST` | `/projets` | Créer un projet |
| `PUT` | `/projets/:id` | Remplacer un projet |
| `PATCH` | `/projets/:id` | Modifier partiellement |
| `DELETE` | `/projets/:id` | Supprimer un projet |

---

## 📋 Contenu des modules

### Module 01 — HTML5
- Présentation de HTML, historique, rôle dans la trinité Web
- Éléments, balises, attributs
- Structure d'une page HTML5
- Publier du texte, lister du contenu, lier des contenus
- Afficher une image, présenter un formulaire
- **Démo** : 3 pages statiques (`lister-projets.html`, `detailler-projet.html`, `ajouter-projet.html`)

### Module 02 — CSS3
- Sélecteurs (type, attribut, ID, classe, combinateurs)
- Propriétés, valeurs, règles, application du CSS
- Modèle de boîte (Box Model)
- Boîtes flexibles (Flexbox)
- **Démo** : Fichier `style.css` commun avec template header/nav/footer

### Module 03 — Tailwind CSS
- Présentation utility-first, mise en place CDN / npm
- Couleurs, typographie, arrière-plan, dimensionnement
- Bordures, espacement, modificateurs (`hover:`, `focus:`, `dark:`...)
- Flexbox Tailwind, responsive design (breakpoints)
- Personnalisation via `tailwind.config.js`
- **Démo** : Refactorisation complète du portfolio en Tailwind

### Module 04 — JavaScript ES2024
- Variables (`const`/`let`/`var`), types, opérateurs
- Entrées/sorties (`prompt`, `alert`, `console`)
- Structures de contrôle (conditions, boucles)
- Fonctions (classiques, arrow, callback, IIFE, closures)
- Événements et délégation d'événements
- Objets, Objet Array, Objet Document (DOM)
- Objet Form, validation
- Requêtes AJAX (Fetch API + async/await)
- **Démo** : SPA complète avec CRUD, json-server, DOM dynamique

---

## 🛠️ Technologies utilisées

| Technologie | Version | Usage |
|-------------|---------|-------|
| HTML5 | Latest | Structure des pages |
| CSS3 | Latest | Mise en forme |
| Tailwind CSS | v3 / CDN | Framework CSS |
| JavaScript | ES2024 | Logique applicative |
| json-server | ^1.0 | API REST factice |
| Google Fonts | — | Typographies des cours |

---

## 🌍 Déploiement

### GitHub Pages (recommandé)

```bash
# 1. Activer GitHub Pages
# → Settings → Pages → Source : main / root

# 2. URL générée automatiquement :
# https://VOTRE-USERNAME.github.io/fullstack-cours/
```

### Netlify

```bash
# Via CLI
npm install -g netlify-cli
netlify deploy --prod --dir .
```

### Vercel

```bash
# Via CLI
npm install -g vercel
vercel --prod
```

> ⚠️ **Note pour le portfolio SPA** : La partie `json-server` nécessite un serveur Node.js.
> Pour un déploiement 100% statique, remplacez les appels fetch par `localStorage`.
> Pour conserver json-server en ligne, utilisez [Render.com](https://render.com) (gratuit).

---

## 📁 Commits Git recommandés

```bash
# Structure de nommage conventionnelle
git commit -m "init: structure du dépôt"
git commit -m "feat: ajout cours HTML module 01"
git commit -m "feat: ajout cours CSS module 02"
git commit -m "feat: ajout cours Tailwind module 03"
git commit -m "feat: ajout cours JavaScript module 04"
git commit -m "feat: page d'accueil index.html"
git commit -m "feat(spa): prototype HTML portfolio SPA"
git commit -m "feat(spa): logique JS complète portfolio.js"
git commit -m "docs: README.md"
```

---

## 📖 Références

- [MDN Web Docs — HTML](https://developer.mozilla.org/fr/docs/Web/HTML)
- [MDN Web Docs — CSS](https://developer.mozilla.org/fr/docs/Web/CSS)
- [MDN Web Docs — JavaScript](https://developer.mozilla.org/fr/docs/Web/JavaScript)
- [Documentation Tailwind CSS](https://tailwindcss.com/docs)
- [json-server sur GitHub](https://github.com/typicode/json-server)
- [The Modern JavaScript Tutorial](https://javascript.info)
- [W3C Markup Validation Service](https://validator.w3.org)

---

## 📄 Licence

Ce projet est à usage pédagogique. Libre de réutilisation et adaptation.

---

*Formation Développement Web Full Stack · HTML · CSS · Tailwind · JavaScript · 2025*
