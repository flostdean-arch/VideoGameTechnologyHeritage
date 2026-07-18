# Contributing to VideoGameTechnologyHeritage

Thank you for your interest in this project.
This document explains **specifically what kind of contributions we're looking for** and how to submit them.

---

## 🎯 What We're Especially Looking For

We value **concrete, verifiable, citable specificity** over abstract "knowledge."
Writing at the level of detail below makes an article far more valuable to future readers.

**Good examples:**
- "The Famicom could only display up to 8 sprites per scanline; exceeding this caused flicker. Games of the era worked around this constraint using techniques such as..."
- "The camera control in [game name] uses a spring model that varies follow-delay based on player movement speed (source: developer interview URL)"

**What to avoid:**
- Unverifiable generalities like "old games were hard to make because storage was limited," with no specifics
- Hearsay with no source at all

## 📂 Where to Put Things

- `GameEngine/<engine family>/<generation>/` — Technical explanations of game engines (see below)
- `Hardware/` — Constraints and mechanisms of specific hardware
- `Algorithm/` — Specific algorithms or hacks (code samples welcome)
- `History/` — Interview records, timelines, industry primary/secondary sources
- `Translations/` — Translations of existing articles (must link to the original)

If you're unsure where something belongs, open an Issue and ask before writing.

### `GameEngine/` Structure Rules

Engines are organized in two levels: **family** (engine lineage) → **generation**.

```
GameEngine/
  UnrealEngine/
    README.md      ← Overview of the whole family, key evolution points between generations
    UE1/
      README.md    ← Overview (release year, notable titles, source/tool availability, etc.)
      rendering.md ← Split into separate files by subtopic, e.g. rendering
      gameplay.md
    UE2/
      README.md
      ...
  idTech/
    README.md      ← Overview of the whole family
    idTech1/
    idTech2/
    idTech3/
    idTech4/
```

- The family-level `README.md` should only contain the overall overview and a "map of differences between generations" — put individual technical details in the generation folders instead
- Each generation folder should follow the same structure: `README.md` (overview) + one file per subtopic
- New engine families should follow this same two-level rule

## ✍️ Minimum Article Format

Please start each article with the following header:

```markdown
# Title

- Subject: (e.g. Famicom / Unreal Engine 3 / General)
- Era: (e.g. 1985–)
- Difficulty: Beginner / Intermediate / Advanced
- Source: (link or citation to book, interview, primary source)
```

## 🔍 Rules on Sourcing

- Prioritize primary sources (developers' own statements, contemporary technical documents)
- If using secondary sources, always include a link or full citation
- Information without a verifiable source is welcome, but must be clearly labeled "unconfirmed" — avoid stating it as fact

## 🚀 How to Contribute

1. If you have a topic to add, ideally open an Issue first with a short outline
   (submitting a PR directly is also fine)
2. Create a file in the appropriate `docs/` subfolder (use lowercase, hyphen-separated filenames, e.g. `famicom-sprite-limit.md`)
3. Write following the format above
4. Submit a Pull Request

## 🌐 About Translations

When submitting a translation, always include a link to the original text and clarify the copyright status (fair use excerpt, or permission obtained).

## 💬 Questions

If you're unsure about formatting or where something belongs, feel free to ask in Discussions or an Issue.
A submitted-but-imperfect article is welcome over a perfect one that never gets posted.

---

**Let's preserve video game technology together!**
