# Hunter Strong – Personal Loan Officer Site

Static site for Hunter Strong, Loan Officer, FirstTrust Home Loans (NMLS #1911747).

## Edit & rebuild
All content and facts live in `_build/build.py` (CONFIG block at the top, page copy below it).

```
python3 _build/build.py
```

This regenerates `index.html`, every page folder, `404.html`, `sitemap.xml`, `robots.txt` and `llms.txt`.

## Before launch
1. Set `SITE` in `_build/build.py` to the real domain (currently a placeholder: `https://www.hunterstrongloans.com`) and rebuild.
2. Get compliance sign-off from FirstTrust Home Loans (personal LO sites usually need approval).
3. Submit `sitemap.xml` in Google Search Console and Bing Webmaster Tools (Bing feeds ChatGPT/Copilot search).

## AEO features
- Answer-first "short answer" block on every page (quotable, self-contained)
- JSON-LD graph: Person (NMLS credential, areaServed, knowsAbout, sameAs), FinancialService, Organization, Service, FAQPage, BreadcrumbList, ProfilePage
- Consistent NAP + NMLS on every page, linked to NMLS Consumer Access
- `llms.txt` fact sheet for AI crawlers; `robots.txt` explicitly allows GPTBot, ClaudeBot, PerplexityBot, Google-Extended, etc.
- State pages (AR, MS, TN) and program pages that target "loan officer in [state]" and "[loan type]" questions
- Visible FAQs that mirror the FAQ schema

Deploys as-is to any static host (Vercel, Netlify, GitHub Pages, Cloudflare Pages).
