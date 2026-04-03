# es.tandemtheory.com — Project Recap

**Date**: April 3, 2026
**Project**: Mexican Spanish transcreation of tandemtheory.com
**Target URL**: es.tandemtheory.com
**Repo**: https://github.com/mikemccartin/es-tandemtheory
**Hosting**: Vercel (pending setup)

---

## What was built

A complete Mexican Spanish (es-MX) version of the Tandem Theory website, **transcreated** — not translated — for the Mexican business market. Every piece of copy was culturally adapted to read as if it were originally written by a native Mexican copywriter for Mexican business decision-makers.

---

## Steps completed

### 1. HTML sync with live WordPress site
The English HTML prototype (v2) had drifted from the live WordPress site. Before transcreating, we synced:
- **Technology section** overhauled — removed partner ecosystem grid, replaced with standalone Tandem Technology Suite (EDWARD, BEAM, Inspect, Edison, Missing-Link, Sentinel, Recon, Pulse, FMT, DCO)
- **Section title**: "Marketing Intelligence at Your Command" → "Tandem Technology Suite"
- **Section subtitle**: Updated to "Built by marketers, for marketers—to fill the gaps your platforms leave behind"
- **EDWARD category**: "AI Operations Platform" → "AI Workflow Platform"
- **AI Agents stat**: "150+" → "100s AI Agents/Tools/Skills/MCPs Built"
- **Insights page**: Added 2 new articles (April 3 and March 27, 2026)

### 2. Transcreation agent created
Built a 917-line specialized agent (`creative-transcreation-localization.md`) with deep Mexican Spanish expertise. See "The Agent" section below.

### 3. Full site transcreation
Used the agent to transcreate every page and article into Mexican Spanish.

### 4. GitHub repo + Vercel pipeline
Created `mikemccartin/es-tandemtheory` repo, committed, and pushed. Ready for Vercel import.

---

## Files delivered

### Core pages
| File | Description |
|------|-------------|
| `index.html` | Full homepage — hero, about, technology suite, services, results/testimonials, contact, footer |
| `insights.html` | Blog listing — 8 articles, all linking to local Spanish article pages |
| `privacy-policy.html` | "Aviso de privacidad" — translated with legal fidelity per Mexican LFPDPPP |

### Insight articles (8 transcreated)
| File | Original title |
|------|---------------|
| `articulo-estrategia-de-marca.html` | Brand Strategy as a System |
| `articulo-mas-alla-del-embudo.html` | Beyond the Funnel |
| `articulo-marcas-consumidores-ia.html` | How Brands Can Win Consumers with AI |
| `articulo-ia-personalizacion-crm.html` | AI Reshaping CRM Personalization |
| `articulo-ser-dueno-de-tu-ethos.html` | Owning Your Ethos |
| `articulo-impacto-aranceles-2025.html` | Impact of 2025 Tariffs |
| `articulo-megan-flynn-premio.html` | Megan Flynn C-Suite Award |
| `articulo-tendencias-consumidor-2025.html` | 2025 Consumer Trends |

### Supporting files
| File | Description |
|------|-------------|
| `glossary.md` | Term glossary with rationale for all vocabulary decisions |
| `transcreation-notes.md` | Creative decisions documented for every major choice |
| `creative-transcreation-localization.md` | The agent definition (reference copy) |
| `styles.css` | Shared stylesheet (unchanged from English) |
| `photos/` | Shared image assets |

---

## Key creative decisions

| English | Spanish | Rationale |
|---------|---------|-----------|
| "Proof, Not Promises" | "Hechos, no promesas" | Stronger cultural resonance — "actions over words" is a deeply held Mexican business value |
| "Full-Stack Marketing" | "Marketing integral de principio a fin" | "Integral" is the standard Mexican agency term for full-service |
| "Let's Talk" | "Hablemos" | Warm, direct, B2B appropriate — avoids overly casual "platiquemos" and overly formal "conversemos" |
| "Privacy Policy" | "Aviso de privacidad" | Legally correct Mexican term per LFPDPPP (not "Política de privacidad") |
| "Years of Partnerships" | "Años de alianzas" | Relationship-first framing — "alianzas" resonates more than "asociaciones" in Mexican business |
| "$1.2B+" | "USD $1.2B+" | Added USD prefix for clarity — $ alone means Mexican Pesos |
| "Insights" | "Perspectivas" | Natural, professional — better than literal "conocimientos" |
| Testimonial quotes | Angular quotation marks «» | Spanish quotation convention |

