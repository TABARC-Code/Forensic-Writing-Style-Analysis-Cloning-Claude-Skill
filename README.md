# Forensic Style Auditor

**Author / Programmer:** TABARC-Code  
**Version:** 2.0  
**Compatibility:** Claude.ai · Claude Desktop · Cowork  
**Type:** Claude Skill (`.skill`)

---

## What It Does

Forensic Style Auditor is a Claude skill that reverse-engineers any writer's voice and produces accurate clones across all formats and registers.

It works on any written material: literary fiction, business memos, op-eds, essays, social media posts, personal correspondence, scripts, journalism — anything where voice is a distinguishing factor.

There are three core capabilities:

**1. Deconstruct**  
Give it a writing sample — a passage, a set of emails, a thread, a chapter — and it analyses the author's voice across ten forensic dimensions: sentence architecture, burstiness, paragraph cadence, lexical fingerprints, formality gradients, punctuation personality, perspective and interiority, dialogue mechanics, thematic gravity, and master voice profile. It produces either a full structured Style Report or a condensed Cloning Key, depending on what you need.

**2. Clone**  
Using the extracted fingerprint, it generates new content in the author's voice — new chapters, memos, tweets, posts, speeches, continuation scenes — applying a pre-delivery checklist to catch common failures like register drift, mode-mixing, and vocabulary contamination before output.

**3. Audit**  
If you are already writing in someone's style and want to know where you have drifted, it reads your work against the established fingerprint and flags specific breaks with explanations and suggested corrections.

---

## How It Works

### The 10-Dimension Audit Framework

Every analysis runs across ten dimensions. Each produces a diagnosis and a cloning instruction.

| # | Dimension | What It Captures |
|---|---|---|
| 1 | Master Voice Profile | Fundamental emotional register; the prose's implicit worldview |
| 2 | Sentence Architecture | Mode-specific sentence length ranges; core cadence unit (e.g. accumulate-then-strike) |
| 3 | Burstiness Profile | Whether sentence-length variation is strategic or ambient; high/low burstiness by scene type |
| 4 | Paragraph Cadence | Paragraph pulse pattern; chapter-opening method; single-line paragraph use |
| 5 | Lexical Fingerprints | Existential vocabulary; qualifier tics; thematic clusters; jargon handling |
| 6 | Contractions and Formality | Narration vs. dialogue register gap; where informality enters and leaves |
| 7 | Punctuation Personality | Em-dash frequency and function; ellipsis policy; structural repetition |
| 8 | Perspective and Interiority | Free indirect discourse depth; self-observation technique; temporal layering |
| 9 | Dialogue Mechanics | Subtext ratio; attribution style; response-length pattern; agreement-as-disagreement |
| 10 | Thematic Gravity | 3–5 core preoccupations the author cannot stop returning to |

---

### Four Output Paths

```
Path A — Full Audit (uploaded files)
  Read files → Sample corpus → All 10 dimensions → Style Report → Clone or Audit

Path B — Paste and Clone (pasted sample)
  Assess confidence → Abbreviated or full audit → Clone Key → Generate → Checklist

Path C — Authenticity Audit
  Establish baseline → Audit passage by passage → Drift ratings → Corrections

Path D — Evolutionary Improvement
  Generation label → Diagnose failing dimension → OLD/NEW rule pair → Regenerate → Offer to continue
```

---

### The Evolutionary Improvement Loop

The most powerful feature. Every time the output is close but not right, the skill enters the improvement loop:

```
GENERATION N → USER FEEDBACK → DRIFT DIAGNOSIS → ROOT CAUSE → RULE UPDATE → GENERATION N+1
```

Each iteration is explicitly numbered. The failing dimension is named. The old rule and new rule are stated as a pair. After delivery, the skill offers to continue.

Feedback maps to dimensions automatically:

| User says | Dimension | Likely fix |
|---|---|---|
| "too formal / too stiff" | Formality (Dim 6) | Lower narration register |
| "dialogue is wrong" | Dialogue (Dim 9) | Subtext ratio, response length, attribution |
| "doesn't sound like them" | Master Voice (Dim 1) | Re-examine emotional register |
| "vocabulary is off" | Lexical (Dim 5) | Rebuild vocabulary cluster from source |
| "sentences feel different" | Architecture (Dim 2) | Re-calibrate mode parameters |
| "pacing is off" | Burstiness + Cadence (Dim 3, 4) | Re-examine mode-switching |
| "too literary / too plain" | Register Anchor | Re-set register from source sample |

---

### Corpus Confidence Levels

The skill never refuses to work with small samples. Confidence levels scale with what you provide:

