# Session Log: Initial Project Setup

**Date:** 2026-05-21
**Project:** AP Psychology Intelligent Textbook
**Site URL:** https://dmccreary.github.io/psychology/

---

## Step 1: Scaffold the Textbook (`/init-textbook`)

**Skill invoked:** `init-textbook`

### 1.1 Directory check

Ran `ls -la` in `/Users/dan/Documents/ws/psychology`. Found only `.git/` — clean slate, safe to scaffold.

### 1.2 Git info gathered

```
git config user.name  → Dan McCreary
git remote get-url origin → https://github.com/dmccreary/psychology.git
basename $(pwd) → psychology
date +%Y → 2026
```

### 1.3 User inputs collected

| Variable | Value |
|----------|-------|
| SITE_NAME | Psychology |
| SITE_DESCRIPTION | A comprehensive intelligent textbook exploring human thought, emotion, development, and behavior through interactive simulations and guided learning. |
| SITE_AUTHOR | Dan McCreary |
| GITHUB_USERNAME | dmccreary |
| REPO_NAME | psychology |
| PRIMARY_COLOR | green |
| ACCENT_COLOR | orange |
| YEAR | 2026 |
| LINKEDIN_URL | https://www.linkedin.com/in/danmccreary/ |

### 1.4 Files created

Directory tree scaffolded at `/Users/dan/Documents/ws/psychology/`:

```
mkdocs.yml
docs/
├── index.md
├── about.md
├── course-description.md
├── contact.md
├── license.md
├── chapters/
│   └── index.md
├── learning-graph/
│   └── index.md
├── sims/
│   └── index.md
├── css/
│   └── extra.css
├── js/             (empty)
└── img/
    └── license.png
```

Key `mkdocs.yml` choices:
- Theme: Material, palette primary=green / accent=orange
- No `navigation.tabs` (side nav optimized for wide screens)
- `pymdownx.arithmatex` enabled (renderer added later via book-installer)
- `exclude_docs` populated for `image-prompt*.md`, `TODO.md`, etc.
- `extra.generator: false` (suppress "Made with Material" footer)
- MicroSim status indicators (`scaffold` / `built` / `approved`) wired via CSS variables in `extra.css` (NOT via `theme.icon.status`, which is Insiders-only)

---

## Step 2: User Enhancements (manual edits)

After scaffolding, the user made the following manual changes:

### 2.1 `mkdocs.yml` — nav expanded

Added learning graph sub-pages and a graph viewer MicroSim to the nav:

```yaml
Learning Graph:
  - Introduction: learning-graph/index.md
  - Course Description Assessment: learning-graph/course-description-assessment.md
  - Concept List (College Board): learning-graph/concept-list-from-college-board.md
  - Concept Enumeration: learning-graph/concept-list.md
  - Graph Quality Analysis: learning-graph/quality-metrics.md
  - Concept Taxonomy: learning-graph/concept-taxonomy.md
  - Taxonomy Distribution Report: learning-graph/taxonomy-distribution.md

MicroSims:
  - List of MicroSims: sims/index.md
  - Learning Graph Viewer: sims/graph-viewer/index.md
```

Also added `**/index-template.md` to `exclude_docs`.

### 2.2 `docs/course-description.md` — full AP course description

Replaced the placeholder with a complete AP Psychology course description (quality score: 100/100) including:
- Audience: high school grades 11–12 AP students
- Prerequisites: none (general reading/numeracy only)
- **6 topic domains** aligned to the College Board AP CED (Effective Fall 2024):
  1. Biological Bases of Behavior
  2. Cognition
  3. Development and Learning
  4. Social Psychology and Personality
  5. Mental and Physical Health
  6. Research Methods (cross-cutting)
