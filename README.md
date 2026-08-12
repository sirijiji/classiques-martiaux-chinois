# Classiques des arts martiaux chinois

Traductions en français de manuels classiques chinois des arts martiaux :
**taiji quan**, **xingyi**, **bagua**, armes traditionnelles (sabre, épée,
bâton, lance), traités théoriques et recueils d'exercices.

📖 Site publié : <https://sirijiji.github.io/classiques-martiaux-chinois/>

---

## À propos

Ce site publie des **traductions originales en français** de classiques chinois
des arts martiaux, réalisées directement à partir des **textes chinois tombés
dans le domaine public** (ouvrages du XIXe siècle et antérieurs). Chaque article
présente le texte chinois en regard de la traduction française, avec les sources
et des notes.

## Fonctionnalités

- Traductions originales à partir des sources chinoises (jamais de reprise d'autres traductions)
- Texte chinois et traduction française en vis-à-vis
- Sommaire automatique sur chaque article, recherche plein texte, flux RSS
- Mode clair / sombre, mise en page imprimable
- Thème éditorial personnalisé : photo historique de Guan Yu (domaine public), logo taijitu

## Pile technique

| Élément      | Choix                                    |
|--------------|------------------------------------------|
| Générateur   | [Hugo](https://gohugo.io) (extended)     |
| Thème        | [PaperMod](https://github.com/adityatelange/hugo-PaperMod) |
| Hébergement  | GitHub Pages (déploiement via GitHub Actions) |
| Contenu      | Markdown (un fichier par article)        |

## Structure du dépôt

```
content/
  posts/            articles (un fichier .md par traduction)
  apropos.md        page « À propos »
  archives.md       page Archives
  contact.md        page Contact
layouts/
  _partials/        surcharge de l'accueil (image d'en-tête)
  partials/         balises de partage social (og:image)
assets/css/extended/custom.css   habillage personnalisé
static/images/      images (domaine public)
themes/PaperMod/    thème (vendored)
```

## Ajouter un article

1. Créer un fichier `content/posts/<slug>.md` :

   ```markdown
   ---
   title: "Titre de la traduction"
   date: 2026-08-12
   description: "Résumé de l'article"
   categories: ["Taiji quan"]
   tags: ["tag1", "tag2"]
   ---

   Corps de l'article, texte chinois en regard.
   ```

2. Pousser sur `main` — le déploiement est automatique (~1 minute).

## Développement local

```bash
hugo server -D        # http://localhost:1313
hugo --minify         # génère le site statique dans public/
```

## Déploiement

Toute poussée sur `main` déclenche le workflow
`.github/workflows/hugo.yml` : construction Hugo + publication sur
GitHub Pages.

## Crédits & licence

- **Images** : portrait de Guan Yu (détail de *Guan Yu capture le général Pang
  De*, Shang Xi, dynastie Ming, XVe siècle — Musée du Palais, Pékin) et symbole
  du taiji, tous deux dans le **domaine public** (Wikimedia Commons).
- **Traductions** : travaux originaux réalisés pour ce site à partir de sources
  chinoises dans le domaine public.
- **Thème** : [PaperMod](https://github.com/adityatelange/hugo-PaperMod), licence MIT.
- Ce projet s'inspire de la forme des sites de traduction anglophones comme
  *Brennan Translation* (Paul Brennan) — référence incontournable pour les
  textes originaux. Les traductions ici publiées sont indépendantes.
