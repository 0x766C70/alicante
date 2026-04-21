# Alicante y MAS — alicanteymas.es

[![Build and deploy](https://github.com/0x766C70/alicante/actions/workflows/hugo.yml/badge.svg)](https://github.com/0x766C70/alicante/actions/workflows/hugo.yml)

*Un blog de famille sur la vida alicantina* — built with [Hugo](https://gohugo.io/) + [Blowfish](https://blowfish.page/), deployed on [GitHub Pages](https://pages.github.com/).

---

## About the blog

*Alicante y MAS* is a family blog written in French by **vlp** (Thomas — the tech guy) and **Albane** (the one with actual taste in fashion and food). Since a spontaneous Easter 2023 trip landed them on the Esplanada, the whole family has been spending two months a year in Alicante — and showing no signs of stopping.

The cast:

| Nickname | Real name | Born |
|---|---|---|
| — | Thomas (vlp) | the one reading this README |
| — | Albane | lifestyle, fashion & the real brains |
| **la Princesse** | Garance | 2015 |
| **le Chouetton** | Auguste | 2018 |
| **la Pomponette** | Philippine | 2022 |

Together they make up **la Mifa** — and they write about everything that makes life at the *Casa Azul* and in Alicante worth sharing: café con leche for under €2, free museums on rainy days, the best toastadas in town, and all the small pleasures of *la vida alicantina*.

The blog is aimed at French-speaking families who want to discover Alicante through the eyes of people who genuinely live there — not a listicle, not a travel agency. Just honest, warm, first-hand experience.

---

## Website structure

```
alicante/
├── .github/
│   ├── agents/
│   │   └── botbot-writer.md    # Botbot custom agent prompt
│   └── workflows/
│       └── hugo.yml            # CI/CD: build & deploy to GitHub Pages on push to main
├── archetypes/
│   └── default.md              # Default front-matter template for new posts
├── assets/
│   ├── gallery/                # Shared image gallery assets
│   ├── home.png                # Homepage hero/card image
│   └── profile.png             # Author profile picture / site logo
├── config/
│   └── _default/
│       ├── hugo.toml           # Core Hugo settings (base URL, pagination, taxonomies…)
│       ├── languages.en.toml   # Language settings and author metadata
│       ├── markup.toml         # Markdown / syntax-highlight options
│       ├── menus.en.toml       # Navigation menus (header & footer)
│       ├── module.toml         # Hugo module / theme import
│       └── params.toml         # Blowfish theme parameters (layout, colours, features…)
├── content/
│   ├── _index.md               # Homepage introduction text
│   └── posts/
│       ├── cafe/               # Article: Café con leche & local cafeterías
│       ├── marq/               # Article: MARQ archaeology museum & BARQ restaurant
│       └── ola/                # Article: Things to do during a heatwave (free museums)
├── public/                     # Hugo build output (generated, not committed)
└── themes/                     # Blowfish theme (git submodule)
```

### Content taxonomy

Posts are organised with two taxonomy types:

| Taxonomy | Example values |
|---|---|
| **Tags** | `cafe`, `lifestyle`, `culture`, `musées`, `pluie`, `canicule` |
| **Categories** | *(available, not yet used)* |

### Navigation

| Menu item | Points to |
|---|---|
| Posts | `/posts/` — full article list |
| Tags | `/tags/` — browsable tag index |

---

## Writing a new article

Each article lives in its own folder under `content/posts/` and must contain an `index.md` file. Use the archetype to scaffold it:

```bash
hugo new content posts/my-article/index.md
```

A minimal front-matter block looks like this (TOML format):

```toml
+++
title   = 'Mon titre accrocheur'
date    = 2025-04-19
summary = "Une phrase qui donne envie de lire la suite."
tags    = ["lifestyle", "cafe"]
draft   = false
+++
```

Put images alongside `index.md` in the same folder and reference them relatively in the article body. Set `draft = true` while writing; flip to `false` when ready to publish.

---

## Tech stack

| Component | Version / details |
|---|---|
| Static site generator | [Hugo Extended](https://gohugo.io/) `0.160.0` |
| Theme | [Blowfish](https://blowfish.page/) (git submodule — `themes/`) |
| CSS pre-processor | Dart Sass `1.99.0` |
| Hosting | GitHub Pages |
| Domain | `alicanteymas.es` |
| CI/CD | GitHub Actions — auto-deploy on push to `main` |

---

## Local development

```bash
# clone with submodules (Blowfish theme)
git clone --recurse-submodules https://github.com/0x766C70/alicante.git

# serve the site with live reload
hugo server

# build for production
hugo build --gc --minify
```

> The generated files land in `public/`. **Do not commit this directory.**

### Deployment

Pushing to `main` automatically triggers the **Build and deploy** GitHub Actions workflow (`.github/workflows/hugo.yml`), which builds the site with Hugo Extended and deploys it to GitHub Pages. No manual step required — *Alicante y MAS* is live within a minute of merging.
