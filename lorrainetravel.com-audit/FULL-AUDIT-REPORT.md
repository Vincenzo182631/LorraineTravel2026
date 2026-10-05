# SEO Audit: lorrainetravel.com
Date: 2026-10-05 · Business type: Local Service / luxury travel agency (brick-and-mortar, Coral Gables FL) with editorial content

**Scope & method (read first):** The bundled renderer refused this sandbox's proxy, so the audit uses raw HTML fetched with curl from `www.lorrainetravel.com`: homepage, robots.txt, sitemap.xml, llms.txt and all 36 sitemap URLs. Not covered: JS-rendered content, Lighthouse/CWV lab or field data, screenshots, backlinks, Google API data, GBP/citations. Specialist subagents were not spawned. Scores are estimates from the evidence below.

## SEO Health Score: ~78 / 100

| Category (weight) | Score |
|---|---|
| Technical SEO (22%) | 74 |
| Content Quality (23%) | 80 |
| On-Page SEO (20%) | 70 |
| Schema (10%) | 90 |
| Performance (10%) | not measured (TTFB 0.15-0.55s, HTML 57 KB: good) |
| AI Search Readiness (10%) | 92 |
| Images (5%) | 80 |

## Top issues
1. **High: apex HTTPS fails from this sandbox.** `https://lorrainetravel.com` returns a TLS handshake failure (`sslv3 alert handshake failure`); `http://` 301s to `https://www`. `https://www` works. Could be sandbox-specific, so verify from a normal network. If real, anyone typing or linking the bare domain over HTTPS gets an error and link equity is lost.
2. **High: 9 destination pages share the meta description** "Editorial travel guide written by Lorraine Travel advisors." (59 chars, also used as og:description). Weak snippet and no keyword/intent signal for the pages most likely to rank for travel queries.
3. **Medium: no security headers.** No HSTS, CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy or Permissions-Policy in the homepage response.
4. **Medium: meta descriptions too long** on 14 of 36 pages (>160 chars, up to 245 on `/cruises`); will be truncated in SERPs.
5. **Medium: titles over ~60 chars** on 15 pages (up to 89 on the Orient Express post), including the homepage (75).
6. **Low: 2 homepage images have no alt text** (and 1-2 on most pages with images). `/resources/*` pages 251-464 words; `/resources/climate` (251) is thin.

## What works
- Clean indexability: all 36 URLs return 200, self-referencing canonicals everywhere, one H1 per page, no duplicate titles, `robots: index, follow, max-image-preview:large`, proper 404 status for missing pages.
- robots.txt allows all and explicitly welcomes GPTBot, ClaudeBot, PerplexityBot, Google-Extended and others; sitemap is declared, valid, and has 36 URLs with lastmod.
- Schema is rich and appropriate: Organization, TravelAgency, LocalBusiness-style Place/GeoCoordinates/OpeningHours, WebSite+SearchAction, FAQPage, Offer on the homepage; Article + BreadcrumbList on guides.
- `llms.txt` present with address, phone, affiliations, specialties.
- Fast: 0.15-0.55s response, 57 KB homepage, 14 of 16 images lazy-loaded.
- Strong E-E-A-T on the homepage: 1948 founding, family ownership, Four Seasons Preferred Partner, Signature Travel Network and ASTA membership, named people.

## Technical SEO
- No redirect chains seen on www; http→www 301 works.
- Sitemap `lastmod` is 2026-10-05 for every URL: looks auto-stamped to the build date, so it gives crawlers no change signal. Set it to real modification dates.
- `changefreq`/`priority` are ignored by Google; harmless.
- No hreflang (single English site: fine).

## On-Page
- Homepage title: "Lorraine Travel — Luxury Travel Advisors Since 1948 | Coral Gables, Florida" (75 chars). Shorten, e.g. "Lorraine Travel | Luxury Travel Advisors Since 1948" (50).
- Destination guides are 353-455 words each: on the light side for pages competing on "best hotels Paris", "luxury Maldives". See Action Plan.

## Local SEO (partially assessed)
NAP is consistent in llms.txt and homepage schema. Not verified: Google Business Profile, reviews, third-party citations. Recommend a separate `/seo-local` run.

## Not assessed
Core Web Vitals (INP/LCP/CLS), JS rendering, mobile screenshots, backlink profile, Search Console data, internal link graph beyond the homepage's 30 links.
