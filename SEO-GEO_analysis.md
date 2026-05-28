# SEO / GEO Analysis — alicanteymas.es

> **Dernière mise à jour :** 2026-05-28 (14:36)
> **Analysé par :** Botbot
> **Objectif de ranking :** `alicante famille`
> **Version du blog :** 6 articles publiés — Thème Blowfish sur Hugo

---

## Légende des priorités

| Icône | Niveau | Description |
|---|---|---|
| 🔴 | URGENT | Correctif immédiat — impact fort et effort faible |
| 🟡 | MOYEN TERME | À faire dans la foulée — bon ratio effort/impact |
| 🟢 | LONG TERME | Investissement éditorial ou technique plus conséquent |

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
| **Sitemap** | Custom avec priorités différenciées ✅ |
| **robots.txt** | Configuré avec sitemap ✅ |
| **Open Graph** | Image `og-alicanteymas.png` (1200×630) ✅ |
| **Schema.org** | Breadcrumbs OK — Restaurant/Museum absent 🟡 |
| **Google Search Console** | Code de vérification corrigé ✅ |
| **`lastmod`** | Présent dans les 6 articles ✅ |
| **Tags "alicante"** | Tous les articles ✅ — "costa blanca" absent 🟡 |
| **Titres avec "Alicante"** | 6/6 articles ✅ |

---

## Points forts identifiés

- `robots.txt` propre avec sitemap déclaré
- GA4 actif et opérationnel
- Sitemap XML custom avec priorités différenciées (accueil `1.0`, piliers `0.9`, articles `0.8`)
- Breadcrumbs structurés activés (`enableStructuredBreadcrumbs = true`)
- Slugs d'URL propres en français (ex: `/posts/restaurants-mexicains-alicante/`)
- Optimisation d'image Hugo activée
- Accessibilité (a11y) activée
- Tags "Alicante" présents dans tous les articles
- "Alicante" dans tous les titres H1
- `lastmod` à jour dans tous les front-matters
- `site.webmanifest` correctement rempli
- Image OG 1200×630px configurée
- Tag `famille` présent dans 5/6 articles

---

## CATÉGORIE 1 — SEO On-Page

### 1.1 · Lien interne cassé dans `que-faire-chaleur-alicante`
- **Priorité :** 🔴 URGENT
- **Fichier :** `content/posts/que-faire-chaleur-alicante/index.md`
- **Problème :** Le lien vers le MARQ pointe sur `/posts/posts/musee-marq-alicante/` (double "posts") — 404 garanti. Un lien cassé nuit au crawl et à l'UX.
- **Action :** Corriger en `/posts/musee-marq-alicante/`.

---

### 1.2 · Tags — "costa blanca" absent de tous les articles
- **Priorité :** 🔴 URGENT
- **Fichiers :** Tous les `content/posts/*/index.md`
- **Problème :** "costa blanca" n'est tag dans aucun article alors que c'est le second mot-clé géographique central du blog. La page de tag `/tags/costa-blanca/` n'existe pas.
- **Action :** Ajouter `"costa blanca"` dans les tags de tous les articles géographiques/famille : Lucentum, MARQ, que-faire-chaleur, café con leche.

---

### 1.3 · Liens internes — maillage quasi inexistant
- **Priorité :** 🟡 MOYEN TERME
- **Fichiers :** Tous les `content/posts/*/index.md`
- **Problème :** Seul `que-faire-chaleur` a un lien interne (vers le MARQ — mais cassé). Zéro lien dans les 5 autres articles. Un maillage faible empêche Google de comprendre la hiérarchie du site.
- **Action :** Ajouter 2 liens internes pertinents dans chaque article :
  - `lucentum` → lier vers `musee-marq-alicante` ("notre guide des musées d'Alicante en famille")
  - `musee-marq-alicante` → lier vers `lucentum` et `que-faire-chaleur`
  - `cafe-con-leche` → lier vers `restaurants-mexicains` ou `restaurant-alba`
  - `restaurants-mexicains` → lier vers `restaurant-alba`
  - `restaurant-alba` → lier vers `restaurants-mexicains`

---

### 1.4 · Page d'accueil `_index.md` quasi vide
- **Priorité :** 🟡 MOYEN TERME
- **Fichier :** `content/_index.md`
- **Problème :** Contient uniquement un titre. C'est la page la mieux positionnée du site et le premier signal sémantique pour Google — elle ne dit rien sur "Alicante" ni "famille".
- **Action :** Ajouter 2-3 paragraphes naturels avec : "famille française à Alicante", "vie à la Costa Blanca", "blog de la Mifa expatriée", "Casa Azul", "activités en famille", "alicante avec enfants".

