# SEO Task A — Audit & Research
**Candidate:** Poovarasan MM
**Subject:** digitalheroesco.com (homepage audited)
**Date:** July 2026

---

## Part A — On-Page Audit (Homepage)

Audited page: `https://digitalheroesco.com/` (live-fetched July 24, 2026)

| # | Priority | Issue | Impact | Recommended Fix |
|---|----------|-------|--------|------------------|
| 1 | High | The H1 ("NO MORE missed deadlines. ghosting devs...") contains zero target keywords and no clear statement of what the company does. | H1 is one of the strongest on-page relevance signals for Google. A keyword-free H1 wastes the single highest-weight text element on the page. | Keep the emotional hook as a subhead/eyebrow, but make the H1 something like "Custom Software, Web & Shopify Development Agency" — literal, keyword-bearing, still bold. |
| 2 | High | Key trust stats (brands built, countries, revenue scaled, Fiverr rating) render as "0" in the base HTML and only animate to real numbers via JavaScript. | If Google's renderer (or any tool without full JS execution) reads the raw content, these trust signals — a core E-E-A-T asset — read as zero. Also breaks for the ~1-2% of crawlers/bots with limited JS budget. | Set the real final values as the initial DOM text, then animate *from* that number, not from 0. Never let the no-JS state show an empty/zero trust signal. |
| 3 | High | Inconsistent brand claims across the same page: "55+ countries" in the hero badge line vs. "40+ countries" in the chat widget section; "9-year story" (founded 2017) vs. "12 yrs shipping" elsewhere on the same page. | Contradicting stats on one page undermine trustworthiness (a direct E-E-A-T signal) and look sloppy to both users and evaluators like Google's quality raters. | Pick one verified number per stat, store it in one place (a CMS variable/global), and reference it everywhere so it can never drift. |
| 4 | Medium | Meta description is right at/over the ~155-character display limit and is written as a feature list rather than a compelling reason to click. | Descriptions over the limit get truncated in search results, often mid-word, which looks unpolished and can cut off the strongest selling point. | Rewrite to a tighter, benefit-led description under 155 characters (see rewrite below). |
| 5 | Medium | The mega-menu exposes 12 services, 32 industries, and a 315-tool hub directly from the homepage nav on every page. | Extremely wide internal linking dilutes the link equity passed to the pages that actually drive revenue (Shopify Plus, migration, core services) and can spread crawl budget thin across hundreds of low-value utility tool pages. | Keep the mega-menu for UX, but curate which links pass full crawl priority via strategic internal linking elsewhere (e.g., footer, contextual links from Journal posts) toward the 8-10 commercially important pages. |
| 6 | Medium | Testimonial quotes are attributed generically ("Founder · DTC skincare," "COO · B2B SaaS") while named case studies (Emani, Big Game Sports, Noble Paris) exist elsewhere on the same page. | Mixing fully-verified case studies with anonymous quotes on one page weakens the credibility of the stronger, named proof — reviewers and algorithms both weigh specific, attributable claims higher. | Replace generic testimonial attributions with named clients where permission exists, or clearly link each quote to its full case study. |
| 7 | Medium | Hero and process sections rely on multiple autoplaying video/animation assets (fire.mp4, three process videos, a YouTube "constellation" embed). | Heavy media early in the page is a common Core Web Vitals (LCP) risk, especially on mobile connections — and it's exactly the kind of page a competitive keyword like "shopify development agency" needs to load fast for. | Lazy-load all below-the-fold video, compress/serve the hero video in a modern codec (WebM/AV1), and confirm LCP element isn't a video frame. |
| 8 | Low | Several badge/logo images appear twice in the DOM (once with descriptive alt text, once with empty alt or repeated markup). | Duplicate image nodes add unnecessary page weight and are a minor accessibility issue (screen readers may announce the same badge twice). | Remove the duplicate render; keep one instance per badge with descriptive alt text. |
| 9 | Low | The 315-tool hub is one of the largest sections of the site by page count, but the homepage gives it minimal context beyond category labels. | Large clusters of thin utility-tool pages are a known quality-dilution risk if they're templated and low on unique content — this can drag down the perceived quality of the whole domain. | Audit the tool hub separately for thin/duplicate content; ensure each tool page has genuinely unique instructions, use-cases, and isn't just a wrapper around a generic script. |
| 10 | Low | No visible breadcrumb trail on the homepage's linked subpages (based on nav structure), despite a deep site hierarchy (services > sub-services, industries > sub-industries). | Breadcrumbs help both users and Google understand site hierarchy, and often appear in SERPs as an enhanced result, improving click-through. | Add schema-marked breadcrumbs to all deep pages (services, industries, case studies, journal posts). |