| Corpus size | Confidence | Capability |
|---|---|---|
| Under 200 words | Seed | Register and 2–3 structural patterns; states what is missing |
| 200–800 words | Partial | Full sentence architecture, tone, vocabulary snapshot |
| 800–3,000 words | Solid | All 10 dimensions with evidence |
| 3,000+ words | High | Full audit; cross-context comparison |

A seed corpus is a starting point, not a barrier. The skill extracts everything possible and updates as more material is provided.

---

## Domain Coverage

| Domain | Primary Dimensions |
|---|---|
| Literary fiction | Master voice, sentence architecture, thematic gravity, perspective |
| Business / professional writing | Register anchor, formality gap, lexical fingerprints |
| Rhetoric / essays / op-eds | Sentence architecture, paragraph cadence, punctuation |
| Social media / micro-formats | Length distribution, register anchor, lexical tics |
| Scripts / screenplays | Dialogue mechanics, rhythm, subtext |
| Personal correspondence | Formality, contractions, thematic gravity |

---

## Trigger Phrases

The skill activates on:

- "write in the style of" / "write like [person]"
- "clone this author" / "sound like X"
- "analyse this writing" / "what makes this voice distinctive"
- "ghost-write" / "match my tone"
- "forensic audit" / "capture this tone"
- "reverse-engineer this prose" / "audit this for authenticity"
- "continue this in the same voice" / "does this sound like [author]"
- pasting a sample and asking for more, continuation, or analysis

Covers all formats: fiction, non-fiction, essays, rhetoric, op-eds, business writing, social media, scripts, and personal correspondence.

**Trigger accuracy (tested against 25 queries):** 100%

---

## Bidirectional Skill Links

| Linked Skill | When | Why |
|---|---|---|
| `docx` | User wants report as Word document | Style Report with headings, pull-quotes, table of contents |
| `pdf-reading` | Source texts are PDFs | Extract text correctly before analysis |
| `file-reading` | Source texts are EPUB or DOCX | Route to correct extraction method |
| `frontend-design` | Visual report requested | Burstiness charts, vocabulary heatmaps |

Incoming: `docx`, `pdf-reading`, and `file-reading` hand off to this skill when they detect a style-analysis or voice-matching request.

---

## File Structure

```
forensic-style-auditor/
├── SKILL.md                          Core methodology (289 lines)
└── references/
    ├── report-template.md            Full style report structure with all section headers
    ├── dimension-deep-dives.md       Extended analysis guidance for each dimension
    ├── sampling-protocol.md          File-type routing and corpus sampling strategy
    ├── improvement-tracker.md        Multi-generation project log template
    ├── activation-prompts.md         Tested scene-type prompts for clone generation
    └── church-case-study.md          Complete worked example — see below
```

---

## Case Study: Author Church

The skill ships with a complete worked example based on a multi-novel corpus from the author designated **Church** — a contemporary author writing large-scale speculative military fiction across multiple settings and character types.

The corpus analysed covers five works spanning distinct narrative registers: philosophical decay fiction, inquisitorial thriller, dynastic warfare, and dark age military drama. Total corpus: approximately 3.4 million characters.

The case study documents all ten dimensions in full, including:

- The **accumulate-then-strike** cadence unit and its mode-specific variations
- The **four-stage paragraph pulse** (entry / expansion / complication / cut)
- Vocabulary clusters for four distinct thematic registers (duty-without-faith, decay-and-persistence, identity-under-erasure, political-threat)
- The **free indirect discourse** technique including tense slippage within interiority
- The **self-observation** interiority method — characters watching themselves think
- The **assume-and-proceed** world-building method — jargon qualified by physical description only, never explained
- The complete Forbidden List (twelve patterns that break the voice)

The case study functions as a calibration reference: it shows what a completed high-confidence audit looks like, and provides a ready-to-use cloning manual for Church's voice specifically.

---

## Eval Results

The skill was developed through two full evaluation iterations.

**Iteration 1 (v1):** 34.75 / 36 across 8 targeted test cases (96.5%)  
**Iteration 2 (v2):** 36 / 36 (100%) after applying 8 identified fixes

Key fixes applied between iterations:

- Register anchoring rule (preventing clone from drifting above source register)
- Evolutionary loop given explicit generation numbering and OLD/NEW rule pair format
- Report template invocation made mandatory for full audits
- Two corpus-type confidence frames (known author vs. unknown personal author)
- Domain coverage extended to non-fiction, social media, scripts, correspondence
- Minimum corpus framing changed from threshold to starting point
- Length distribution added to pre-delivery checklist for micro-formats
- Pre-generation checklist made visible to users on request

---

## Installation

Drop the `.skill` file into your Claude skills directory and reload.

---

## Licence

MIT  
© TABARC-Code