---

### 1.5 · Tag "famille" manquant sur `restaurant-alba`
- **Priorité :** 🟡 MOYEN TERME
- **Fichier :** `content/posts/restaurant-alba-alicante/index.md`
- **Problème :** Le tag "famille" est absent de cet article alors qu'il est présent dans 5/6 articles. La page de tag `/tags/famille/` perd un article.
- **Action :** Ajouter `"famille"` dans les tags du front-matter.

---

### 1.6 · Alt text des images — absent sur les galeries
- **Priorité :** 🟢 LONG TERME
- **Problème :** Le shortcode `{{< carousel images="gallery/*" >}}` ne passe pas d'attribut `alt`. Toutes les images de galerie sont invisibles pour Google Images et les lecteurs d'écran.
- **Action :**
  1. Vérifier si Blowfish supporte `alt` dans le shortcode `figure` pour les images clés.
  2. Remplacer le shortcode carousel par des shortcodes `figure` avec `alt` explicite sur les images les plus importantes (ex: `alt="Musée MARQ d'Alicante en famille"`).

---

## CATÉGORIE 2 — Local SEO (signaux géographiques)

### 2.1 · "Costa Blanca" absent du corps des articles
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** "Costa Blanca" n'apparaît nulle part dans le corps des articles — ni les intros, ni les corps de texte. Le signal géographique est inexistant pour les requêtes "costa blanca famille".
- **Action :** Intégrer "Costa Blanca" naturellement dans les intros des articles à fort ancrage géographique (Lucentum, que-faire-chaleur, café con leche). Exemple : *"À Alicante, sur la Costa Blanca..."*

---

### 2.2 · Schema.org Restaurant/Museum absent
- **Priorité :** 🟢 LONG TERME
- **Problème :** Pas de balisage structuré pour les établissements locaux. Google et Maps ne peuvent pas extraire automatiquement les infos. Impact fort pour les recherches "restaurant alicante famille" ou "musée alicante enfants".
- **Action :** Créer `layouts/partials/schema-local.html` avec JSON-LD `Restaurant` / `Museum` / `TouristAttraction` (avec `audience: families`) et l'inclure dans les articles concernés.

---

### 2.3 · Catégorie "Vie pratique" sous-exploitée
- **Priorité :** 🟢 LONG TERME
- **Problème :** Une seule page dans la catégorie la plus cherchée par les familles planifiant un séjour ou une expatriation.
- **Sujets à fort potentiel :**
  - "vivre à Alicante en famille"
  - "transports Alicante TRAM avec enfants"
  - "Costa Blanca avec enfants : notre guide"
  - "médecin Alicante expatriés"
  - "école française Alicante"

---

## CATÉGORIE 3 — GEO (Generative Engine Optimization)

*Optimisation pour ChatGPT, Perplexity, Google AI Overviews, Bing Copilot*

### 3.1 · Aucune section FAQ dans les articles
- **Priorité :** 🔴 URGENT
- **Problème :** Les sections FAQ sont la nourriture préférée des LLMs. Leur absence réduit drastiquement la probabilité d'être cité dans une réponse IA pour "que faire à alicante en famille".
- **Action :** Ajouter une section `## Questions fréquentes` avec 3-5 Q/R en fin de chaque article. Privilégier les formulations "avec des enfants" / "en famille". Exemples :
  - *"Le MARQ est-il adapté aux enfants ?"* / *"À partir de quel âge visiter Lucentum ?"*
  - *"Peut-on aller à la plage après Lucentum ?"* / *"Le MACA est-il gratuit pour les enfants ?"*
  - *"Quel restaurant mexicain est le mieux pour une famille ?"*

---

### 3.2 · Infoboxes / tableaux "Infos pratiques" absents
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Un tableau structuré est beaucoup plus facilement extrait par une IA qu'un paragraphe narratif. Sans infobox, le risque d'être ignoré par les AI Overviews est élevé.
- **Action :** Ajouter pour chaque article restaurant/musée un tableau récapitulatif en fin d'article :

```markdown
| | |
|---|---|
| **Adresse** | Calle Mayor, Alicante |
| **Prix** | Menu dégustation 37,50€ |
| **Adapté aux familles** | Oui — terrasse sécurisée |
| **Réservation** | Recommandée |
| **Transport** | TRAM station MARQ |
| **Site officiel** | [lien](...) |
```

---

### 3.3 · Sources et liens externes insuffisants
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Seul Lucentum cite une source officielle. Les LLMs priorisent les pages qui prouvent leurs affirmations par des liens externes de confiance.
- **Action :** Dans chaque article avec des faits (prix, horaires, adresses), ajouter un lien vers la source officielle (site du musée, Guide Michelin, alicanteturismo.com, etc.).

