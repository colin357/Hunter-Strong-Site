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

## Brand (FirstTrust Brand & Style Guidelines)
- Colors: Red `#BC242B`, Gray `#524B4B`, White, Black (tokens at the top of `assets/styles.css`).
- Type: Minion Pro (primary) and Gill Sans MT (secondary) are licensed fonts. The CSS uses them when installed and falls back to Crimson Pro and Cabin from Google Fonts. The signature uses Mrs Saint Delafield as a stand-in for "The Secret".
- Logos: `assets/firsttrust-logo.png` (primary horizontal, on white only), `firsttrust-wordmark.png`, `firsttrust-mark.png`. Don't recolor, stretch or add effects.
- Required on every page: Equal Housing Lender logo, NMLS 75271, myFTHL.com, and the FirstTrust disclaimer (all in the footer; the wording lives in `DISCLAIMER` in `_build/build.py`).
- Copy: say "can", not "will". No guaranteed approvals, and nothing that downplays credit or income requirements.

## Photos
Stock photos in `assets/img/` come from Unsplash (free under the Unsplash License, no attribution required). Swap in local photos of Hunter, his team or Arkansas homes whenever you have them.
