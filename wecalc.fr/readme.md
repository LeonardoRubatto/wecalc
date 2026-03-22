# wecalc.fr

> Portail de calculateurs gratuits — Finance, Éducation, Santé, Outils — formules officielles 2026  
> Domaine : https://wecalc.fr · Langue : fr · Catégorie : Portail · Accent : `#1E3A5F`

## Fonctionnalités

- Page d'accueil centrale du réseau wecalc.fr : agrège et référence 7 calculateurs spécialisés déployés sur sous-domaines dédiés
- Navigation par catégorie (Finance, Éducation, Santé, Outils) avec pills de filtre sticky et scroll-spy actif
- Bandeau de crédibilité (trust band) mettant en avant : absence de collecte de données, formules officielles sourcées, accès sans inscription
- Section SEO éditoriale full-width (350 mots) avec liens internes vers chaque sous-domaine, structurée pour le référencement naturel
- 4 blocs JSON-LD : `WebSite`, `ItemList` (7 entrées), `BreadcrumbList`, `FAQPage` (6 Q&A) — rich results Google activés
- Dark mode, responsive mobile-first, bulles interactives au curseur dans le hero et la section SEO, cookie banner RGPD

## Structure des fichiers

```
wecalc.fr/
├── index.html
├── confidentialite.html
├── 404.html
├── _headers
├── robots.txt
├── sitemap.xml
├── sitemap-index.xml
├── readme.md
├── favicon.png
├── favicon.ico
├── apple-touch-icon.png
├── og-image.png
└── assets/
    └── icons/
        ├── logo-fibo4.svg
        ├── bonus.svg
        ├── calc.svg
        ├── cookie.svg
        ├── egal.svg
        ├── error.svg
        ├── europe.svg
        ├── exam.svg
        ├── fast.svg
        ├── france.svg
        ├── monitor.svg
        ├── official.svg
        ├── op.svg
        ├── pdf.svg
        ├── share.svg
        ├── sources.svg
        ├── sources-dark.svg
        ├── success.svg
        ├── swap.svg
        ├── theme-dark.svg
        ├── theme-light.svg
        └── warning.svg
```

## Icônes SVG requises

Installer dans `/assets/icons/` : `logo-fibo4.svg`, `bonus.svg`, `calc.svg`, `cookie.svg`, `egal.svg`, `error.svg`, `europe.svg`, `exam.svg`, `fast.svg`, `france.svg`, `monitor.svg`, `official.svg`, `op.svg`, `pdf.svg`, `share.svg`, `sources.svg`, `sources-dark.svg`, `success.svg`, `swap.svg`, `theme-dark.svg`, `theme-light.svg`, `warning.svg`

## Sources des données

| Source | Organisme | URL | Vérifié le |
|--------|-----------|-----|------------|
| Taux TVA officiels | DGFiP | https://www.impots.gouv.fr | 2026-03-22 |
| Barèmes cotisations sociales | URSSAF | https://www.urssaf.fr | 2026-03-22 |
| Courbes de croissance pédiatriques | CDC | https://www.cdc.gov/growthcharts | 2026-03-22 |
| Coefficients baccalauréat 2026–2027 | Éducation nationale | https://www.education.gouv.fr | 2026-03-22 |
| Facteurs de conversion d'unités | BIPM / NIST | https://www.bipm.org · https://www.nist.gov | 2026-03-22 |
| Formules de marge | Bpifrance | https://bpifrance-creation.fr | 2026-03-22 |

## Déploiement

Push GitHub → Cloudflare Pages. Aucun outil de build. Le dossier `wecalc.fr/` est la racine du site.

```bash
git add .
git commit -m "update: [description courte]"
git push origin main
```

Cloudflare Pages détecte le push et redéploie automatiquement en ~30 secondes.

## Mise à jour des données

- Fréquence recommandée : annuelle (janvier) + ponctuelle lors de réformes fiscales ou pédagogiques
- Prochaine vérification : janvier 2027
- Fichiers à mettre à jour : `index.html` (texte éditorial, année dans le title), `sitemap.xml` (`lastmod`), `sitemap-index.xml` (`lastmod` de chaque entrée)

## Assets graphiques à produire manuellement

| Fichier | Dimensions | Contenu |
|---------|------------|---------|
| `favicon.png` | 32×32 px | Fond `#1E3A5F`, lettres **WC** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design — iOS arrondit automatiquement les coins |
| `og-image.png` | 1200×630 px | Fond `#F5F5F2`, card blanche centrée : logo wecalc.fr + "Calculateurs gratuits 2026 — Finance, Santé, Éducation" |

