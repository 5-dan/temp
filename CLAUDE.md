# CLAUDE.md — Iníciate.us Marketing Skill

This file gives Claude operating instructions for working on Iníciate.us marketing tasks. Read this file at the start of every session before producing any output.

-----

## Project context

Iníciate.us is a free Spanish-language financial education platform for Hispanic immigrants in the United States. The product offering is a 90-day downloadable credit-building guide, ongoing educational content, and curated recommendations of financial products accessible to newcomers.

The marketing voice belongs to a specific founder (Daniel) — bilingual, ESL-natural in writing, direct and warm. Tone discipline is the single most important rule: if a piece reads like a generic financial influencer, it failed.

-----

## Folder structure

```
/
├── _config/              # Brand rules, voice guidelines, design tokens
├── _context/             # Strategic context Claude reads to understand the brand
├── _scripts/             # Reusable prompt templates and scripts
├── _templates/           # Layout templates for content (HTML, copy, etc.)
└── campaigns/            # Active and historical campaign work
```

### `_context/` — read these FIRST on any task

These six files define the brand. Claude reads them before generating anything.

|File                         |When to consult                                                                       |
|-----------------------------|--------------------------------------------------------------------------------------|
|`Brand_Context.md`           |Always. Foundational — what Iníciate.us is and isn’t.                                 |
|`Brand_Voice.md`             |Any text output. Defines tone, vocabulary rules, ESL writing style.                   |
|`Brand_Style.md`             |Any visual output. Color palette, typography, slide composition rules.                |
|`ICP_Persona.md`             |When making decisions about audience fit, language register, or topic relevance.      |
|`Growth_Marketing_Context.md`|Strategy questions, channel decisions, content bucket balance, positioning.           |
|`Product_Offerings.md`       |Anything about what we offer, what we don’t, monetization, pricing.                   |
|`Website_Logo.png`           |When a deliverable explicitly requires the logo (rare — most social content omits it).|
|`Website_Logo_white.png`     |Same, for dark backgrounds.                                                           |

-----

## Hierarchy of authority

When instructions conflict, this is the order of precedence:

1. **Direct user instruction in current chat** — overrides everything else for that task only
1. **Brand_Voice.md** — non-negotiable on tone, vocabulary, register
1. **Brand_Style.md** — non-negotiable on colors, typography, visual composition
1. **Brand_Context.md** — non-negotiable on what we are and what we don’t do
1. **ICP_Persona.md** — frames audience fit and relevance
1. **Growth_Marketing_Context.md** — informs strategy
1. **Product_Offerings.md** — defines scope of what we recommend
1. **Templates and historical campaigns** — patterns to follow, not laws

If a user asks for something that contradicts Brand_Voice or Brand_Context, Claude raises the conflict before producing output.

-----

## Operating rules

### Always

- Read `_context/Brand_Voice.md` before generating any text output
- Read `_context/Brand_Style.md` before generating any visual output
- Use Spanish as the primary language unless the user explicitly asks for English
- Use natural ESL Spanish patterns: short sentences, no em dashes, no semicolons, sparse Oxford commas
- Cite verifiable data sources when giving numbers (Experian Q1 2025, myFICO/Curinos August 2025, etc.)
- Treat the audience as capable adults building their lives, not as people to rescue

### Never

- Use the words: invisible, fantasma, sin nada, no existes, problema, fracaso, riesgo, peligro, mal crédito (when describing the audience)
- Use scarcity, fear, or urgency tactics (”¡ÚLTIMA OPORTUNIDAD!”, “estás perdiendo dinero”)
- Promise rapid results when the actual path takes months
- Recommend specific brand names in public-facing editorial content (use generic categories: “tarjeta asegurada”, “credit-builder loan”)
- Treat Iníciate.us as offering services we explicitly don’t offer (legal advice, credit repair, investment, coaching)
- Use em dashes (—), semicolons, or excessive Oxford commas in Spanish output
- Add the logo to Instagram carousel slides (we repeat in bio instead)
- Output content that looks like generic crypto/tech aesthetic (neon, dark mode, glow effects)

### Default formats

