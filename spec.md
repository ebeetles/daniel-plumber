# Design Spec — Daniel's Plumbing & Handyman

## Thesis
Daniel is a one-man operation — plumber *and* handyman — who neighbors describe as "efficient, friendly, super honest, and very reasonable." His business lives on Nextdoor referrals alone. The site needs to bottle that word-of-mouth trust into a page that feels like a friend texting you a number. No fake testimonials — just real neighbor praise and a dead-simple way to reach him.

Single audience: San Jose homeowner with a clogged drain, leaky faucet, or simple repair.
Single job: Call (408) 624-2095.

## Design Tokens

### Color
| Name | Hex | Role |
|------|-----|------|
| Deep Blue | `#0A1628` | Primary background |
| Navy | `#142444` | Card/section surfaces |
| Steel Blue | `#2A4A7F` | Borders, accents |
| Pipe Copper | `#D4764A` | Hero accent — warm, metallic, plumbing-adjacent |
| Off White | `#F0F4F8` | Primary text |
| Muted | `#8899B0` | Secondary text |

Copper is the signature move — it's a material every homeowner associates with plumbing, but used as a UI accent color (CTAs, icons, headline underlines). Subconscious "this person knows pipes."

### Type
| Role | Face | Notes |
|------|------|-------|
| Display | **Space Grotesk** (600/700) | Modern, slightly technical feel |
| Body | **Inter** (400/500) | Clean, highly legible |
| Utility | **JetBrains Mono** (400) | Phone number, hours, rate info |

### Layout
Single column, mobile-first. Hero: copper-tinted photo of plumbing work or tools. Value prop under it: "Honest plumbing. Fair prices. No surprises." → Services list (plumbing + handyman) → "What neighbors say" section → Contact with big phone button. Sticky bottom bar always visible.

```
┌──────────────────────────┐
│ DANIEL   📞 Call       │
├──────────────────────────┤
│ [Hero: copper pipes /    │
│  wrench photo]           │
│                           │
│ Honest Plumbing.          │
│ Fair Prices.              │
│ No Surprises.             │
├──────────────────────────┤
│ 🛠 Plumbing               │
│ 🏠 Handyman               │
│ → Drain cleaning          │
│ → Faucet repair           │
│ → Pipe fixes              │
│ → Drywall                 │
│ → Assembly                │
├──────────────────────────┤
│ "Efficient, friendly,     │
│  super honest"            │
│  — Nextdoor neighbors     │
├──────────────────────────┤
│ 📍 San Jose, CA           │
│ 📞 (408) 624-2095         │
├──────────────────────────┤
│ [STICKY: TAP TO CALL   │
│  (408) 624-2095]         │
└──────────────────────────┘
```

## Content
- **Business:** Daniel's Plumbing & Handyman Service
- **Owner:** Daniel
- **Phone:** (408) 624-2095
- **Email:** plumbingmaster8@gmail.com
- **Location:** San Jose, CA (Leigh Ave area)
- **Services:** Plumbing repairs, drain cleaning, faucet installation, pipe repair, drywall patching, furniture assembly, general handyman
- **Hours:** Open until 8:00 PM (verify)
- **Tone:** Straightforward, neighborly, no-upsell. "Call Daniel. He'll fix it right the first time."
- **Unsplash keywords:** copper pipes, plumbing tools, wrench, plumbing repair, modern kitchen faucet
