# Site Building Project — CLAUDE.md

ebeetles is building a series of free websites for small local businesses in the San Francisco Bay Area (primarily San Jose, Mountain View, Sunnyvale, Palo Alto) that lack an online presence — approaching businesses cold and offering the service.

The overarching goal is honest, distinctive design that reflects each specific business rather than producing templated, generic sites. ebeetles explicitly pushes back on "AI slop" defaults and expects design choices to be justified with specific reasoning.

## Key Design Principles

- **Each site needs a genuine concept, not a layout variation** — the concept should emerge from what makes that specific business distinctive (review themes, history, owner identity, physical context)
- **No font or palette reuse across sites** — differentiation is tracked deliberately across the growing series
- **Missing physical presence changes design metaphors** — businesses without storefronts (e.g., mobile services) require different spatial and trust-building approaches
- **Reviews and real-world details are primary content** — treat review-based stories as structural elements (styled as ticket cards, logbook entries, etc.) rather than generic testimonials carousels
- **Verify before committing** — do not assume a domain with an active-looking URL actually has a live site. Verify owner names, addresses, and other details
- **Website pitch angle matters** — for owner-operated businesses with strong word-of-mouth, frame a site as an operational tool (answering repetitive calls, freeing reputation from Yelp) rather than a marketing play

## Lead Types — Two Tracks

**Cold Call Leads** (Leads tab) — phone calls only. Source can be ANYTHING: Google Maps, directories, Yelp, web search. No email or website needed. Photos don't matter for these. Google Maps browser is now accessible via Playwright if extraction is needed.

**Email Leads** (Email Leads tab) — getting websites built. These MUST have an email and NO existing website. Nextdoor is the ideal source because it exposes emails + has real business photos + lets us verify "no website" status in one place. All email leads are found through Nextdoor.

## Workflow

1. Receive a brief: business name, type, phone, email, location, and any known differentiators
2. Research the business via web search (Nextdoor for email leads, any source for cold call leads)
3. **Photo extraction** — if the business has a Nextdoor page, browse it and extract real business photos (storefront, interior, work samples). Then save them to the site directory. Nextdoor photo URLs are directly accessible (200 OK, no auth needed). See `/home/elwin/Sites/extract-nextdoor-photos.py` for the extraction script.
4. Design a unique concept inspired by what makes that business distinctive
5. Build the complete single-page HTML site — use **real Nextdoor photos** when available (prefer over Unsplash stock)
6. All work outputs go to the site's directory under `/home/elwin/Sites/[site-name]/`
7. The site directory already exists when you start — write `index.html` and any supporting files there

## Build Requirements

- Mobile-first, fully responsive single HTML file
- All CSS inline (no external files)
- **Photo priority: 1) Real Nextdoor biz photos in the site directory 2) Google Maps extracted photos 3) Unsplash as last resort only** — do NOT default to stock Unsplash images without checking for real photos first
- Sticky bottom call bar with phone number as a real `tel:` link
- Fonts: Google Fonts via @import
- No JavaScript frameworks — vanilla JS only if needed
- Mark every unconfirmed fact with `[placeholder]` — do not fabricate
- SEO meta tags, Open Graph tags
- Accessibility: proper heading hierarchy, alt text on all images, aria labels on CTAs
- Preferred-reduced-motion respected
- Deploy to Vercel ready (no build step needed)

## Deployment

- GitHub account: `ebeetles`
- Auth: Token-based HTTPS (token set via environment variable `GITHUB_TOKEN`)
- Vercel team scope: `elwin-s-projects2`
- Vercel token set via environment variable `VERCEL_TOKEN`
- After building `index.html`, run: `git init -b main && git add -A && git commit -m "Initial commit" && git remote add origin https://ebeetles:$GITHUB_TOKEN@github.com/ebeetles/[site-name].git && git push -u origin main`
- Then: `vercel deploy --token "$VERCEL_TOKEN" --scope "elwin-s-projects2" --name "[site-name]" --yes .`

## Completed Sites (Design Concepts)

Previous work includes specs for:
- A&L Pure Water — "Corner store, done beautifully"; light warm palette, DM Serif Display + Inter
- M&S Watch Repair — "The Watchmaker's Bench"; near-black warm palette, Cormorant Garamond + Spectral + Inter
- Say Ray Foreign Auto Service — "1959" concept built around founding year; warm parchment tones, Crimson Pro + Source Sans 3
- Souren Master Shoe Repair — "The Repair Counter"; claim-ticket/workbench metaphor, Special Elite or Courier Prime
- Peninsula Auto Repair — "The Diagnostic Bay"; cool dark palette, Space Grotesk + IBM Plex Mono + IBM Plex Sans
- Fred's Watch and Jewelry Repair — "While You Wait"; Fraunces + Hanken Grotesk + DM Mono
- Salga2 Complete Auto Repair — "The Straight Answer"; warm concrete grey + charcoal-navy + safety amber, Barlow Condensed + Work Sans + DM Mono
- Vivace Piano Service — "The House Call"; walnut-and-aged-brass palette, Lora + Karla, "Logbook" review section
