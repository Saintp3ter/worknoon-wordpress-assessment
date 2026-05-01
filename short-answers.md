# Short Answer Questions – Section E

## 1. Difference between Google Knowledge Graph and Google Knowledge Panel

| **Knowledge Graph** | **Knowledge Panel** |
|---------------------|----------------------|
| A massive database of entities (people, places, things) and their relationships used by Google to understand real-world facts. | A visible information box shown on Google search results (typically on the right side on desktop, or top on mobile). |
| Not visible to users – it's backend structured data. | Visible to users – it displays facts, images, social profiles, etc. |
| Powers Knowledge Panels, rich results, and voice search answers. | A visual presentation derived from the Knowledge Graph and other trusted sources (Wikipedia, Wikidata, official site, schema markup). |
| Built from structured data, public databases, and user contributions. | Requires entity recognition and authority signals; can be claimed or suggested via Google’s feedback tools. |

**Key takeaway:** The Knowledge Graph is the engine; the Knowledge Panel is the dashboard displayed to users.

---

## 2. How Google determines entity identity

Google uses multiple signals to understand and distinguish an entity (e.g., a specific person, business, or thing):

- **Unique identifiers** – Wikidata ID, Wikipedia URL, official website.
- **Consistent structured data** – Schema markup (sameAs, name, identifier) across multiple pages.
- **Entity salience** – How prominently the entity appears across authoritative sources.
- **Co-occurrence & linking** – Other reputable entities linking to or referencing this entity.
- **Contextual signals** – Disambiguation via categories, locations, or time (e.g., “Apple Inc.” vs. “apple fruit”).
- **User behavior signals** – Search queries and click patterns help confirm identity.

Google’s Knowledge Graph fuses these signals into a unique entity ID.

---

## 3. When to create Custom Post Types instead of pages

Use **Custom Post Types (CPTs)** when content has:

- **Recurring, structured fields** – e.g., each portfolio item has client name, date, image gallery, tech stack.
- **Different permalink structure** – e.g., `website.com/case-studies/post-name` vs. `/services/`.
- **Custom admin UI** – separate menu, columns, filters.
- **Taxonomy hierarchies** – categories/tags that differ from blog categories.
- **Scalability** – more than 30–50 similar items (pages become unmanageable).

**Example:**  
- Pages = static “About”, “Contact”, “Services”.  
- CPT = “Projects” (100+ items) or “Team Members” (each with bio, photo, social links).

Avoid CPTs for one‑off content – pages are simpler and faster for unique pages.

---

## 4. Recommended plugins for speed optimization and why

| Plugin | Why recommended |
|--------|----------------|
| **WP Rocket** (premium) | All-in-one: page caching, gzip, file minification, lazy loading, CDN integration – easiest for non‑developers. |
| **LiteSpeed Cache** (free for LiteSpeed servers) | Full‑page cache, image optimisation (WebP), CSS/JS combine, and edge caching if using QUIC.cloud CDN. |
| **Autoptimize** (free) | Excellent for minifying scripts/styles, async loading, and moving JS to footer – works alongside caching plugins. |
| **Smush or ShortPixel** (free/premium) | Lossless/lossy image compression, WebP conversion, lazy loading – images are the #1 speed factor. |
| **Perfmatters** (premium) | Disables unused WordPress scripts (embeds, dashicons, emojis) and selectively loads CSS/JS only where needed. |

**Why these matter:** Core Web Vitals (LCP, FID, CLS) are ranking factors. Proper caching + image optimisation + minification can lift mobile scores from 40 to 80+.