---

## Quality standards applied

- All ¿¡ inverted punctuation marks present (the #1 "gringo wrote this" signal)
- Accent marks on all words that require them, including capitals
- No Title Case in Spanish headings — sentence case only
- Simple past tense throughout (Mexican preference, not Spain's present perfect)
- Lowercase days, months, nationalities
- "Marketing" not "mercadotecnia" (modern Mexican usage)
- "Costo" not "coste" (Mexico, not Spain)
- No "vosotros" — always "ustedes"
- No "coger" — safe vocabulary throughout
- Usted in body copy, tú in CTAs
- All `lang="es-MX"` set on every page
- False cognates checked against watchlist

---

## Remaining items

- [ ] Connect Vercel to `mikemccartin/es-tandemtheory` repo
- [ ] Add CNAME record: `es.tandemtheory.com` → `cname.vercel-dns.com`
- [ ] Create new BugHerd project for es.tandemtheory.com and add script to all 11 HTML pages
- [ ] Add language selector link on tandemtheory.com (English site) pointing to es.tandemtheory.com
- [ ] Add language selector link on es.tandemtheory.com pointing back to tandemtheory.com
- [ ] Native speaker review (Max or other fluent reviewer via BugHerd)
- [ ] Consider hreflang tags for SEO (tells Google the two sites are language variants of each other)

---

## The Agent: creative-transcreation-localization

**Location**: 
- `~/.claude/agents/creative-transcreation-localization.md` (globally available)
- `tandem-ai/.claude/agents/creative-transcreation-localization.md` (official agent repo)
- `2026site/es-mx/creative-transcreation-localization.md` (project reference)

**Size**: 917 lines

**What it does**: Transcreates, translates, and culturally adapts marketing, web, and business content between English and Spanish regional variants. It thinks like a bilingual creative director, not a translator.

**What makes it different from a translator:**
- Rebuilds messaging for the target culture rather than converting words
- Deep Mexican Spanish reference material: vocabulary tables (30+ business/tech terms), formality spectrum, false cognate watchlist (21 dangerous entries), punctuation/typography rules, SEO keyword mapping
- Structured 6-phase workflow: discovery → source analysis → glossary → transcreation → quality review → delivery with notes
- Understands regional variants (Mexican, Castilian, Argentine, Colombian, Pan-Latin) with Mexican Spanish as default
- Includes documented real brand fail examples (Parker Pen, American Airlines, KFC, NPR) as cautionary training data
- Built-in quality checklist covering linguistic, cultural, brand, and technical dimensions
- Content type playbooks for websites, campaigns, emails, and presentations
- SEO keyword reference showing what Mexicans actually search vs. what translators assume

**Key rules it enforces:**
- ¿¡ inverted punctuation on every question and exclamation
- Accent marks on all words including capitals (ADQUISICIÓN not ADQUISICION)
- No Title Case in Spanish — sentence case only
- Simple past tense (comí) — Mexican preference over Spain's present perfect (he comido)
- "Marketing" not "mercadotecnia", "costo" not "coste", "Aviso de privacidad" not "Política de privacidad"
- Relationship-first framing for Mexican business culture
- Discovery process with guided questions (like job-description-writer agent)
- Glossary establishment for consistency across multi-page projects
- Transcreation notes documenting every creative decision

**Naming convention**: Follows Tandem Theory's `{category}-{function}` agent naming standard under the `creative-` prefix.

**Integration**: Works upstream from web development agents (receives content), downstream from strategy/brand agents (receives positioning), parallel with design agents (visual adaptation).
