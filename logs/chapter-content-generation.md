# Session Log: Chapter Content Generation

**Date:** 2026-05-21  
**Session skill:** chapter-content-generator  
**Operator:** Claude Sonnet 4.6 (claude-sonnet-4-6)  
**Project:** AP Psychology Intelligent Textbook  
**URL:** https://dmccreary.github.io/psychology/

---

## Overview

This session generated full content for all 16 chapters of the AP Psychology
intelligent textbook, replacing stub files created by the book-chapter-generator
skill. The work was split across two Claude Code sessions — chapters 1–8 in a
prior session (summarized from context), chapters 9–16 in the current session.

Input resources used:
- `docs/learning-graph/chapters.json` — authoritative chapter plan (16 chapters, 387 concepts)
- `docs/learning-graph/learning-graph.json` — concept dependency DAG
- `CLAUDE.md` — mascot character guidelines, admonition format, placement rules
- `docs/img/mascot/character-sheet.md` — Psy the Owl canonical identity

---

## Standing Instructions (Applied to All Chapters)

The user gave two standing instructions before generation began:

1. **Interactive infographic overlays** — use the `<details markdown="1">` pattern
   for all biological structures (neurons, brain regions, sensory organs, etc.)
   rather than static figures.

2. **Biology sim reuse** — check `../biology/docs/sims` and copy relevant sims
   to `docs/sims/` for embedding via iframe.

---

## Biology Sims Copied

Five sims were identified in `../biology/docs/sims/` and copied to `docs/sims/`:

| Sim | Iframe Height | Used In |
|-----|--------------|---------|
| `neuron-structure/` | 730px | Ch 2 (motor neuron anatomy) |
| `scientific-method/` | 1600px | Ch 1 (research methods flowchart) |
| `standard-deviation/` | 530px | Ch 1 (statistical reasoning) |
| `signal-transduction-pathway/` | 590px | Ch 3 (GPCR–cAMP pathway) |
| `feedback-loop-simulator/` | 740px | Ch 14 (GAS / stress response) |

---

## Chapter Generation Log

### Chapters 1–8 (Prior Session)

| Ch | Title | Concepts | ~Words | Status |
|----|-------|----------|--------|--------|
| 1 | Foundations of Psychology and Research Methods | 30 | 5,327 | ✓ Complete |
| 2 | Biological Bases of Behavior: Neurons and the Brain | 36 | 6,396 | ✓ Complete |
| 3 | Neurochemistry and Psychopharmacology | 35 | 5,511 | ✓ Complete |
| 4 | Sensation and Perception | 26 | 7,127 | ✓ Complete |
| 5 | Cognition and Thinking | 22 | 6,806 | ✓ Complete |
| 6 | Memory: Encoding and Storage | 18 | 5,648 | ✓ Complete |
| 7 | Memory: Retrieval and Forgetting | 18 | 7,074 | ✓ Complete |
| 8 | Development: Prenatal Through Childhood | 19 | 7,636 | ✓ Complete |

### Chapters 9–16 (This Session)

| Ch | Title | Concepts | ~Words | Status |
|----|-------|----------|--------|--------|
| 9 | Development: Adolescence Through Adulthood | 18 | 4,999 | ✓ Complete |
| 10 | Learning and Conditioning | 28 | 4,048 | ✓ Complete |
| 11 | Social Psychology: Attitudes, Attribution, and Influence | 19 | 3,533 | ✓ Complete |
| 12 | Social Psychology: Groups, Prejudice, and Aggression | 18 | 3,291 | ✓ Complete |
| 13 | Personality and Motivation | 31 | 4,209 | ✓ Complete |
| 14 | Health Psychology and Introduction to Psychological Disorders | 23 | 3,183 | ✓ Complete |
| 15 | Psychological Disorders | 23 | 3,692 | ✓ Complete |
| 16 | Treatment and Therapy | 23 | 3,919 | ✓ Complete |

**Total across all 16 chapters:** 387 concepts, ~82,400 words, 0 TODOs.

---

## Chapter Structure Convention

Every chapter follows a consistent internal structure:

```
---
YAML frontmatter (title, description, generated_by, date, version)
---

# Chapter N: Title

## Summary          — 4–6 sentence overview
## Concepts Covered — numbered list matching chapters.json
## Prerequisites    — links to prerequisite chapters

---

## N.1 First Section
  !!! mascot-welcome  (chapter opening, every chapter)
  ...content with <details> interactive diagrams...
  !!! mascot-thinking or mascot-tip (2–3 per chapter)

## N.2 ... N.X  Additional sections

## N.last Chapter Review
  !!! mascot-celebration  (chapter close, every chapter)
  ### Key Terms           — definition list
  ### Practice Questions  — 5 questions
  <details> Show Answers  — revealed on demand
```

