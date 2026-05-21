# CLAUDE.md — AP Psychology Intelligent Textbook

Project-level instructions for Claude Code. These override global defaults.

## Project Overview

- **Site:** AP Psychology intelligent textbook
- **URL:** https://dmccreary.github.io/psychology/
- **Framework:** MkDocs Material (community edition)
- **Primary color:** green · **Accent:** orange
- **Audience:** High school students (grades 11–12), AP exam prep

## Publish Command

When the user says "publish", run these three steps in order:
1. `git commit` any uncommitted changes
2. `git push`
3. `mkdocs gh-deploy --force`

## Navigation Rule

Do NOT add `navigation.tabs` to `mkdocs.yml`. This book uses side navigation
optimized for wide landscape screens.

---

## Learning Mascot: Psy the Owl

### Mascot File Index

The canonical files for this mascot. When editing any of these, update the
others in the same turn so they stay in sync.

| File | Purpose |
|------|---------|
| [`docs/img/mascot/character-sheet.md`](docs/img/mascot/character-sheet.md) | Canonical identity document (name, species, colors, voice). Source of truth. |
| [`docs/img/mascot/image-prompts.md`](docs/img/mascot/image-prompts.md) | Self-contained AI prompts for regenerating each pose. |
| [`docs/img/mascot/neutral.png`](docs/img/mascot/neutral.png) | Default / general-purpose pose. |
| [`docs/img/mascot/welcome.png`](docs/img/mascot/welcome.png) | Chapter-opening pose. |
| [`docs/img/mascot/thinking.png`](docs/img/mascot/thinking.png) | Key-concept pose. |
| [`docs/img/mascot/tip.png`](docs/img/mascot/tip.png) | Hint / helpful-guidance pose. |
| [`docs/img/mascot/warning.png`](docs/img/mascot/warning.png) | Common-mistake / pitfall pose. |
| [`docs/img/mascot/encouraging.png`](docs/img/mascot/encouraging.png) | Difficult-content / struggle pose. |
| [`docs/img/mascot/celebration.png`](docs/img/mascot/celebration.png) | End-of-chapter / achievement pose. |
| [`docs/css/mascot.css`](docs/css/mascot.css) | Custom admonition styles for the seven pose contexts. |
| [`docs/learning-graph/mascot-test.md`](docs/learning-graph/mascot-test.md) | Rendering test page that exercises every admonition style. |

### Character Overview

- **Name:** Psy
- **Species:** Owl (stylized flat cartoon, round and compact)
- **Personality:** Warm and encouraging, patiently curious, gently humorous, empathetic
- **Catchphrase:** "Let's think about that!"
- **Visual:** Cream/ivory feathers, green-tinted wing tips, orange beak and talons, small round wire-frame glasses, tiny open notebook tucked under one wing

### Voice Characteristics

- Speaks in short, clear sentences accessible to high-school readers
- Uses "we" language to stand alongside the student, not above them
- Normalizes confusion: "This one trips a lot of people up — let's slow down together"
- Grounds enthusiasm in evidence: "Research shows…", "Studies suggest…"
- Signature phrases: "Let's think about that!", "Fascinating, right?", "You've got this!"

### Mascot Admonition Format

Always place mascot images in the admonition **body**, never in the title bar.
The `src` path is relative to the rendered page URL (count `../` from the
rendered page depth to `docs/img/mascot/`).

For a chapter page at `chapters/01-foundations/index.md` (renders at
`chapters/01-foundations/`), use `../../img/mascot/`.

```markdown
!!! mascot-welcome "Welcome to This Chapter!"
    <img src="../../img/mascot/welcome.png" class="mascot-admonition-img" alt="Psy waving welcome">
    Admonition text goes here after the img tag.
```

### Placement Rules

| Context | Admonition Type | Frequency |
|---------|----------------|-----------|
| General note / sidebar | mascot-neutral | As needed |
| Chapter opening | mascot-welcome | Every chapter (once) |
| Key concept | mascot-thinking | 2–3 per chapter |
| Helpful tip / study hint | mascot-tip | As needed |
| Common mistake / exam pitfall | mascot-warning | As needed |
| Difficult or sensitive content | mascot-encourage | Where students may struggle |
| Chapter completion | mascot-celebration | End of chapter (once) |

### Do's and Don'ts

**Do:**
- Use Psy to introduce new topics warmly
- Include the catchphrase in welcome admonitions
- Keep dialogue brief (1–3 sentences)
- Match the pose/image to the content type
- Acknowledge that mental health chapters may feel personal

**Don't:**
- Use Psy more than 5–6 times per chapter
- Place mascot admonitions back-to-back
- Use the mascot for purely decorative purposes
- Change Psy's personality or speech patterns
- Put mascot images in the admonition title bar
