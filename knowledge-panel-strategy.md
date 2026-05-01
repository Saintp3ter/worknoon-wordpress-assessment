# Knowledge Panel Optimization Strategy – Worknoon

## How Worknoon can trigger or strengthen a Google Knowledge Panel

Google Knowledge Panels are automatically generated for entities with sufficient authority and trust. To trigger or strengthen one for **Worknoon**:

1. **Establish a unique, verifiable entity** – Ensure Worknoon has a distinct identity (name, logo, location, founding date, legal registration).
2. **Build authoritative references** – Wikipedia or Wikidata entry (or at least a Crunchbase/Bloomberg profile).
3. **Consistent structured data** across all owned web properties.
4. **Earn external citations** – news articles, industry directories, government listings.

If a panel does not exist, **suggest a panel** via Google’s feedback tool (but only works after entity is partially recognised). Strengthen an existing one by claiming it and adding verified details.

---

## Entity building steps

| Step | Action |
|------|--------|
| 1. **Define unique entity** | Legal name, alternate names (e.g., “Worknoon”, “Worknoon Inc.”), DBA, previous names. |
| 2. **Create authoritative profiles** | Wikipedia (if you qualify), LinkedIn Company Page, Wikidata entry, Google Business Profile (if local). |
| 3. **Publish a permanent “About” page** | URL: `/about` or `/team`. Include founder names, founding date, headquarters, mission. |
| 4. **Build external backlinks from authoritative sources** | .gov, .edu, major news outlets, industry associations. |
| 5. **Add consistent NAP+W** (Name, Address, Phone, Website) on every page’s schema. |
| 6. **Earn knowledge graph citations** – Get mentioned in Wikipedia references or trusted databases (e.g., LinkedIn, Wikidata). |
| 7. **Use Google’s “suggest a panel”** – in search results when you see a partial panel. |

---

## Schema requirements

Implement at minimum these schema types on Worknoon’s homepage and /about page:

- **Organization schema** – required properties: `name`, `url`, `logo`, `sameAs`.
- **LocalBusiness** (if physical location) or **Corporation** subtype.
- **ContactPoint** – email, phone, contact option.
- **sameAs** – include all verified social profiles (LinkedIn, Twitter, Crunchbase, Wikipedia).

Example snippet:

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Worknoon",
  "url": "https://www.worknoon.com",
  "logo": "https://www.worknoon.com/logo.png",
  "foundingDate": "2018",
  "founder": { "@type": "Person", "name": "Founder Name" },
  "sameAs": [
    "https://www.linkedin.com/company/worknoon",
    "https://twitter.com/worknoon",
    "https://www.crunchbase.com/organization/worknoon"
  ],
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "customer support",
    "email": "hello@worknoon.com"
  }
}