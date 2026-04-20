---
name: md-to-pptx
description: Convert a markdown chapter from the HoCE book into a summarized PowerPoint presentation using the EPAM template. Use this when the user asks to create a presentation, slides, or PowerPoint from a chapter or markdown file.
---

# Markdown Chapter to PowerPoint Presentation

Convert a book chapter (markdown) into a polished, summarized PowerPoint deck using the EPAM dark template.

## Core principle

This is **not** a conversion — it is a **summarization and redesign** for a presentation context. The chapter is long-form writing; the deck must be concise, scannable, and impactful. You are making editorial decisions about what belongs on a slide and what does not.

## Step 1 — Understand the inputs

The input is: $ARGUMENTS

Parse it to get the markdown file path. If none provided, ask the user.

Derive the output path by replacing the `.md` extension with `.pptx` and placing it in the same directory as the input file.

The script lives at: `.claude/skills/md-to-pptx/scripts/generate_pptx.py` relative to the project root.
The JSON plan is a file: same directory as the output, named `_slides_plan.json`. Keep the file in case we want to compare the plan to the final output for debugging or improvement.

## Step 2 — Read and analyze the chapter

Read the full markdown file. Identify:
- The **central thesis** (what is the one thing this chapter argues?)
- The **narrative arc** (how does the argument build?)
- **Key concepts** that need their own slide
- **Memorable quotes or bold statements** (marked with `**...**` in the markdown) — these become impact slides
- **Analogies or stories** that carry the argument (e.g. the keypuncher story)

## Step 3 — Design the slide plan

Design a deck of **12–18 slides** average. However, if there are more key concepts, or stories, or bold statements; I'd prefer deleting some extra slides that building them myself, so you may exceed this range by double with no problem. Apply these rules:

**Slide types and when to use them:**