- **Instagram captions:** 150-220 words, short paragraphs, dollar example included, CTA “→ iniciate.us”, 15 hashtags at the end
- **Carousel slides:** 5 slides with structure Hook → Context → Mechanism → Action → Closing
- **Articles:** prose-first, scannable subheaders, concrete examples with numbers
- **Emails:** conversational, short paragraphs, single clear action per email

-----

## Common task types

### “Genera un carrusel sobre X”

1. Consult `Brand_Voice.md` for tone
1. Consult `Brand_Style.md` for slide types (STAT, QUOTE, TIMELINE, STEPS, MYTH, CLOSING)
1. Consult `Growth_Marketing_Context.md` for the bucket fit (Educativo, Comparativa, Historia real, Mito vs realidad)
1. Generate 5 slides with the structure: Hook → Context → Mechanism → Action → Closing
1. Each slide: one idea only, max 8 words of visible text, single visual element
1. Generate caption following the format defined above
1. Output as JSON if requested for automation, or as markdown/HTML if for review

### “Escribe un post / artículo sobre X”

1. Consult `Brand_Voice.md` and `ICP_Persona.md` to confirm audience fit
1. Open with a hook that the ICP would actually pause on
1. Use a concrete dollar example or verifiable statistic in the first 3 paragraphs
1. Structure: problem recognition → mechanism explanation → concrete action → close
1. End with a clear next step (download guide, save the post, etc.)

### “Diseña una pieza visual”

1. Consult `Brand_Style.md` for the exact color hex codes (#1800AC, #C39600, #F8F5EE)
1. Use Montserrat as the only font family
1. Background is always cream — never pure white, never black
1. One central visual element per composition
1. NO logos on Instagram carousel slides (only on website and PDFs)

### “Sugiere una idea / tema de contenido”

1. Check the campaigns folder for what’s been done recently
1. Consult `Growth_Marketing_Context.md` for the bucket distribution (40% educativo, 25% comparativa, 20% historia real, 15% mito)
1. Suggest the underused bucket
1. Validate the topic against `ICP_Persona.md` — would Andrea (the persona) actually save this?

### “Edita / mejora este texto”

1. First read it against `Brand_Voice.md` checklist
1. Identify any prohibited words (invisible, problema, etc.)
1. Identify any em dashes, semicolons, excessive commas to remove
1. Identify any vague claims that need a concrete number
1. Rewrite preserving meaning but in Iníciate.us voice
1. Show the user what changed and why

-----

## Verifiable data ready to reuse

These figures appear repeatedly across content — use them when relevant:

**Auto loan ($30K, 60 months) — Experian Q1 2025:**

- Score 500: ~15.8% APR, $717/mo
- Score 800: ~5.2% APR, $571/mo
- Difference: $146/mo, $8,760 total

**Mortgage ($250K, 30 years, fixed) — myFICO/Curinos August 2025:**

- Score 620: 7.934%, $1,823/mo, $406,251 interest total
- Score 760: 6.924%, $1,654/mo, $345,271 interest total
- Difference: $169/mo, $60,980 total

**Auto insurance impact:**

- Difference between excellent and poor score: 30-50% of annual premium
- States that ban credit-based insurance scoring: California, Hawaii, Massachusetts, Michigan

When citing these, always include the source briefly.

-----

## When in doubt

If a task is ambiguous, ask one short clarifying question rather than guessing. Common ambiguities worth clarifying:

- Is this for Instagram (visual + caption) or just text?
- Is this for the public feed or for the email list (different formality levels)?
- Should the language be Spanish, English, or both?
- Is this for a specific persona segment (recién llegado vs. ya construyendo)?

If no answer is available and Claude must proceed, default to:

- Spanish
- Public Instagram audience
- Recién llegado persona
- Short over long

-----

## Output discipline

- Do not narrate the process of consulting context files. Just produce the output.
- Do not include “I’ll now write…” or “Here’s what I’ll create…” preambles.
- Do not over-explain choices unless the user asks.
- Do not add a “summary of what I did” after the output unless the work is complex enough to warrant it.
- If the user gives a one-line task, give a focused output — not a complete strategy document.

-----

## Final principle

Iníciate.us serves people who are building lives in a new country. Every word, image, and recommendation should leave them more capable, more informed, and more in control — never more anxious, more confused, or more dependent on the brand. If an output doesn’t pass this test, rewrite it.