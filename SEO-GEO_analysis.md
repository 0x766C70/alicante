# SEO / GEO Analysis — alicanteymas.es

> **Dernière mise à jour :** 2026-05-28 (13:59)
> **Analysé par :** Botbot
> **Version du blog :** 6 articles publiés — Thème Blowfish sur Hugo

---

## Légende des priorités

| Icône | Niveau | Description |
|---|---|---|
| 🔴 | URGENT | Correctif immédiat — impact fort et effort faible |
| 🟡 | MOYEN TERME | À faire dans la foulée — bon ratio effort/impact |
| 🟢 | LONG TERME | Investissement éditorial ou technique plus conséquent |
| ✅ | FAIT | Action terminée |

---

## État global du site (dernière analyse)

| Métrique | Valeur |
|---|---|
| **URL** | https://www.alicanteymas.es |
| **Thème Hugo** | Blowfish |
| **Langue** | Français (fr-FR) uniquement |
| **Articles publiés** | 6 |
| **Catégories** | Gastronomie, Culture & Musées, Vie pratique, À propos |
| **Google Analytics** | GA4 `G-TFG30FJJL2` ✅ |
| **Sitemap** | Auto-généré, hebdomadaire ✅ |
| **robots.txt** | Configuré avec sitemap ✅ |
| **Open Graph** | Image `og-alicanteymas.png` (1200×630) configurée ✅ |
| **Schema.org** | Breadcrumbs OK — Restaurant/Museum absent 🟡 |
| **Google Search Console** | Code de vérification corrigé ✅ |

---

## Points forts identifiés

- `robots.txt` propre avec sitemap déclaré
- GA4 actif et opérationnel
- Sitemap XML auto-généré (fréquence hebdomadaire)
- Breadcrumbs structurés activés (`enableStructuredBreadcrumbs = true`)
- Slugs d'URL propres en français (ex: `/posts/restaurants-mexicains-alicante/`)
- Optimisation d'image Hugo activée
- Accessibilité (a11y) activée
- Tags et catégories affichés sur les articles
- Shortcodes carousel pour les galeries photos

---

## CATÉGORIE 1 — SEO Technique

### 1.1 · Image Open Graph par défaut inutilisable
- **Priorité :** 🔴 URGENT
- **Statut :** ✅ FAIT
- **Fichier :** `config/_default/params.toml` + `static/og-alicanteymas.png`
- **Problème :** `defaultSocialImage = "/android-chrome-512x512.png"` — un favicon 512×512 n'est pas une image OG valide. Les partages sur WhatsApp/Facebook/LinkedIn produisent un aperçu cassé.
- **Action :** ~~Créer une image `og-alicanteymas.jpg` (1200×630px) et mettre à jour le param~~ → `og-alicanteymas.png` créée et `defaultSocialImage = "/og-alicanteymas.png"` configuré ✅

---

### 1.2 · Mauvais code Google Search Console
- **Priorité :** 🔴 URGENT
- **Statut :** ✅ FAIT
- **Fichier :** `config/_default/params.toml` → `[verification]`
- **Problème :** `google = "GTM-KGVJBLJV"` — le champ `google` attend un code GSC (format alphanumérique), pas un ID GTM. Ce sont deux systèmes distincts.
- **Action :** ~~Aller dans Google Search Console → copier le code alphanumérique~~ → Corrigé, code GSC `AMIe6cNA7HH...` en place ✅

---

### 1.3 · `site.webmanifest` — champs vides
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ✅ FAIT
- **Fichier :** `static/site.webmanifest`
- **Problème :** `"name": ""` et `"short_name": ""` étaient vides. Signal de site inachevé pour Google, ajout à l'écran d'accueil mobile impossible.
- **Action :** ~~Remplir avec `"name": "Alicante y MAS"` et `"short_name": "AlicanteYMAS"`~~ → `"name": "Alicante y MAS"` et `"short_name": "alicanteymas"` configurés ✅

---

### 1.4 · Language Switcher affiché sans raison
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ✅ FAIT
- **Fichier :** `config/_default/params.toml`
- **Problème :** `showLanguageSwitcher = true` mais une seule langue configurée. Nuit à l'UX.
- **Action :** ~~Passer à `showLanguageSwitcher = false`~~ → Corrigé ✅

---

