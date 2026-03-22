# wecalc.fr — Hub

| Champ | Valeur |
|-------|--------|
| Domaine | wecalc.fr |
| Langue | fr |
| Catégorie | hub |
| Couleur accent | `#1E3A5F` |

## Fonctionnalités

- Page d'accueil listant 7 calculateurs satellites sur sous-domaines
- Navigation par catégories (Finance, Éducation, Santé, Outils)
- Maillage interne complet vers tous les satellites
- Thème clair/sombre avec persistance localStorage
- Cookie banner RGPD-compliant
- SEO complet : 3 JSON-LD, canonical, og, twitter card

## Structure

```
wecalc-hub/
├── index.html
├── confidentialite.html
├── 404.html
├── _headers
├── robots.txt
├── sitemap.xml
├── sitemap-index.xml
├── readme.md
├── favicon.png               ← à produire (32×32)
├── apple-touch-icon.png      ← à produire (180×180)
├── og-image.png              ← à produire (1200×630)
└── assets/
    └── icons/
        ├── logo-fibo4.svg    ← fourni
        ├── theme-dark.svg
        └── theme-light.svg
```

## Icônes — Installation

Placer les fichiers SVG dans `/assets/icons/` :

```
logo-fibo4.svg    — fourni dans ce projet
theme-dark.svg    — lune (switch dark mode)
theme-light.svg   — soleil (switch light mode)
```

## Assets graphiques

| Fichier | Dimensions | Contenu |
|---------|-----------|---------|
| `favicon.png` | 32×32 px | Fond `#1E3A5F`, lettres **WC** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design que favicon — iOS ajoute automatiquement les coins arrondis |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée avec logo + "wecalc.fr" + "Calculateurs gratuits 2026" |

## Déploiement

Push GitHub → Cloudflare Pages. Aucun outil de build requis.
Build command : *(vide)*
Output directory : `/` (racine)

## Mise à jour des données

- Vérification annuelle recommandée (taux TVA, barèmes URSSAF, coefficients bac)
- Prochaine vérification : janvier 2027