| Layout | Use for |
|--------|---------|
| `Cover_Dark` | First slide only — chapter title + subtitle. Max 5 words for title, max 10 words for subtitle. |
| `Contents` | Second slide only — table of contents listing the main named slides (Subsection_Divider titles). Use `items` list of `{number, text}` pairs, up to 6. Each `text` must match the title of a `Subsection_Divider` slide in the deck. |
| `Subsection_Divider` | Section transitions — signals a new topic block. **These are the main sections listed in the Contents slide.** |
| `Quote_Large_Black` | Big quotes, bold statements, or the central thesis. The `quote` field holds the impactful text. Keep it under 10 words. |
| `Title+Small_Text` | Content slides with bullet points. Max 5 bullets. Each bullet max 10 words. Optional `subtitle` adds small text below. |
| `Title Only` | Title + optional short section label. **Has no body area** — do NOT use for paragraph or bullet content. Use `Title+Small_Text` instead. Reserve for standalone title moments or visual breaks. |
| `Our_People_1_Person_White` | Story/example slide built around a real-world scenario from the chapter — use when the chapter uses a concrete person or role as an illustrative example (e.g. the keypuncher, a developer archetype, a case study character). `name` holds the character/role label, `job_title` the one-line context, `body` the narrative (3–4 sentences max, fits ~2.8" tall). Right half is a visual placeholder not filled by the script. |
| `Thank_you` | Last slide only, no body |

**Editorial rules:**
- Every slide must earn its place — cut anything that is supporting detail rather than a key idea
- Bullets must be crisp takeaways, not sentences copied from the chapter
- Impact slides (`Quote_Large_Black`) should punch — use the chapter's own bold-marked statements when they are strong enough
- Prefer fewer slides with stronger content over more slides with diluted content
- The deck must work as a standalone communication — someone who hasn't read the chapter should understand the argument
- Do not add the folder name or "HoCE" anywhere in the deck — this is a presentation about the chapter's content
- Always include a `Contents` slide as slide 2 (after `Cover_Dark`). Its `items` must list the titles of all `Subsection_Divider` slides in the deck, in order, numbered sequentially
- `Title Only` has **no body placeholder** — never assign paragraph or bullet content to it. Use `Title+Small_Text` for any slide that needs content below the title

## Step 4 — Produce the JSON slide plan

Write the JSON plan to `_slides_plan.json`. Format:

```json
{
  "slides": [
    {
      "layout": "Cover_Dark",
      "title": "The Best Programming Language for the AI Era",
      "subtitle": "How Spec-Driven Development changes the game",
      "label": "APRIL 2026"
    },
    {
      "layout": "Contents",
      "title": "Contents",
      "items": [
        { "number": "01", "text": "The Key Puncher Parallel" },
        { "number": "02", "text": "The Paradigm Inversion" },
        { "number": "03", "text": "Three Developer Shapes" },
        { "number": "04", "text": "Spec-Driven Development" }
      ]
    },
    {
      "layout": "Quote_Large_Black",
      "title": "",
      "quote": "The machine understands human language now.",
      "label": "The paradigm shift"
    },
    {
      "layout": "Title+Small_Text",
      "title": "The Key Puncher Parallel",
      "body": [
        "- In the 70s, key punchers were essential — 12,000 keystrokes/hour",
        "- COBOL arrived and their role became obsolete",
        "- Today's developers face the same inflection point",
        "- AI makes coding faster → smaller teams → fewer seats"
      ],
      "subtitle": ""
    },
    {
      "layout": "Subsection_Divider",
      "title": "Three Developer Shapes",
      "subtitle": "Which one survives the AI era?"
    },
    {
      "layout": "Our_People_1_Person_White",
      "section_title": "A REAL-WORLD EXAMPLE",
      "name": "The Keypuncher",
      "job_title": "12,000 keystrokes/hour — the gold standard of 1970",
      "body": "When COBOL arrived, keypunchers didn't disappear overnight. Their craft still had value — but the craft itself had been redefined. The skill that took years to master was now a commodity. Today's developer faces the same moment: not obsolescence, but redefinition."
    },
    {
      "layout": "Thank_you",
      "name": "Edgar Alvarez",
      "job_title": "Head of Core Engineering",
      "email": "edgar_alvarez1@epam.com"
    }
  ]
}
```

**Field rules:**
- `title`: string (slide headline, keep short)
- `subtitle`: string (secondary line, optional)
- `body`: array of strings (bullets) or single string (paragraph) — **not valid for `Title Only`**
- `quote`: string (impact text for `Quote_Large_Black` slides only)
- `label`: string (small category label, optional)
- `items`: array of `{number, text}` objects for `Contents` slides only — up to 6; `number` is a zero-padded string like `"01"`, `text` matches the corresponding `Subsection_Divider` title exactly
- `section_label`: string for `Title Only` — short label shown in the small top-left box (max 5 words)
- `section_title`: string (small top-left label for `Our_People_1_Person_White` — max 4 words, all caps)
- `name`: string (character/role label for `Our_People_1_Person_White`, or presenter name for `Thank_you`)
- `job_title`: string (one-line context for `Our_People_1_Person_White` — fits ~5.1" wide single line; or job title for `Thank_you`)
- `email`: string for `Thank_you` slide only (pre-filled with Edgar Alvarez's details)
- All fields are optional except `layout`

## Step 5 — Run the script

Find the project root (directory containing `.claude/`). Run:

```
python "<project-root>/.claude/skills/md-to-pptx/scripts/generate_pptx.py" "<path-to/_slides_plan.json>" "<output.pptx>"
```

Always quote paths to handle spaces.

## Step 6 — Clean up and report

Delete the temporary `_slides_plan.json` file.

Report:
- Output file path
- Number of slides generated
- Brief summary of the deck structure (e.g. "1 cover + 3 section dividers + 8 content slides + 1 closing")
- Note any editorial decisions worth flagging (e.g. "I condensed the I/T/M-shaped section into one slide — let me know if you want it expanded")
