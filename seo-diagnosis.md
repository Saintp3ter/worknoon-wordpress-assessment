# SEO Technical Troubleshooting – Worknoon website not indexing

**Scenario:** A new Worknoon website is not indexing even after sitemap submission.

## 1. Crawlability tests

- **Check robots.txt** → `worknoon.com/robots.txt`  
  Ensure `User-agent: *` and `Disallow:` directives don’t block important paths.  
  Test with Google’s robots.txt tester in Search Console.

- **Check HTTP headers** (use `curl -I` or browser dev tools)  
  Look for `X-Robots-Tag: noindex` or `noarchive`.  
  Also verify status 200 (not 301/302 redirect loop, not 404).

- **Fetch as Google** (Search Console → URL Inspection)  
  Request indexing and see if Googlebot can access the page. Check `Page Fetch` status.

- **Internal linking** – Is the homepage linked from any external source? Without any backlinks, Google may not discover pages even with sitemap.

---

## 2. Canonical checks

- **Check canonical tags** in `<head>` of the homepage and a few inner pages.  
  Use `view-source:` to look for `<link rel="canonical" href="...">`.  
  - If canonical points to a different URL (e.g., `/home` vs `/`), Google may ignore your submitted URL.
  - Avoid self‑referencing canonicals that differ by trailing slash or `www` vs non‑`www`.

- **Multiple versions of the site** – enforce one version via 301 redirect (e.g., redirect `http://` to `https://` and `www` to non‑www or vice versa) to consolidate canonical signals.

---

## 3. Robots.txt & no-index audit

- **Check robots.txt** for accidental blocks:  