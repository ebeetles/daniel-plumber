# "The Running List"
## Design Spec — Daniel Plumbing & Handyman

---

### Concept

**The insight:** Every Bay Area homeowner has one. A sticky on the fridge, a note in their phone: *dripping faucet. garbage disposal. cabinet hinge. toilet running. screen door off the track.* Some items are plumbing. Some are handyman. Most people file this list under "eventually" because sorting out who handles which item, and then calling two different people, feels like more work than the problems themselves.

Daniel removes that friction entirely. He's both a plumber and a handyman — which means one call clears the whole list. The site should make this immediately visceral, not explain it. The hero is not a tagline with a stock photo. The hero IS the list — job line items, already checked off in green. Not "here's what Daniel can do." Here's what Daniel has already done, for someone exactly like you.

**Why this concept fits Daniel specifically:**

1. **The dual trade is the product.** Most residential tradespeople specialize. The "running list" metaphor makes the dual-trade value self-evident without needing to argue for it. You see a list of mixed plumbing + handyman jobs, all checked — and you immediately understand.

2. **Nextdoor-only referrals means every job earns the next.** This is not a guy who advertises. He survives entirely on neighbor-to-neighbor trust. The "cleared list" visual shows the outcome of that trust rather than claiming it. No testimonial carousel, no star-rating badge. The work speaks for itself as work-order records.

3. **No storefront — the site is his trust anchor.** When a neighbor says "call Daniel," this site is what you find. It needs to signal competence and specificity immediately — not look like another generic contractor site. The work-order visual grammar does that instantly: this is a person who tracks jobs, shows up, and finishes things.

---

### Design Tokens

**Palette:**

| Token | Value | Justification |
|-------|-------|---------------|
| `--bg` | `#F7F8FA` | Almost white with a faint cool cast — fresh clipboard paper, not warm artisan parchment. Every warm-toned palette in this series has been used. The cool break is deliberate. |
| `--ink` | `#111827` | Near-black with a blue undertone. Printer ink. Reads as text that belongs on a form. |
| `--blue` | `#1A56DB` | Clear, reliable, zero warmth. Bay Area sky. Water running through a clean pipe. Municipal confidence. This is not a design-trend blue — it's the color of something official being resolved. |
| `--blue-fill` | `#EFF6FF` | Checked-item backgrounds and hover states. Keeps the blue accent from overloading. |
| `--green` | `#059669` | The "done" signal. Checkmarks are this color throughout — they appear before anything else on load. Green is universally task-completion. |
| `--green-fill` | `#ECFDF5` | Paired fill for green elements. |
| `--gray` | `#6B7280` | Category labels, service tags, metadata. Recedes appropriately. |
| `--border` | `#E5E7EB` | The ruled lines on the form. Barely there. |
| `--amber` | `#D97706` | Handyman category label text color. |
| `--amber-fill` | `#FFFBEB` | Handyman tag background. |

**Typography:**

| Role | Face | Justification |
|------|------|---------------|
| Display | **Bitter** (slab serif) | When you look at an actual work order or service receipt, the type is a slab or condensed sans — printed for speed and trust, not beauty. Bitter has that authority. Sturdy stroke contrast, confident weight. Not used elsewhere in the series. Not chosen for elegance. Chosen because it fits a clipboard. |
| Body | **Plus Jakarta Sans** | Clean humanist sans. Contemporary without being tech-bro. Reads quickly on mobile, which is where most callers will land. Not used in this series. |
| Detail | **JetBrains Mono** | Small monospace for category tags (PLUMBING / HANDYMAN), used like a typewriter label. Reinforces the form/data-entry feeling without the manual typewriter affect of Special Elite (already used on Souren). |

**Type Scale:**
- H1: Bitter 700, 3rem / 1.1 line-height (desktop), 2.2rem (mobile)
- H2: Bitter 600, 1.75rem
- H3: Bitter 600, 1.125rem
- Body: Plus Jakarta Sans 400, 1rem / 1.65 line-height
- Tags/labels: JetBrains Mono 500, 0.7rem, uppercase, letter-spacing 0.08em

**Layout:**

Desktop hero: two-column, 55/45 split. Left: eyebrow + headline + checked list + CTA. Right: plumbing photo, clipped with slight border-radius (8px). The photo is supporting context — the list is the hero.

Mobile: single column, photo appears as a contained image block above the list. List items span full width.

Ruled lines: thin 1px `--border` borders bottom each list row, exactly like a form.

**Signature element:** The pre-checked hero list. Six job line items — alternating plumbing and handyman — rendered with green ✓ checkmarks, job descriptions, and inline category tags. On page load, each checkmark pops in with a 120ms staggered delay (the satisfaction of watching a list get cleared). This is the one animated moment; everything else is static.

---

### Content Outline

1. **Nav** — "Daniel" wordmark left, phone number link right
2. **Hero** — Eyebrow (Plumbing · Handyman · Silicon Valley) + H1 + checked list + CTA button
3. **The Difference** — Three-sentence paragraph explaining why plumber + handyman together matters
4. **The Full List** — Two-column service list: Plumbing / Handyman. Styled as form line items, not a bulleted grid.
5. **The Neighborhood Keeps Calling Back** — Three job-record cards (Nextdoor context explained, no fake quotes)
6. **Reach Daniel** — Big phone number as CTA, area served, Nextdoor note
7. **Sticky call bar** — Fixed bottom, persistent on mobile

---

### Photo Direction

**Hero photo** — Unsplash ID: `1504328345606`
A tradesperson working on a pipe in a wall. Shows actual work in progress. Not a posed portrait, not a stock-photo handshake. Alt text: "Plumber working on residential pipe installation." Right column on desktop, contained block above list on mobile.

**Services section accent** — Unsplash ID: `1562259929`
Organized toolkit display. Used as a contained image in the services section, visually grounding the "handyman" column. Shows the range of tools — wrenches, levels, drills — which speaks to the dual-trade without captioning it. Alt text: "Organized handyman toolkit with wrenches, levels, and hand tools."

**Photo treatment:** Both photos at object-fit: cover, no filters, no overlays. The design earns its identity through type and layout, not photography treatment.
