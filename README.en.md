# Chinese Martial Arts Classics (in French)

French translations of classical Chinese martial arts manuals:
**taiji quan**, **xingyi**, **bagua**, traditional weapons (saber, sword,
staff, spear), theoretical treatises and exercise collections.

📖 Live site: <https://sirijiji.github.io/classiques-martiaux-chinois/>

---

## About

This site publishes **original French translations** of Chinese martial arts
classics, made directly from **public-domain Chinese source texts** (works from
the 19th century and earlier). Every article shows the Chinese text alongside
the French translation, with sources and notes.

## Features

- Original translations from Chinese sources (never derived from other translations)
- Chinese text and French translation side by side
- Automatic table of contents, full-text search, RSS feed
- Light / dark mode, print-friendly layout
- Custom editorial theme: historical Guan Yu portrait (public domain), taijitu logo

## Tech stack

| Element      | Choice                                   |
|--------------|------------------------------------------|
| Generator    | [Hugo](https://gohugo.io) (extended)     |
| Theme        | [PaperMod](https://github.com/adityatelange/hugo-PaperMod) |
| Hosting      | GitHub Pages (deployed via GitHub Actions) |
| Content      | Markdown (one file per article)          |

## Repository layout

```
content/
  posts/            articles (one .md file per translation)
  apropos.md        "About" page (French)
  archives.md       Archives page
  contact.md        Contact page
layouts/
  _partials/        homepage override (header image)
  partials/         social share tags (og:image)
assets/css/extended/custom.css   custom styling
static/images/      images (public domain)
themes/PaperMod/    theme (vendored)
```

## Adding an article

1. Create `content/posts/<slug>.md`:

   ```markdown
   ---
   title: "Translation title"
   date: 2026-08-12
   description: "Article summary"
   categories: ["Taiji quan"]
   tags: ["tag1", "tag2"]
   ---

   Article body, Chinese text alongside.
   ```

2. Push to `main` — deployment is automatic (~1 minute).

## Local development

```bash
hugo server -D        # http://localhost:1313
hugo --minify         # build static site into public/
```

## Deployment

Any push to `main` triggers the `.github/workflows/hugo.yml` workflow:
Hugo build + publish to GitHub Pages.

## Credits & license

- **Images**: Guan Yu portrait (detail of *Guan Yu Captures General Pang De*,
  Shang Xi, Ming dynasty, 15th century — Palace Museum, Beijing) and the taiji
  symbol, both **public domain** (Wikimedia Commons).
- **Translations**: original works created for this site from public-domain
  Chinese sources.
- **Theme**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod), MIT license.
- This project takes its form from English-language translation sites such as
  *Brennan Translation* (Paul Brennan) — an essential reference for the source
  texts. The translations published here are independent works.
