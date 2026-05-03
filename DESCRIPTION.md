# Forensic Style Auditor — Skill Description

**Author:** TABARC-Code  
**Version:** 2.0  
**Type:** Claude Skill  

---

## One-Line

Reverse-engineers any writer's voice and produces accurate clones across all formats.

---

## Short Description

Forensic Style Auditor is a Claude skill that deconstructs writing style across ten forensic dimensions — sentence architecture, burstiness, lexical fingerprints, dialogue mechanics, thematic gravity, and more — then clones the voice for new content in any format.

Works on literary fiction, business writing, journalism, op-eds, social media, scripts, and personal correspondence. Includes an evolutionary improvement loop that labels generations, states rule changes explicitly, and iterates until the clone is right.

Ships with a complete worked example (Author: Church) covering a five-novel corpus, fully documented across all ten dimensions with a ready-to-use cloning instruction manual.

---

## Capability Summary

| Capability | Description |
|---|---|
| **Style Audit** | 10-dimension forensic breakdown with diagnosis and cloning instruction per dimension |
| **Voice Clone** | New content generated in the source author's voice with pre-delivery checklist |
| **Authenticity Audit** | Existing text compared against fingerprint; breaks rated and corrected |
| **Evolutionary Loop** | Iterative improvement with generation labels, OLD/NEW rule pairs, dimension diagnosis |
| **Seed Corpus Mode** | Works from a single sentence upward; scales confidence with corpus size |

---

## Trigger Phrases

Activates on any of the following:

```
write in the style of / write like [person]
clone this author / sound like X
analyse this writing / what makes this voice distinctive
ghost-write / match my tone
forensic audit / capture this tone
reverse-engineer this prose / audit this for authenticity
continue this in the same voice / does this sound like [author]
[paste text] + any request for more, continuation, or analysis
```

**Formats covered:** fiction · non-fiction · essays · rhetoric · op-eds · business writing · social media · scripts · personal correspondence

---

## Linked Skills

| Skill | Direction | Purpose |
|---|---|---|
| `docx` | Outgoing | Export Style Report as formatted Word document |
| `pdf-reading` | Incoming | Extract source text from PDF before analysis |
| `file-reading` | Incoming | Route EPUB/DOCX source texts for extraction |
| `frontend-design` | Outgoing | Visual burstiness charts and vocabulary heatmaps |

---

## The 10 Dimensions

1. **Master Voice Profile** — emotional register and prose worldview  
2. **Sentence Architecture** — mode-specific length ranges and cadence unit  
3. **Burstiness Profile** — strategic vs. ambient sentence-length variation  
4. **Paragraph Cadence** — pulse pattern, chapter openings, single-line use  
5. **Lexical Fingerprints** — existential vocabulary, qualifier tics, thematic clusters  
6. **Contractions and Formality** — narration/dialogue register gap  
7. **Punctuation Personality** — em-dash, ellipsis, structural repetition  
8. **Perspective and Interiority** — FID depth, self-observation, temporal layering  
9. **Dialogue Mechanics** — subtext ratio, attribution, response-length pattern  
10. **Thematic Gravity** — core preoccupations expressed through structure  

---

## Confidence Levels

| Corpus | Level | Output |
|---|---|---|
| Under 200 words | Seed | Register + 2–3 patterns |
| 200–800 words | Partial | Full architecture + vocabulary snapshot |
| 800–3,000 words | Solid | All 10 dimensions |
| 3,000+ words | High | Full audit + cross-context comparison |

---

## Eval Performance

- **v1:** 96.5% across 8 targeted test cases  
- **v2:** 100% across 8 test cases + 25 trigger accuracy tests  

---

## Case Study Included

`references/church-case-study.md` — complete worked example from a five-novel speculative fiction corpus. All 10 dimensions documented in full. Ready-to-use cloning manual included.

---

## Installation

Drop `forensic-style-auditor.skill` into your Claude skills directory and reload.

---

**Author:** TABARC-Code  
**Licence:** MIT