### 1.5 · `lastmod` absent des front-matters
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ✅ FAIT
- **Fichiers :** Tous les `content/posts/*/index.md`
- **Problème :** `showDateUpdated = true` est activé mais aucun article n'avait de champ `lastmod`. Hugo et Google ne pouvaient pas détecter les mises à jour.
- **Action :** ~~Ajouter `lastmod = YYYY-MM-DD` dans le front-matter des articles mis à jour.~~ → `lastmod = 2026-05-28` ajouté dans les 6 articles et la page "À propos" ✅

---

### 1.6 · Sitemap — priorité plate (0.5) pour toutes les pages
- **Priorité :** 🟢 LONG TERME
- **Statut :** ✅ FAIT
- **Fichier :** `layouts/sitemap.xml` (créé)
- **Problème :** Tous les contenus avaient la même priorité. Aucune hiérarchie signalée à Google.
- **Action :** ~~Créer `layouts/sitemap.xml` avec une logique de priorité différenciée~~ → Template custom créé avec : accueil `1.0`, articles piliers (param `pilier = true`) `0.9`, articles standards `0.8`, pages statiques `0.6`, taxonomies `0.4` ✅

---

## CATÉGORIE 2 — SEO On-Page

### 2.1 · "Alicante" absent de 4 titres sur 6
- **Priorité :** 🔴 URGENT
- **Statut :** ☐ À faire
- **Problème :** Le mot-clé principal du blog n'apparaît pas dans la majorité des `<h1>`.

| Article | Titre actuel | Titre suggéré |
|---|---|---|
| `que-faire-chaleur-alicante` | *Ola de calor : que faire quand il fait trop chaud ?* | *Que faire à Alicante quand il fait trop chaud ?* |
| `musee-marq-alicante` | *Le MARQ : le musée d'archéologie incontournable* | *Le MARQ d'Alicante : le musée d'archéologie incontournable* |
| `restaurants-mexicains-alicante` | *Restaurants mexicains : nos adresses favorites* | *Meilleurs restaurants mexicains à Alicante : nos 3 adresses testées* |
| `cafe-con-leche-alicante` | *Café con leche y tostadas : le rituel du matin à ne pas manquer* | *Café con leche à Alicante : le rituel du matin à ne pas manquer* |

- **Action :** Mettre à jour le champ `title` dans les front-matters concernés.

---

### 2.2 · Tags — "alicante" et "costa blanca" absents
- **Priorité :** 🔴 URGENT
- **Statut :** ☐ À faire
- **Fichiers :** Tous les `content/posts/*/index.md`
- **Problème :** Aucun article n'a "alicante" ou "costa blanca" comme tag, alors que ce sont les mots-clés centraux du blog.
- **Action :** Ajouter `"alicante"` dans les tags de chaque article. Ajouter `"costa blanca"` sur les articles géographiques.

---

### 2.3 · Méta-descriptions (summaries) à affiner
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire

| Article | Problème |
|---|---|
| `lucentum` | La summary contient `[source]` — pas une vraie meta description |
| `que-faire-chaleur` | Trop courte, pas de CTA |

- **Action :** Réécrire les summaries selon la règle : **120-160 caractères**, inclure "Alicante", finir par un CTA implicite.

---

### 2.4 · Liens internes — quasi absents
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Problème :** Très peu de liens croisés entre articles. Maillage interne faible.
- **Action :** Ajouter 2 liens internes pertinents dans chaque article. Exemples :
  - `que-faire-chaleur` → lier vers `musee-marq-alicante` et `lucentum`
  - `cafe-con-leche` → lier vers `restaurant-alba` ou `restaurants-mexicains`

---

### 2.5 · Page d'accueil `_index.md` trop vide
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Fichier :** `content/_index.md`
- **Problème :** Contient uniquement un titre. C'est la page la mieux positionnée du site — elle mérite du contenu texte avec les mots-clés.
- **Action :** Ajouter 2-3 paragraphes naturels avec : "famille française à Alicante", "vie à la Costa Blanca", "blog expatriés", "Casa Azul".

---

### 2.6 · Alt text des images — absent sur les galeries
- **Priorité :** 🟢 LONG TERME
- **Statut :** ☐ À faire
- **Problème :** Le shortcode `{{< carousel images="gallery/*" >}}` ne passe pas d'attribut `alt`. Toutes les images de galerie sont sans texte alternatif.
- **Action :**
  1. Court terme : vérifier si Blowfish supporte `alt` dans le shortcode `figure` pour les images clés.
  2. Moyen terme : remplacer le shortcode carousel par des shortcodes `figure` avec `alt` explicite sur les images les plus importantes.

