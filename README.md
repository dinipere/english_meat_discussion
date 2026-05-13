# English Meat Discussion

Slidev test presentation for an English discussion about meat consumption.

## Start

```bash
npm install
npm run dev
```

Then open `http://localhost:3040/`, or the local URL printed by Slidev.

## Open Without the Dev Server

Slidev itself is a small web app, so the interactive presentation is meant to run through a local server. Double-clicking `slides.md` or `dist/index.html` is not reliable.

For a real file you can open directly, export to PDF:

```bash
npm run export:pdf
```

If Slidev asks for Playwright, install it once:

```bash
npm install -D playwright-chromium
```

Alternative while the dev server is running: open `http://localhost:3040/export/` and export the PDF in the browser.

## Project Structure

- `slides.md` is the deck index. It imports every slide in order.
- `slides/` contains one Markdown file per slide.
- `layouts/` contains simple Slidev layouts that turn plain Markdown into designed slides.
- `styles/design.css` contains the central design variables.
- `style.css` applies those variables to Slidev layouts and reusable classes.

## Writing Slides

The slide files are intentionally plain Markdown. You usually only need:

```md
---
layout: apple-cards
---

## Small label

# Slide title

- **Card title**
  Card text goes here.
```

Use these layouts:

- `apple-cover` for the title slide
- `apple-default` for normal text and bullet slides
- `apple-cards` for two-by-two card slides
- `apple-stats` for three large key points
- `apple-quote` for one central question plus cards
- `apple-table` for Markdown tables
- `apple-stakeholders` for stakeholder lists
- `apple-steps` for numbered process slides
- `apple-vocab` for vocabulary lists
- `apple-closing` for the final question slide

## Change Font Sizes

Open `styles/design.css` and edit these values:

```css
--fs-title: 2.55rem;
--fs-body: 1.02rem;
```

The same file also controls colors, card radius, shadows, and smaller type sizes.

## Working Together on GitHub

This structure is meant to reduce merge conflicts. One person can edit `slides/07-position-keep.md` while another edits `slides/08-position-reduce.md`. The only file that needs coordination is `slides.md`, because it controls the slide order.