- Explicit list of **topics NOT covered** (sodium-potassium pump, Freud's psychosexual stages, full DSM-5, etc.)
- Full Bloom's Taxonomy outcomes across all 6 levels (Remember → Create)

### 2.3 `docs/learning-graph/index.md` — full learning graph landing page

Replaced placeholder with a content-rich page including:
- Iframe embed of the graph viewer (`sims/graph-viewer/main.html`)
- Summary: **387 concepts, 12 categories**, aligned to AP CED
- Links to all learning graph analysis files (CSV, JSON, assessments)
- Taxonomy color legend table (FOUND=SteelBlue, BIO=DarkGreen, … CLIN=DarkSlateBlue)

The learning graph itself (`learning-graph.json`) was also generated — 387 nodes, 587 edges, vis-network format, valid DAG (0 cycles).

---

## Step 3: Design Chapter Structure (`/book-chapter-generator`)

**Skill invoked:** `book-chapter-generator`

### 3.1 Inputs read

- `docs/course-description.md` — AP Psychology full description
- `docs/learning-graph/learning-graph.json` — 387 nodes, 587 edges
- `docs/learning-graph/concept-taxonomy.md` — 12 taxonomy categories

### 3.2 Graph analysis (Python agent)

A Python agent was spawned to:
1. Parse `learning-graph.json`
2. Build the prerequisite map using the dependency direction: `prereqs[edge['from']].add(edge['to'])`
3. Validate edge direction — confirmed foundational concepts are simple/introductory (Psychology as a Science, Scientific Method, etc.)
4. Run topological sort — clean, 0 cycles
5. Assign all 387 concepts to 16 chapters following taxonomy order (FOUND → BIO → CHEM → SEN → COG → MEM → DEV → LEARN → SOC → PERS → HLTH → CLIN)
6. Resolve 5 cross-category dependency violations by moving individual concepts

### 3.3 Cross-category moves (violations resolved)

| Concept | Original taxonomy | Moved from | Moved to | Reason |
|---------|------------------|------------|----------|--------|
| Circadian Rhythms | BIO | Ch 2 | Ch 3 | Depends on Melatonin (CHEM) |
| Stereotype Threat | COG | Ch 5 | Ch 11 | Depends on Stereotypes (SOC) |
| Fixed vs. Growth Mindset | COG | Ch 5 | Ch 10 | Depends on Self-Efficacy (LEARN) |
| Posttraumatic Growth | HLTH | Ch 14 | Ch 16 | Depends on PTSD (CLIN) |
| Ethnocentrism | SOC | Ch 11 | Ch 15 | Depends on Sociocultural Perspective on Disorders (CLIN) |

### 3.4 Output

Chapter plan saved to `docs/learning-graph/chapters.json`.

### 3.5 Proposed 16-chapter structure (awaiting user approval)

| # | Title | Concepts |
|---|-------|----------|
| 1 | Foundations of Psychology and Research Methods | 30 |
| 2 | Biological Bases of Behavior: Neurons and the Brain | 36 |
| 3 | Neurochemistry and Psychopharmacology | 35 |
| 4 | Sensation and Perception | 26 |
| 5 | Cognition and Thinking | 22 |
| 6 | Memory: Encoding, Storage, and Models | 18 |
| 7 | Memory: Retrieval, Forgetting, and Distortion | 18 |
| 8 | Development: Prenatal Through Childhood | 19 |
| 9 | Development: Adolescence Through Adulthood | 18 |
| 10 | Learning and Conditioning | 28 |
| 11 | Social Psychology: Attitudes, Attribution, and Influence | 19 |
| 12 | Social Psychology: Groups, Prejudice, and Aggression | 18 |
| 13 | Personality and Motivation | 31 |
| 14 | Health Psychology and Introduction to Psychological Disorders | 23 |
| 15 | Psychological Disorders | 23 |
| 16 | Treatment and Therapy | 23 |

**Total: 387 concepts · min 18 · max 36 · avg 24.2 · dependency violations: 0 ✓**

**Status: Awaiting user approval before generating chapter directories and `mkdocs.yml` nav.**

---

## Current State

```
docs/
├── index.md                          ✓ complete
├── about.md                          ✓ complete
├── course-description.md             ✓ complete (quality score 100/100)
├── contact.md                        ✓ complete
├── license.md                        ✓ complete
├── chapters/
│   └── index.md                      ✓ placeholder
├── learning-graph/
│   ├── index.md                      ✓ complete
│   ├── learning-graph.json           ✓ 387 nodes, 587 edges
│   ├── chapters.json                 ✓ 16-chapter plan
│   └── concept-taxonomy.md           ✓ complete
├── sims/
│   ├── index.md                      ✓ placeholder
│   └── graph-viewer/                 ✓ (graph viewer MicroSim)
├── css/extra.css                     ✓ complete
└── img/license.png                   ✓ complete
mkdocs.yml                            ✓ complete
```

## Next Steps

1. User approves (or revises) the 16-chapter structure
2. Run `book-chapter-generator` Step 4 to create chapter directories and `index.md` files
3. Update `mkdocs.yml` nav with all 16 chapter entries
4. Run `chapter-content-generator` to fill each chapter with content
5. Run `microsim-generator` as needed for interactive sims
6. Run `glossary-generator`, `faq-generator`, `quiz-generator` once ≥30% of chapters are complete
