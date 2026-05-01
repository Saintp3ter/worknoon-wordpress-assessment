# Worknoon WordPress Assessment

## Project Overview
This is a functional WordPress landing page built for the Worknoon WordPress Developer (SEO + Systems Specialist) assessment.  
The page includes:
- Hero section with CTA
- Services section
- Testimonials
- Contact form
- Mobile responsive design
- Page speed optimizations
- Google Analytics integration

**Live demo video:** [Your Video Link Here]  
**GitHub repo:** [Link to this repo]

---

## Setup Instructions

### Prerequisites
- Local WordPress environment (LocalWP / XAMPP / MAMP) or live server.
- WordPress 6.x or higher.
- PHP 7.4+.

### Installation steps
1. Clone this repository (but note: WordPress core is not included – only custom documentation/schema).
2. Install a fresh WordPress site.
3. Install and activate the following plugins:
   - Elementor (free)
   - Contact Form 7 or WPForms Lite
   - Site Kit by Google (for analytics)
   - (Optional) WP Super Cache + Autoptimize for speed
   - (Optional) Rank Math SEO or Schema Pro for structured data
4. Import the Elementor template from `/export/elementor-template.json` (if provided) or rebuild manually using the sections described below.
5. Set your homepage to the landing page (Settings → Reading).
6. Configure Google Analytics via Site Kit (connect your GA4 property).
7. Add the custom JSON-LD schema (see below) via a plugin like "Insert Headers and Footers".

### Alternative manual build
- Create a new page using Elementor.
- Add Hero, Services, Testimonials, Contact Form widgets as shown in the video.
- Ensure responsive settings (mobile, tablet).

---

## Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| WordPress 6.4 | CMS |
| Elementor (Free) | Page builder |
| Contact Form 7 | Contact form |
| Site Kit by Google | Google Analytics integration |
| Astra Theme | Lightweight base theme |
| WP Super Cache + Autoptimize | Caching & minification |
| TinyPNG + Smush | Image compression |
| Rank Math SEO | Schema markup (alternative to manual JSON-LD) |
| Git | Version control |
| Loom | Demo recording |

---

## SEO & Schema Explanations

### Structured Data Added
I implemented **Organization** and **Testimonial** schema to improve search visibility.

**Organization schema** (JSON-LD):
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Worknoon Assessment Demo",
  "url": "http://localhost/worknoon",
  "logo": "http://localhost/worknoon/wp-content/uploads/logo.png",
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "customer service",
    "email": "demo@worknoon.com"
  }
}