---

## CATÉGORIE 3 — Local SEO (signaux géographiques)

### 3.1 · Schema.org Restaurant/Museum absent
- **Priorité :** 🟢 LONG TERME
- **Statut :** ☐ À faire
- **Problème :** Pas de balisage structuré pour les établissements locaux. Google et Maps ne peuvent pas extraire automatiquement les infos.
- **Action :** Créer `layouts/partials/schema-local.html` avec JSON-LD `Restaurant` / `Museum` et l'inclure dans les articles concernés.

---

### 3.2 · "Costa Blanca" absent du contenu des articles
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Problème :** "Costa Blanca" n'apparaît que dans la description du site, jamais dans le corps des articles ni les tags.
- **Action :** Intégrer "Costa Blanca" naturellement dans les intros des articles géographiques et dans les tags.

---

### 3.3 · Catégorie "Vie pratique" sous-exploitée
- **Priorité :** 🟢 LONG TERME
- **Statut :** ☐ À faire
- **Problème :** Une seule page dans la catégorie la plus cherchée par les familles planifiant un séjour ou une expatriation.
- **Sujets à fort potentiel :** "vivre à Alicante famille", "expat Alicante", "transports Alicante TRAM", "Costa Blanca avec enfants", "médecin Alicante expatriés"

---

## CATÉGORIE 4 — GEO (Generative Engine Optimization)

*Optimisation pour ChatGPT, Perplexity, Google AI Overviews, Bing Copilot*

### 4.1 · Aucune section FAQ dans les articles
- **Priorité :** 🔴 URGENT
- **Statut :** ☐ À faire
- **Problème :** Les sections FAQ sont la nourriture préférée des LLMs. Leur absence réduit drastiquement la probabilité d'être cité dans une réponse IA.
- **Action :** Ajouter une section `## Questions fréquentes` avec 3-5 Q/R en fin de chaque article. Exemples :
  - *"Le MARQ est-il gratuit pour les enfants ?"*
  - *"Peut-on aller à Lucentum en transports en commun ?"*
  - *"Quel est le prix du menu dégustation chez Alba ?"*
  - *"À quelle heure ouvre Lucentum ?"*

---

### 4.2 · Infoboxes / tableaux "Infos pratiques" absents
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Problème :** Un tableau structuré est beaucoup plus facilement extrait par une IA qu'un paragraphe narratif.
- **Action :** Ajouter pour chaque article restaurant/musée un tableau récapitulatif en fin d'article :

```markdown
| | |
|---|---|
| **Adresse** | Calle Mayor, Alicante |
| **Prix** | Menu dégustation 37,50€ |
| **Réservation** | Recommandée |
| **Transport** | TRAM station MARQ |
| **Site officiel** | [lien](...) |
```

---

### 4.3 · Sources et liens externes insuffisants
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Problème :** Seul Lucentum cite une source officielle. Les LLMs priorisent les pages qui prouvent leurs affirmations par des liens externes.
- **Action :** Dans chaque article avec des faits (prix, horaires, adresses), ajouter un lien vers la source officielle (site du musée, Guide Michelin, alicanteymas.es, etc.).

---

### 4.4 · Profil auteur trop mince (E-E-A-T)
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Fichiers :** `config/_default/languages.fr.toml`, `content/a-propos-de-nous/index.md`
- **Problème :** La bio auteur est trop courte et manque de signaux d'expertise (principe E-E-A-T de Google). Les moteurs IA priorisent les auteurs identifiables avec une expertise locale démontrée.
- **Action :**
  1. Enrichir la bio dans `languages.fr.toml` : durée d'installation, fréquence des séjours, domaines d'expertise
  2. Enrichir `a-propos-de-nous/index.md` avec des détails concrets sur la famille et l'ancrage alicantino
  3. Envisager des profils auteurs distincts pour les différents membres de la Mifa (Blowfish supporte la taxonomie `authors`)

---

