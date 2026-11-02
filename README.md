# Lotus Colour World — Website

Production-ready static website for **Lotus Colour World**, a hardware, paint and
bathroom-supply store at Patel Complex, Right Bhusari Colony, Kothrud, Pune 411038.

Built and prepared by **DEVANSHVERSE**.

---

## Contents

```
index.html                  Single-page site (Hero, About, Products, Visit, Contact)
styles.css                  Design system + responsive layout
script.js                   Mobile nav, sticky header, scroll reveal (progressive enhancement)
robots.txt                  Crawler rules
.nojekyll                   Disables Jekyll processing on GitHub Pages
sitemap.xml                 Sitemap for search engines
```

No build step, no dependencies, no framework. Upload and it runs.

---

## Source of business information

Every factual detail on this site comes from the business's **public Google Business
Profile** at the time of generation. Nothing was invented.

| Field | Value | Source |
| --- | --- | --- |
| Business name | Lotus Colour World | Google Business Profile |
| Categories | Hardware store · Bathroom supply store · Paint store | Google Business Profile |
| Address | Shop No. 1, Patel Complex, Right Bhusari Colony, Kothrud, Pune 411038 | Google Business Profile |
| Phone | +91 95611 94243 | Google Business Profile |
| Rating | 4.0 from 75 reviews | Google Business Profile |
| Coordinates | 18.508744, 73.790853 | Google Business Profile |

### Deliberately omitted

These were **not** available and were therefore left out rather than invented:

- Opening hours per day (only "opens 9 AM" was listed, not a full week)
- Prices, product brands, stock levels
- Testimonials, awards, years in business, staff names
- Any claim about quality, speed or guarantees

The Products section describes the three listed Google categories in plain language and
tells the visitor to call and confirm stock. That is intentional: it stays useful without
asserting facts the store has not confirmed.

---

## To confirm with the store before publishing

1. **Phone number** — confirm +91 95611 94243 is the current, preferred number.
2. **WhatsApp** — confirm the number receives WhatsApp before keeping the WhatsApp CTA.
   Remove the `.cta-note` line in `index.html` once confirmed.
3. **Opening hours** — send a weekly schedule and it can replace the "timings vary" copy.
4. **Brands stocked** — optional; would let the Products section name real brands.
5. **Photographs** — a shopfront and interior photo would materially improve the hero.

---

## Run locally

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

---

## Deploy

Hosted on **GitHub Pages**, deploying straight from the `main` branch. No build step,
no CI secrets, no hosting account required.

| | |
| --- | --- |
| Repository | https://github.com/DEVZONE940/lotus-colour-world |
| Live URL | https://devzone940.github.io/lotus-colour-world/ |
| Source | `main` branch, repository root |
| Jekyll | Disabled via `.nojekyll` |

### Redeploying after an edit

```bash
git add -A
git commit -m "Update site content"
git push origin main
```

GitHub Pages rebuilds automatically. A build usually completes in under a minute.

### Using a custom domain later

1. Add the domain in the repository's Settings → Pages → Custom domain.
2. Point a `CNAME` record at `devzone940.github.io`.
3. Tick "Enforce HTTPS" once the certificate is issued.
4. Update `canonical`, `og:url` in `index.html` and `sitemap.xml` to the new domain.

### Any other static host

The folder is plain HTML/CSS/JS, so it also drops onto Netlify, Cloudflare Pages,
Vercel or nginx unchanged.

## Post-deployment checklist

- [ ] Live URL returns HTTP 200 and renders the site
- [ ] Phone link opens the dialler on a real phone
- [ ] WhatsApp CTA confirmed by the store
- [ ] Map embed loads on both desktop and mobile
- [ ] Mobile nav opens and closes correctly at 390px width
- [ ] Lighthouse mobile score checked
- [x] `og:url`, `canonical` and `sitemap.xml` set to the live URL
- [ ] Submitted to Google Search Console with a sitemap

---

## Accessibility and performance notes

- Semantic landmarks, skip link, visible focus rings, labelled controls.
- Respects `prefers-reduced-motion`.
- Zero JS required for content, navigation or contact.
- Fonts loaded with `display=swap`; only two families, four weights total.
- Map iframe is lazy-loaded and the only third-party embed.

---

© Lotus Colour World. Prepared as a proposal by DEVANSHVERSE.
