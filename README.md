# Alicante y MAS — alicanteymas.es

A family travel blog about life in Alicante, built with [Hugo](https://gohugo.io/) using the [Blowfish](https://blowfish.page/) theme.

## About the website

*Alicante y MAS* is a personal blog run by Thomas and Albane, parents of three children (Garance, Auguste and Philippine). Since their first trip to Alicante at Easter 2023, the family fell in love with the city and has been spending two months a year there. The site shares their authentic experience of *la vida alicantina*: family outings, cultural discoveries, local food spots, lifestyle tips and all the small pleasures that make Alicante so special.

The blog is written in French and is aimed at families who want to discover Alicante through the eyes of people who genuinely live there.

## Website structure

```
alicante/
├── archetypes/
│   └── default.md          # Default front-matter template for new posts
├── assets/
│   ├── gallery/            # Shared image gallery assets
│   ├── home.png            # Homepage hero/card image
│   └── profile.png         # Author profile picture / site logo
├── config/
│   └── _default/
│       ├── hugo.toml           # Core Hugo settings (base URL, pagination, taxonomies…)
│       ├── languages.en.toml   # Language settings and author metadata
│       ├── markup.toml         # Markdown / syntax-highlight options
│       ├── menus.en.toml       # Navigation menus (header & footer)
│       ├── module.toml         # Hugo module / theme import
│       └── params.toml         # Blowfish theme parameters (layout, colours, features…)
├── content/
│   ├── _index.md           # Homepage introduction text
│   └── posts/
│       ├── cafe/           # Article: Café con leche & local cafeterías
│       ├── marq/           # Article: MARQ archaeology museum & BARQ restaurant
│       └── ola/            # Article: Things to do during a heatwave (free museums)
├── public/                 # Hugo build output (generated, not committed)
└── themes/                 # Blowfish theme (git submodule)
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

## Tech stack

| Component | Details |
|---|---|
| Static site generator | [Hugo](https://gohugo.io/) |
| Theme | [Blowfish](https://blowfish.page/) (git submodule in `themes/`) |
| Hosting / domain | `alicanteymas.es` |

## Local development

```bash
# serve the site with live reload
hugo server

# build for production
hugo
```

> The generated files land in `public/`. Do not commit this directory.
