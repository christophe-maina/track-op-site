# Track-Op — Landing Page

> **Le planning, clair d'un coup d'œil.**
> Site officiel — by C-Ter · contact@c-ter.fr

---

## 📦 Contenu du pack

```
deploy/
├── index.html              ← La landing page (autonome, tout-en-un)
├── assets/
│   ├── ecosystem-real.jpg  ← Photo hero (écran + poste + mobile)
│   ├── carousel-1.png      ← Capture écran mural
│   ├── carousel-2.png      ← Capture poste de travail
│   ├── carousel-3.png      ← Capture app mobile
│   ├── favicon.svg         ← Favicon
│   └── track-op-logo.svg   ← Logo principal (pour réutilisation)
├── robots.txt              ← SEO
├── _redirects              ← Redirections (Netlify / Cloudflare Pages)
└── README.md               ← Ce fichier
```

**Tout est statique.** Pas de build, pas de framework, pas de dépendance serveur.
Les polices viennent de Google Fonts (chargées au runtime).

---

## 🚀 Déployer en ligne — 4 options

### Option 1 — Cloudflare Pages (recommandé)
Le plus simple si tu as déjà ton domaine `track-op.fr` chez IONOS :

1. Crée un dépôt GitHub privé, push le dossier `deploy/` dedans.
2. Va sur [pages.cloudflare.com](https://pages.cloudflare.com) → "Create a project" → "Connect to Git".
3. Sélectionne le repo. Build settings : **aucun** (le dossier est servi tel quel).
4. Une fois déployé, lie ton domaine `track-op.fr` dans Custom domains.

**Avantage** : CDN mondial, HTTPS auto, gratuit, ultra rapide.

### Option 2 — Netlify
1. [netlify.com](https://netlify.com) → "Add new site" → "Deploy manually".
2. Glisse-dépose le dossier `deploy/` dans la zone de drop.
3. Site en ligne immédiatement à une URL `*.netlify.app`.
4. Custom domain : ajoute `track-op.fr` dans les settings.

### Option 3 — Vercel
1. [vercel.com](https://vercel.com) → "Add new" → "Project".
2. Import depuis Git, ou drag & drop du dossier `deploy/`.
3. Framework Preset : **Other**. Output Directory : `.`
4. Custom domain dans les settings.

### Option 4 — GitHub Pages
1. Crée un repo GitHub (public ou Pro privé).
2. Push tout le contenu de `deploy/` à la racine.
3. Settings → Pages → Source : `main` branch, root.
4. Custom domain dans les settings.

---

## 🌐 Configuration DNS (pour track-op.fr / .com)

Une fois l'hébergement choisi, dans ton interface IONOS :

| Type  | Hôte | Valeur                                      |
|-------|------|---------------------------------------------|
| A     | @    | (IP fournie par l'hébergeur)                |
| CNAME | www  | `<ton-projet>.pages.dev` (ou équivalent)    |

**Délai de propagation** : 1 à 24 h selon les FAI.

---

## ✏️ Modifier le contenu

Le fichier `index.html` est **un seul fichier HTML autonome** (HTML + CSS + JS inline).

### Modifier un texte
Ouvre `index.html` dans un éditeur (VS Code, Sublime, Notepad++).
Cherche le texte à remplacer (Ctrl+F), modifie, sauvegarde, re-déploie.

### Remplacer une image
Remplace le fichier dans `assets/` en gardant **exactement le même nom**.
Tailles recommandées :
- `ecosystem-real.jpg` : 1920×1080 environ (16/9)
- `carousel-*.png` : carré (1:1), 1600×1600 minimum

### Changer l'email de contact
Cherche `contact@c-ter.fr` dans `index.html` (4 occurrences) et remplace toutes.

### Changer la couleur d'accent
Cherche `--orange:` dans le `<style>` :
```css
--orange:       #E26847;   /* terracotta vif sur dark */
```
Remplace par ta couleur (en hex).

---

## 🔒 Mentions légales — à compléter

Avant publication officielle, **ajoute une page de mentions légales** conforme LCEN :

1. Éditeur : C-Ter SARL, SIREN 851521948, 11 impasse Arthecia, 97351 Matoury
2. Directeur de publication : Christophe Maina
3. Hébergeur : (nom + adresse du service choisi ci-dessus)
4. Contact : contact@c-ter.fr
5. Marque Track-Op® déposée à l'INPI sous le N° 5260665

Le lien "Mentions légales" en footer pointe actuellement vers `#` — à remplacer par `mentions-legales.html` quand la page sera prête.

---

## 📊 Analytics (optionnel)

Pour ajouter Plausible (recommandé, RGPD-friendly, pas de cookie) :

```html
<!-- À placer dans <head> de index.html -->
<script defer data-domain="track-op.fr" src="https://plausible.io/js/script.js"></script>
```

Ou Google Analytics 4, ou Matomo, ou Cloudflare Web Analytics (gratuit avec Pages).

---

## ✅ Checklist avant mise en ligne

- [ ] Email `contact@c-ter.fr` actif et lu régulièrement
- [ ] Domaine `track-op.fr` redirigé vers l'hébergeur
- [ ] HTTPS activé (auto sur tous les hébergeurs cités)
- [ ] Mentions légales en place
- [ ] Politique de confidentialité (si tracking analytics)
- [ ] Test responsive : mobile, tablette, desktop
- [ ] Test navigateurs : Chrome, Safari, Firefox, Edge
- [ ] Performance : passe à [PageSpeed Insights](https://pagespeed.web.dev/) en vert
- [ ] SEO : vérifie le title, description et og:image
- [ ] Backup : garde une copie locale de tout le dossier `deploy/`

---

## 🆘 Support technique

Pour toute question sur le déploiement ou la modification du site :
- Email : contact@c-ter.fr
- Documentation : ce README

---

**Track-Op™** — le planning, clair d'un coup d'œil.
© 2026 C-Ter Studio · Matoury, Guyane Française · INPI N° 5260665