### 4.5 · Données structurées `BlogPosting` à vérifier
- **Priorité :** 🟢 LONG TERME
- **Statut :** ☐ À faire
- **Problème :** Blowfish génère du Schema.org de base mais `BlogPosting` avec `datePublished`, `dateModified`, `author`, `wordCount` n'est pas garanti.
- **Action :**
  1. Tester avec [Rich Results Test](https://search.google.com/test/rich-results) sur 2-3 URLs
  2. Si absent, créer `layouts/partials/head/schema-article.html` avec le JSON-LD `BlogPosting`

---

## CATÉGORIE 5 — Stratégie Éditoriale

### 5.1 · Volume — 6 articles insuffisants pour l'autorité thématique
- **Priorité :** 🔴 URGENT (éditorial)
- **Statut :** ☐ En cours
- **Problème :** Google et les LLMs accordent de l'autorité aux sites qui couvrent un sujet en profondeur. 6 articles ne suffisent pas pour ranker sur "Alicante famille".
- **Sujets prioritaires à rédiger :**

| Sujet | Volume estimé | Catégorie |
|---|---|---|
| "Que faire à Alicante avec des enfants" | Très fort | Avec les enfants |
| "Visiter le Château Santa Bárbara" | Fort | Culture & Musées |
| "Plages d'Alicante : guide complet" | Fort | Vie pratique |
| "Vivre à Alicante : guide de l'expat français" | Fort | Vie pratique |
| "Marché central d'Alicante" | Moyen | Gastronomie |
| "Fêtes de San Juan à Alicante" | Moyen | Culture & Musées |
| "TRAM Alicante : comment se déplacer ?" | Moyen | Vie pratique |

---

### 5.2 · Séries d'articles non utilisées
- **Priorité :** 🟡 MOYEN TERME
- **Statut :** ☐ À faire
- **Problème :** Blowfish supporte les séries (navigation dédiée, maillage interne automatique). Cette fonctionnalité n'est pas exploitée.
- **Action :** Créer la série `"Nos musées préférés"` regroupant MARQ, Lucentum, MACA/MUBAG. Ajouter `series = ["Nos musées préférés"]` dans les front-matters concernés.

---

### 5.3 · Catégories à enrichir
- **Priorité :** 🟢 LONG TERME
- **Statut :** ☐ À faire
- **Action :** Envisager deux nouvelles catégories :
  - **"Avec les enfants"** — contenu très cherché par les familles
  - **"Expat & Vie locale"** — pour les articles pratiques d'installation

---

## Tableau de bord récapitulatif

| # | Action | Catégorie | Priorité | Statut |
|---|---|---|---|---|
| 1 | Titres — ajouter "Alicante" aux 4 articles | On-Page | 🔴 | ☐ |
| 2 | Créer image OG 1200×630px | Technique | 🔴 | ✅ |
| 3 | Corriger code Google Search Console | Technique | 🔴 | ✅ |
| 4 | FAQ dans chaque article (3-5 Q/R) | GEO | 🔴 | ☐ |
| 5 | Ajouter tags "alicante" / "costa blanca" | On-Page | 🔴 | ☐ |
| 6 | Remplir `site.webmanifest` (name/short_name) | Technique | 🟡 | ✅ |
| 7 | Infoboxes "Infos pratiques" dans les articles | GEO | 🟡 | ☐ |
| 8 | Liens internes croisés (2 min. par article) | On-Page | 🟡 | ☐ |
| 9 | Enrichir `_index.md` avec texte SEO | On-Page | 🟡 | ☐ |
| 10 | `showLanguageSwitcher = false` | Technique | 🟡 | ✅ |
| 11 | Enrichir bio auteur + page "À propos" | GEO / E-E-A-T | 🟡 | ☐ |
| 12 | Ajouter `lastmod` dans les front-matters | Technique | 🟡 | ✅ |
| 13 | Ajouter sources/liens officiels dans articles | GEO | 🟡 | ☐ |
| 14 | Récrire summaries problématiques | On-Page | 🟡 | ☐ |
| 15 | "Costa Blanca" dans le contenu des articles | Local SEO | 🟡 | ☐ |
| 16 | Séries d'articles (ex: "Nos musées préférés") | Éditorial | 🟡 | ☐ |
| 17 | Schema.org Restaurant/Museum (JSON-LD) | Local SEO | 🟢 | ☐ |
| 18 | Vérifier/créer `BlogPosting` structured data | GEO | 🟢 | ☐ |
| 19 | Alt text sur images de galeries | Technique | 🟢 | ☐ |
| 20 | Priorités différenciées dans le sitemap | Technique | 🟢 | ✅ |
| 21 | 7+ nouveaux articles sujets piliers | Éditorial | 🟢 | ☐ |
| 22 | Nouvelles catégories ("Avec les enfants", etc.) | Éditorial | 🟢 | ☐ |

---

*Pour mettre à jour ce fichier : changer le statut `☐` en `✅` quand une action est terminée, et mettre à jour la date en en-tête.*