---

## Part B — Keyword Research (10 keywords, US-targeted Shopify agency)

| Keyword | Search Intent | Difficulty (judgment) | Maps to Page Type |
|---|---|---|---|
| shopify development agency | Commercial / hiring intent | High | Core service page (Shopify Development) |
| shopify plus agency | Commercial, higher-budget buyer | High | Shopify Plus service page |
| shopify migration services | Commercial, replatforming intent | Medium-High | Shopify Migration page |
| hire shopify developer | Transactional | Medium | Shopify Development page or dedicated landing page |
| shopify store redesign | Commercial | Medium | Web Design / Shopify Development page |
| best shopify agency for small business | Commercial, comparison intent | Medium | Comparison/"Best of" guide (they already have a `/best/` and `/compare/` section) |
| shopify seo services | Commercial | Medium | SEO service page |
| shopify vs woocommerce | Informational, top-of-funnel | Medium | Journal/blog comparison article |
| custom shopify theme development | Commercial, specific | Low-Medium | Shopify Development page or dedicated sub-page |
| shopify app development cost | Informational/commercial, pricing intent | Low-Medium | Pricing guide page (they already have a `/cost/` hub) |

*Difficulty judgments are directional (based on competitiveness of the term and typical SERP crowding for "Shopify agency" style queries) — worth validating with a tool like Ahrefs/Semrush before finalizing, and I'd note that as an assumption in the submission.*

---

## Part C — Title Tag & Meta Description Rewrites (3 pages)

### 1. Homepage
**Current title:** Software, Web & App Development Company | Digital Heroes
**Current meta:** Digital Heroes builds custom software, websites, web & mobile apps, Shopify stores and SaaS. Senior NY + Delhi team, 2,000+ brands shipped in 55+ countries.

**Rewrite — Title (58 chars):** Shopify, Web & Software Development Agency | Digital Heroes
**Rewrite — Meta (149 chars):** Shopify Plus, web, and custom software — built by a senior NY + Delhi team. 2,000+ brands shipped across 55+ countries. Book a call today.

### 2. Shopify Development service page
**Assumed current focus:** general Shopify development service page
**Rewrite — Title (56 chars):** Shopify Development Company | Custom Stores That Convert
**Rewrite — Meta (152 chars):** Custom Shopify stores built by a Shopify Premier Partner. From theme builds to full replatforms — senior developers, no junior hand-offs.

### 3. Shopify Plus Agency page
**Assumed current focus:** Shopify Plus-specific service page
**Rewrite — Title (54 chars):** Shopify Plus Agency | Enterprise Ecommerce Partner
**Rewrite — Meta (154 chars):** Shopify Plus Premier Partner handling checkout extensibility, replatforms, and enterprise builds. 2,000+ brands shipped — scoped quote in 48 hours.

*Assumption stated for submission: I audited the homepage directly; the two service-page rewrites are based on the site's own positioning language (Premier Partner, 48-hour quote, no junior hand-offs) pulled from the homepage FAQ, since I focused my full audit budget on one page as instructed.*

---

## AI Use Disclosure (required by brief — customize this before submitting)
*Draft note — replace with your own honest account:*
I used Claude to fetch and analyze the live homepage content, structure the audit into issue/impact/fix format, and draft a first pass at keyword and meta rewrites. I then [describe what you changed — e.g., "re-prioritized which findings mattered most based on my own read of the page," "rewrote the meta descriptions in my own voice," "added/removed keywords based on my own judgment of what a US small business would actually search"].
