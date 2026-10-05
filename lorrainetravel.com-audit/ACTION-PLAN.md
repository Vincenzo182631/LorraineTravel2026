# Action Plan: lorrainetravel.com

## Critical
- None found in the evidence collected.

## High (within 1 week)
1. **Verify and fix apex HTTPS** (`https://lorrainetravel.com`). Test from a normal network (`curl -I https://lorrainetravel.com`). If it fails, add the apex to the Cloudflare certificate/SSL setup and 301 it to `https://www`.
2. **Write unique meta descriptions for the 9 `/destinations/*` guides** (120-155 chars each, destination + hook), and update og:description to match.

## Medium (within 1 month)
3. Add security headers (Cloudflare Transform Rules or the app): `Strict-Transport-Security`, `X-Content-Type-Options: nosniff`, `Referrer-Policy: strict-origin-when-cross-origin`, `X-Frame-Options`/CSP `frame-ancestors`, `Permissions-Policy`.
4. Trim meta descriptions to <=155 chars on `/`, `/about`, `/luxury-vacations`, `/cruises`, `/hotels`, `/destinations`, `/compare`, `/contact`, `/corporate`, `/app` and the 4 blog posts.
5. Trim titles to <=60 chars on the 15 pages flagged (homepage first).
6. Make sitemap `lastmod` reflect real content changes.
7. Add alt text to the images missing it (2 on the homepage).

## Low (backlog)
8. Expand `/resources/climate` and the destination guides toward 800+ words with specifics (seasons, properties, itineraries, advisor commentary).
9. Run `/seo-local`, `/seo-google` (needs credentials) and a Lighthouse/CWV check; this audit did not cover them.
10. Add more blog posts and link them from destination guides (only 4 posts in the sitemap).