---

## Mascot Admonition Usage

Psy the Owl appears 5–6 times per chapter, never back-to-back. Types used:

| Type | Context | Frequency |
|------|---------|-----------|
| `mascot-welcome` | Chapter opening | Every chapter (once) |
| `mascot-thinking` | Key concept elaboration | 2–3 per chapter |
| `mascot-tip` | AP exam strategy / study hint | As needed |
| `mascot-warning` | Common mistakes / misconceptions | As needed |
| `mascot-encourage` | Difficult or sensitive content | As needed |
| `mascot-neutral` | Clarifying sidebar notes | As needed |
| `mascot-celebration` | Chapter completion | Every chapter (once) |

Image paths use `../../img/mascot/` (from chapter depth `chapters/XX-slug/`).

---

## Interactive Diagram Pattern

All diagrams use the `<details markdown="1">` expand pattern rather than
static images. The heading above each `<details>` block uses
`#### Diagram: [title]` so it is visually separated from body prose.

Example (Chapter 13, Yerkes-Dodson):

```markdown
#### Diagram: The Yerkes-Dodson Inverted-U Curve

<details markdown="1">
<summary>Explore: How does task complexity shift the optimal arousal point?</summary>

[body text with two overlaid curve descriptions, examples, implications]

</details>
```

---

## Notable Content Decisions

**Chapter 1** — includes mandatory Psy self-introduction listing all seven
pose-roles (per CLAUDE.md convention for Chapter 1 only).

**Chapter 2** — embeds the `neuron-structure` MicroSim from biology for the
motor neuron anatomy diagram; uses interactive overlay for brain regions.

**Chapter 3** — embeds `signal-transduction-pathway` MicroSim (GPCR–cAMP)
for signal transduction section.

**Chapter 10** — covers 28 concepts (largest non-Ch13 chapter); structured
into three major frameworks (classical conditioning, operant conditioning,
social learning / cognitive) plus neuroplasticity and mindset.

**Chapter 13** — 31 concepts (largest chapter); structured into four
personality frameworks + motivation theories + emotion psychology. Each
section cross-references others to reduce cognitive load.

**Chapter 14** — embeds `feedback-loop-simulator` MicroSim for the GAS
(General Adaptation Syndrome) section; bridges stress biology and clinical
classification.

**Chapters 15–16** — cover disorder content jointly to avoid duplication:
Ch 15 surveys disorders + introduces therapy modalities; Ch 16 revisits
remaining disorders through the treatment lens (PTSD, bipolar, eating
disorders, panic disorder, dissociative disorders) and covers biological
treatments (medications, ECT, TMS, biofeedback).

---

## Git Commit

Commit: `a929d95`  
Message: "Generate full content for all 16 AP Psychology chapters"  
Files changed: 24 (16 chapter index.md files + 7 mascot PNG images + 1 deleted image-prompts.md)  
Insertions: 5,315 | Deletions: 298

---

## Validation

```
for each chapter:
  - words > 3000 ✓
  - grep "TODO" = 0 ✓
  - mascot-welcome present ✓
  - mascot-celebration present ✓
  - concepts covered list matches chapters.json ✓
```

---

## Next Steps

Recommended follow-on work:

1. **MicroSim generation** — `microsim-generator` skill to create interactive
   simulations for key concepts (Pavlov conditioning, Milgram obedience,
   memory models, neural action potential, etc.)

2. **Glossary generation** — `glossary-generator` skill; pull all bolded terms
   from chapters into a searchable glossary.

3. **FAQ generation** — `faq-generator` skill for each chapter.

4. **Quiz generation** — `quiz-generator` skill to expand beyond the 5
   end-of-chapter questions already included.

5. **Slide generation** — `book-installer 37` (slide-viewer + slides.md decks
   per chapter) for classroom presentation use.

6. **Reading level analysis** — `book-installer 38` (Flesch-Kincaid analysis)
   to check consistency across chapters; chapters 1–4 may score higher due to
   technical vocabulary.

7. **Publish** — `git push` + `mkdocs gh-deploy --force` to deploy to
   https://dmccreary.github.io/psychology/