---

### 3.4 · Profil auteur trop mince (E-E-A-T)
- **Priorité :** 🟡 MOYEN TERME
- **Fichiers :** `config/_default/languages.fr.toml`, `content/a-propos-de-nous/index.md`
- **Problème :** La bio auteur est trop courte et manque de signaux d'expertise locale. Les moteurs IA priorisent les auteurs identifiables avec une expertise démontrée sur le terrain — une famille qui *vit* à Alicante est un signal E-E-A-T très fort s'il est mis en avant.
- **Action :**
  1. Enrichir la bio dans `languages.fr.toml` : durée d'installation, fréquence des séjours, quartier (les Carolinas !), domaines d'expertise (gastronomie, musées, activités famille)
  2. Enrichir `a-propos-de-nous/index.md` avec des détails concrets : la Casa Azul, les enfants, les rituels alicantinos
  3. Envisager des profils auteurs distincts pour vlp et Albane (Blowfish supporte la taxonomie `authors`)

---

### 3.5 · Données structurées `BlogPosting` à vérifier
- **Priorité :** 🟢 LONG TERME
- **Problème :** Blowfish génère du Schema.org de base mais `BlogPosting` avec `datePublished`, `dateModified`, `author`, `wordCount` n'est pas garanti.
- **Action :**
  1. Tester avec [Rich Results Test](https://search.google.com/test/rich-results) sur 2-3 URLs
  2. Si absent, créer `layouts/partials/head/schema-article.html` avec le JSON-LD `BlogPosting`

---

## CATÉGORIE 4 — Stratégie "Alicante Famille" 🎯

*Actions spécifiques pour ranker sur la requête cible `alicante famille`*

### 4.1 · Aucun article pilier "Alicante en famille" — le vide à combler en priorité
- **Priorité :** 🔴 URGENT (éditorial)
- **Problème :** La requête "alicante famille" / "alicante avec enfants" / "que faire à alicante en famille" est la cible principale du blog. Il n'existe pas d'article dédié qui consolide toutes les expériences famille. C'est le contenu manquant le plus critique.
- **Action :** Rédiger un article pilier (1500+ mots) :
  - **Titre H1 :** *"Alicante en famille : notre guide complet des meilleures activités avec enfants"*
  - **Slug :** `/posts/alicante-en-famille/`
  - **Contenu :** musées (MARQ, Lucentum, MACA/MUBAG), plages accessibles, restaurants family-friendly, TRAM, budget, conseils pratiques
  - **Liens internes :** vers les 5 articles famille existants
  - **Tags :** `["alicante", "famille", "enfants", "costa blanca", "activités"]`
  - **Param :** `pilier = true` (pour le sitemap custom)

---

### 4.2 · "En famille" / "avec enfants" absent des H2 des articles existants
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Les articles sont family-friendly dans leur contenu mais leurs titres de section (H2/H3) ne le signalent pas à Google. La requête "musée alicante enfants" est une longue traîne à fort potentiel non adressée.
- **Action :** Ajouter un H2 orienté famille dans les articles clés :
  - `musee-marq-alicante` → ajouter `## Pourquoi le MARQ est idéal pour les familles avec enfants`
  - `lucentum` → renommer la section randonnée en `## Randonnée en famille : nos deux itinéraires conseillés`
  - `restaurants-mexicains` → ajouter `## Le meilleur pour les familles : Mexican Granny`

---

### 4.3 · La phrase exacte "Alicante en famille" absente des corps d'articles
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Aucun article ne contient la phrase exacte "Alicante en famille" dans son corps de texte. Les moteurs de recherche et les LLMs ne peuvent pas l'associer à cette requête cible.
- **Action :** Intégrer naturellement "Alicante en famille" ou "à Alicante en famille" dans l'intro ou la conclusion de chaque article family-friendly (MARQ, Lucentum, que-faire-chaleur, café con leche, restaurants mexicains).

---

### 4.4 · Catégorie dédiée "Avec les enfants" manquante
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Les familles qui cherchent "alicante famille" atterrissent sur des articles éparpillés dans des catégories hétérogènes (Culture, Gastronomie, Vie pratique). Il n'existe pas de point d'entrée unique pour le contenu famille — un signal d'autorité thématique inexploité.
- **Action :**
  1. Créer la catégorie `"Avec les enfants"` dans Hugo
  2. Re-catégoriser MARQ, Lucentum, que-faire-chaleur (double catégorie possible sous Hugo)
  3. L'article pilier 4.1 doit impérativement être dans cette catégorie
  4. Ajouter une `_index.md` de catégorie avec description SEO : "Toutes nos idées d'activités à Alicante avec les enfants — musées, plages, randonnées et adresses family-friendly testées par la Mifa."

---

### 4.5 · Série "Alicante en famille" non créée
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** Blowfish supporte les séries (navigation dédiée, maillage interne automatique). Regrouper les articles famille dans une série crée un cluster sémantique fort et améliore le temps passé sur le site.
- **Action :**
  1. Créer la série `"Alicante en famille"` dans les front-matters : `series = ["Alicante en famille"]`
  2. Articles à inclure : pilier famille (4.1), MARQ, Lucentum, que-faire-chaleur, café con leche, restaurants mexicains

---

## CATÉGORIE 5 — Stratégie Éditoriale

### 5.1 · Volume — 6 articles insuffisants pour l'autorité thématique
- **Priorité :** 🔴 URGENT (éditorial)
- **Problème :** Google et les LLMs accordent de l'autorité aux sites qui couvrent un sujet en profondeur. 6 articles ne suffisent pas pour ranker durablement sur "alicante famille".
- **Sujets prioritaires à rédiger (par potentiel sur la requête cible) :**

| Sujet | Angle famille | Volume estimé | Catégorie |
|---|---|---|---|
| "Plages d'Alicante avec des enfants" | Fort | Très fort | Avec les enfants |
| "Château Santa Bárbara : visite en famille" | Fort | Fort | Avec les enfants |
| "TRAM Alicante : se déplacer en famille" | Fort | Moyen | Vie pratique |
| "Vivre à Alicante : guide de l'expat français" | Moyen | Fort | Vie pratique |
| "Marché central d'Alicante" | Moyen | Moyen | Gastronomie |
| "Fêtes de San Juan à Alicante" | Moyen | Moyen | Culture & Musées |
| "Playa de San Juan : notre plage de famille" | Très fort | Fort | Avec les enfants |

---

### 5.2 · Série "Nos musées préférés" non créée
- **Priorité :** 🟡 MOYEN TERME
- **Problème :** MARQ, Lucentum et MACA/MUBAG sont trois articles de la même thématique sans navigation croisée entre eux.
- **Action :** Créer la série `"Nos musées préférés"`. Ajouter `series = ["Nos musées préférés"]` dans les front-matters de MARQ, Lucentum et que-faire-chaleur.

---

## Tableau de bord récapitulatif

| # | Action | Catégorie | Priorité |
|---|---|---|---|
| 1 | Corriger le lien cassé `/posts/posts/...` dans que-faire-chaleur | On-Page | 🔴 |
| 2 | Ajouter tag "costa blanca" aux articles géographiques | On-Page | 🔴 |
| 3 | FAQ dans chaque article (3-5 Q/R orientées famille) | GEO | 🔴 |
| 4 | Article pilier "Alicante en famille" (1500+ mots) | Famille 🎯 | 🔴 |
| 5 | Enrichir `_index.md` avec texte SEO famille | On-Page | 🟡 |
| 6 | "En famille" dans les H2 des articles existants | Famille 🎯 | 🟡 |
| 7 | Phrase "Alicante en famille" dans les intros/conclusions | Famille 🎯 | 🟡 |
| 8 | Créer la catégorie "Avec les enfants" + `_index.md` | Famille 🎯 | 🟡 |
| 9 | Ajouter tag "famille" sur restaurant-alba | On-Page | 🟡 |
| 10 | Liens internes croisés (2 min. par article) | On-Page | 🟡 |
| 11 | "Costa Blanca" dans le corps des articles | Local SEO | 🟡 |
| 12 | Infoboxes "Infos pratiques" avec champ "Adapté familles" | GEO | 🟡 |
| 13 | Ajouter sources/liens officiels dans articles | GEO | 🟡 |
| 14 | Enrichir bio auteur + page "À propos" (E-E-A-T) | GEO | 🟡 |
| 15 | Série "Alicante en famille" (Blowfish series) | Famille 🎯 | 🟡 |
| 16 | Série "Nos musées préférés" | Éditorial | 🟡 |
| 17 | 7+ nouveaux articles sujets piliers (priorité plages + château) | Éditorial | 🟢 |
| 18 | Schema.org Restaurant/Museum/TouristAttraction (JSON-LD) | Local SEO | 🟢 |
| 19 | Vérifier/créer `BlogPosting` structured data | GEO | 🟢 |
| 20 | Alt text sur images de galeries | Technique | 🟢 |

---

*Pour mettre à jour ce fichier : supprimer les lignes dont les actions sont terminées (ne pas les taguer ✅, les retirer) et ajouter de nouvelles suggestions. Mettre à jour la date en en-tête.*
