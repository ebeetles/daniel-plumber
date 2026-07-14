# Design Spec — Daniel's Plumbing & Handyman Service

## Concept: "The Running List"

Every home has one. Not written anywhere, just real: the kitchen drain that's getting slow, the faucet that drips, the drywall patch that's been three weeks from "getting done." Most homeowners let the list grow because they don't know who to call first — is this a plumber job or a handyman job? Two calls. Two quotes. Two trips.

Daniel eliminates that friction entirely. He is the plumber-and-handyman — one person who figures out which hat to put on once he sees the job. The site IS the list. Services rendered as a clean work-order document — already crossed off for a hundred San Jose homes, ready for yours. The visual language is the form you'd hand a trusted tradesman: precise, legible, no-frills. Not a brochure. A record of work done.

Why this fits Daniel specifically:
- His business is built on Nextdoor referrals — the neighbor who texts you his number already trusts him. The site just needs to confirm what they said.
- The "both plumber AND handyman" differentiator is the story. Most service sites hide this under a generic "services" section. Here it IS the structure.
- The work-order metaphor conveys competence without bragging — it's the confidence of someone who doesn't need to sell you, just show you what he does.

---

## Design Tokens

### Color

| Name | Hex | Role | Justification |
|------|-----|------|---------------|
| Warm Paper | `#F1EFE8` | Main background | Like actual copy paper — warm, not bright. Grounding the "document" metaphor. |
| Ink | `#1A1916` | Primary text, hero bg, contact bg | Near-black with warm undertone. Ink on paper — the obvious pair. |
| Pencil | `#6B6860` | Secondary text | The grey of pencil marks — supporting but not competing. |
| Rule | `#CCC9C0` | Dividers, table rules | Like ledger lines. Thin, present, functional. |
| Copper | `#B5611D` | Accent, checkmarks, CTA | True plumbing copper — the material that runs through every home. Only warm chromatic color. Subconscious trust signal. |
| Copper Light | `rgba(181,97,29,.08)` | Subtle section tint | Very faint wash for emphasis sections. |
| Check Green | `#3A7A4E` | Done-state indicators | The relief of a completed item. Used sparingly — just the service checkmarks. |
| Off-Paper | `#E8E6DE` | Services section bg | Slightly darker than main paper — the "form" reads as a bounded document. |

### Typography

| Role | Face | Weight | Justification |
|------|------|--------|---------------|
| Display | **Playfair Display** | 600, 700 | Serif authority without formality. Conveys craft and trust — the kind of type on a well-made invoice or a lawyer's business card. Never used in this series. |
| Body | **Instrument Sans** | 400, 500, 600 | Clean, modern, highly legible at small sizes. Functional without feeling tech-ish. Never used in this series. |
| Utility / Numbers | **Roboto Mono** | 400 | Phone number, hours, the "precise" information deserves monospace precision. Never used in this series. |

No palette overlap with completed sites. No font overlap with completed sites.

### Layout

Single column, max 600px, lots of breathing room. Not a dense information site — the restraint IS the confidence.

```
┌─────────────────────────────────┐
│ DANIEL              [Call Now] │  ← sticky header
├─────────────────────────────────┤
│ [Photo: plumber at work]        │
│  with dark ink overlay          │
│                                 │
│  "One call handles              │  ← Playfair Display 700
│   the whole list."              │
│  San Jose · Plumbing & Handyman │
│  [Call (408) 624-2095]          │
├─────────────────────────────────┤
│ Every job earns the next one    │  ← Value props, 3-col desktop
│  Straight answers               │
│  One person shows up            │
│  Fair pricing                   │
├─────────────────────────────────┤
│ ╔═══════════════════════════╗   │  ← Work order document
│ ║ SERVICES · WORK ORDER     ║   │
│ ╠═══════════════╦═══════════╣   │
│ ║ PLUMBING      ║ HANDYMAN  ║   │
│ ╠═══════════════╬═══════════╣   │
│ ║ ✓ Drain clean ║ ✓ Drywall ║   │
│ ║ ✓ Faucet rep  ║ ✓ Assembl ║   │
│ ║ ✓ Pipe repair ║ ✓ Repairs ║   │
│ ╚═══════════════╩═══════════╝   │
├─────────────────────────────────┤
│ What neighbors say              │  ← 1-2 quote blocks
│  "Efficient, friendly,          │
│   super honest, very reasonable"│
├─────────────────────────────────┤
│ [Dark section]                  │  ← Contact
│  (408) 624-2095   ← huge serif  │
│  Daniel answers his own phone.  │
│  email · hours · location       │
├─────────────────────────────────┤
│ [STICKY: TAP TO CALL]           │
└─────────────────────────────────┘
```

---

## Content

- **Business:** Daniel's Plumbing & Handyman Service
- **Phone:** (408) 624-2095
- **Email:** plumbingmaster8@gmail.com
- **Location:** San Jose, CA (Leigh Ave area)
- **Services — Plumbing:** Drain cleaning, faucet repair & installation, pipe repair, toilet & fixture repair, general plumbing
- **Services — Handyman:** Drywall patching, furniture assembly, small home repairs, general handyman
- **Hours:** Available until 8:00 PM daily
- **Tone:** Quiet confidence. A tradesman who doesn't need to sell you — he just shows you what he does.
- **Key message:** You don't need to figure out if it's a plumbing job or a handyman job. Call Daniel. He figures it out.

---

## Photo Direction

Primary (hero): Unsplash `photo-1504328345606-18bbc8c9d7d1`
- Plumber at work — practical, authentic
- Verified live URL

Secondary (optional, services area or not used): Unsplash `photo-1585771724684-38269d6639fd`
- Plumbing tools
- Verified live URL

Approach: Dark ink overlay (opacity 0.65) over the hero image so the text reads cleanly on the warm-dark background. The photo adds texture and credibility — you see real work happening — without overwhelming the type.
