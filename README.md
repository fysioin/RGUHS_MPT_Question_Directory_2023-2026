# RGUHS MPT - Master Question Directory (Papers I-IV, 2023-2026)

An interactive, accessible HTML study tool built from the **RGUHS Master of Physiotherapy (MPT)**
**Master Question Directory - Papers I, II, III & IV** (RS-4 Syllabus), covering the six latest
exam sittings: **Nov 2023, May 2024, Nov 2024, May 2025, Nov 2025 & May 2026**.

The whole resource is a **single self-contained HTML file** - no build step, no dependencies, no
internet connection required. Just open it in a browser.

## What it contains

- **4 papers, 40 topics, 178 questions**, grouped paper-wise into high-yield core topics.
- Each topic shows its **exact examination sittings** and the **total number of repetitions** (a badge).
  High-frequency clusters carry the highest probability of recurrence.
- **Term popups** - difficult words are dotted-underlined; hover or tap for a plain-English definition.
- **Glossary** of every difficult term used, at the foot of the page.

| Paper | Title | Q.P. Code |
| --- | --- | --- |
| I | Fundamentals in Physiotherapy Practice, Pedagogy & Research | 8129 |
| II | Fundamental Principles of Musculoskeletal Physiotherapy | 8130 |
| III | Physical and Functional Diagnosis in Musculoskeletal Disorders | 8131 |
| IV | Physiotherapy Interventions in Musculoskeletal Disorders | 8132 |

## Files

| File | Purpose |
| --- | --- |
| `RGUHS_MPT_Question_Directory_2023-2026.html` | The interactive study page (open this). |
| `index.html` | Minimal landing page used by the GitHub Pages site. |
| `README.md` | This documentation. |

## Components

### 1. Toolbar (sticky, top)
Minimal, monochrome by default. Contains: three highlight swatches, **Erase**, **Clear all**,
**Term notes** (toggles the popup underlines), **Night mode**, **Fit to screen**, and a
**Paper** filter - **All / Paper I / Paper II / Paper III / Paper IV** - that shows one paper's
topics at a time (the choice is remembered between visits).

### 2. Paper blocks and topic sections (`.card > .paper-head`, `section.q`)
A `.paper-head` divider introduces each paper. Each topic is one `<section class="q">` with a heading
row (plus its notes pill), a repetition-count badge, its sittings line, and the numbered question list.

### 3. Term popups (`.term[data-note]`)
Every difficult word is wrapped in `<span class="term" data-note="...">`. Hovering or tapping shows a
plain-English definition in a floating popup. Definitions also appear in the collapsible **glossary**
at the foot of the page.

### 4. Study Notes (auto-saving)
Two synced entry points, both saved automatically in the browser:

- **Floating "Study Notes" button** (bottom-right, always visible) opens a slide-out drawer listing
  every topic with its own notes box. A badge shows how many topics have notes.
- **Notes pill on each topic heading** opens a notes box beside the topic (wide screens) or under the
  heading (narrow screens). When a topic has no notes, it collapses to a small numbered button.

### 5. Night mode
A light/dark toggle; the choice is remembered. Both themes meet contrast expectations for body text.

### 6. Fit to screen
Toggles between a comfortable reading width and full-window width; remembered between visits.

### 7. Highlighting
Select text, then click a colour swatch (yellow / green / pink). **Erase** removes highlights in the
selection; **Clear all** removes every highlight.

### Storage keys
All user data is stored locally in the browser (nothing is uploaded), namespaced to this directory so
it does not mix with other papers on the same site:

- `rguhsQDir-highlights` - your highlights
- `rguhsQDir-note-qN` - notes for topic N
- `rguhsQDir-theme` - `dark` / `light`
- `rguhsQDir-fit` - `1` / `0`

## Accessibility

- Semantic headings (`h1`-`h4`), and real ordered lists.
- Interactive controls are native `<button>` elements with `aria-expanded` / `aria-controls` on the
  notes toggles and `aria-live` on the save status.
- Term popups are keyboard reachable (`tabindex="0"`, opened with Enter/Space, dismissed with Escape).
- Readable default font size, generous line height, and a print stylesheet (toolbar, popups and the
  notes UI are hidden when printing).

## Regenerating / editing

The HTML is generated from the source question directory text. To change the content, edit the source
and re-run the generator; to tweak the look, edit the `<style>` block at the top of the HTML. The CSS
uses variables (`--bg`, `--ink`, `--accent`, ...) so the palette can be changed in one place.

## Definitions and sources

Definitions are written in plain English to explain the directory's terminology, drawing on standard
physiotherapy references and the concepts named in the questions themselves. They are study aids, not
quotations.

## Disclaimer

Study aid only - a compiled question directory, not an official university publication, and not a
substitute for the current syllabus or clinical judgement.
