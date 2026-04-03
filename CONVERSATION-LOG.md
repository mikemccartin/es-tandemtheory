# es.tandemtheory.com — Conversation Log

**Date**: April 3, 2026
**Session**: Full build of Spanish transcreated website

---

## What was accomplished

### 1. Transcreation Agent Built
- Created `creative-transcreation-localization.md` (917 lines)
- Named per Tandem Theory's `{category}-{function}` convention
- Deep Mexican Spanish reference: vocabulary tables, false cognates, punctuation rules, SEO keywords, brand fail examples, cultural norms
- Stored in `~/.claude/agents/`, `tandem-ai/.claude/agents/`, and `es-mx/` project folder
- Copies on Desktop for sharing

### 2. English HTML Synced with Live WordPress Site
- Technology section overhauled (partner ecosystem removed, proprietary product suite added)
- EDWARD category updated: "AI Operations Platform" → "AI Workflow Platform"
- AI Agents stat: "150+" → "100s AI Agents/Tools/Skills/MCPs Built"
- 2 new insight articles added (April 3 and March 27, 2026)

### 3. Full Site Transcreated into Mexican Spanish (es-MX)
- **index.html** — all sections: hero, humans, technology, services, results, testimonials, contact, footer
- **perspectivas.html** — 8 article listings with Mexican date format
- **aviso-de-privacidad.html** — legal translation per Mexican LFPDPPP
- **8 article pages** — full thought leadership articles transcreated
- **glossary.md** — term glossary with rationale
- **transcreation-notes.md** — creative decisions documented
- **PROJECT-RECAP.md** — full project summary

### 4. Key Creative Decisions
| English | Spanish | Why |
|---------|---------|-----|
| "Proof, Not Promises" | "Hechos, no promesas" | Culturally punchier — "actions over words" is deep Mexican value |
| "Full-Stack Marketing" | "Marketing integral de principio a fin" | "Integral" is standard Mexican agency term |
| "Let's Talk" | "Hablemos" | Warm, direct, B2B appropriate |
| "Privacy Policy" | "Aviso de privacidad" | Legally correct Mexican term per LFPDPPP |
| "Years of Partnerships" | "Años de alianzas" | Relationship-first framing |
| "$1.2B+" | "USD $1.2B+" | $ alone means MXN in Mexico |
| "Insights" | "Perspectivas" | Natural, professional |

### 5. File Names Translated
- `insights.html` → `perspectivas.html`
- `privacy-policy.html` → `aviso-de-privacidad.html`
- All internal links updated across 11 HTML files

### 6. CSS Synced with Live WordPress Site
- Downloaded all 19 CSS files from live tandemtheory.com
- Combined into single `styles.css`
- Replaced inline style blocks on all HTML pages with external stylesheet link
- Applied to both English HTML prototype and Spanish site

### 7. HTML Structure Synced with Live WordPress Site
- Rainbow color bar added under nav (`nav__color-bar`)
- Particles canvas and animated layers removed (removed on live site per creative direction)
- Particles JavaScript removed (120+ lines)
- Technology section HTML restructured to match live site classes (`intelligence-suite`, `suite-header`, `suite-footer`, `container--suite`)

### 8. EN | ES Language Switcher
- Added to all 11 ES pages — EN links to tandemtheory.com, ES highlighted as active
- Added to English HTML prototype — EN highlighted, ES links to es.tandemtheory.com
- Added to live WordPress site via WPCode JavaScript snippet
- Style: monospace font, red accent on active language, right side of nav

### 9. BugHerd
- New BugHerd project created for es.tandemtheory.com
- Script added to all 11 HTML pages with new API key (`samqx12xtiby1tspx6awha`)
- Old API key replaced on index.html

### 10. GitHub + Vercel + DNS
- Repo created: `mikemccartin/es-tandemtheory`
- Connected to Vercel
- Live at es.tandemtheory.com
- CNAME configured

### 11. Card Flip Bug Fix
- **Problem**: Front face text visible through back face on technology tool card flip
- **Root cause**: Semi-transparent rgba backgrounds (4% opacity) on card faces — text bleeds through
- **Fix**: `visibility: hidden` on front face when hovered/flipped, `visibility: visible` on back face
- Applied to ES site via styles.css
- Applied to live WordPress site via WPCode CSS snippet

---

## Remaining Items
- [ ] Native speaker review via BugHerd (Max or fluent reviewer)
- [ ] hreflang tags for SEO (tells Google the EN/ES sites are language variants)
- [ ] Article links on perspectivas.html still link to local HTML — future articles will need transcreation too
- [ ] Consider registering tandemtheory.mx as redirect to es.tandemtheory.com

---

## Issues Encountered

### Cloudflare WAF Blocking
- REST API works for ACF/content but Cloudflare blocks any POST payload containing HTML/JS tags
- Cannot edit WordPress theme files via REST API
- Solution: use WPCode snippets manually in WP Admin for JS/CSS injection
- **Memory saved**: `feedback_wp_cli_limits.md` — stop after one failed attempt, give user paste-ready code

### HTML/CSS Drift
- The v2 HTML prototype had drifted significantly from the live WordPress site
- CSS was inline in index.html (2,833 lines) vs external files on WP
- HTML class names differed (e.g., `tech-ecosystem` vs `intelligence-suite`)
- Particles and animated layers were removed on live site but still in prototype
- Rainbow color bar was added on live site but missing from prototype
- **Lesson**: Always pull fresh CSS and compare HTML structure from live site before building on the prototype

---

## Files in this directory

```
es-mx/
├── index.html                              # Homepage (transcreated)
├── perspectivas.html                       # Insights listing (transcreated)
├── aviso-de-privacidad.html                # Privacy policy (translated)
├── articulo-estrategia-de-marca.html       # Brand Strategy as a System
├── articulo-mas-alla-del-embudo.html       # Beyond the Funnel
├── articulo-marcas-consumidores-ia.html    # Brands Win Consumers with AI
├── articulo-ia-personalizacion-crm.html    # AI Reshaping CRM
├── articulo-ser-dueno-de-tu-ethos.html     # Owning Your Ethos
├── articulo-impacto-aranceles-2025.html    # Impact of 2025 Tariffs
├── articulo-megan-flynn-premio.html        # Megan Flynn C-Suite Award
├── articulo-tendencias-consumidor-2025.html # 2025 Consumer Trends
├── styles.css                              # Combined CSS from live WP site
├── photos/                                 # Shared image assets
├── glossary.md                             # Term glossary
├── transcreation-notes.md                  # Creative decisions
├── creative-transcreation-localization.md  # Agent definition (reference)
├── PROJECT-RECAP.md                        # Project summary
├── CONVERSATION-LOG.md                     # This file
├── favicon.ico / favicon-*.png             # Favicons
└── apple-touch-icon.png                    # Apple touch icon
```

---

## Key URLs
- **Live English site**: https://tandemtheory.com
- **Live Spanish site**: https://es.tandemtheory.com
- **GitHub repo**: https://github.com/mikemccartin/es-tandemtheory
- **WP Engine environment**: tt2026newsite

---

*Session completed April 3, 2026*
