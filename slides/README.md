# Slide Files

Each real slide lives in this folder. The root `slides.md` file only decides the order.

Write the slide body as plain Markdown. Avoid manual HTML such as `<div>` or `<p>` unless there is a very specific reason.

Recommended workflow for two people:

1. Pick different slide files before editing.
2. Keep one idea per slide.
3. Put source notes in HTML comments until the final source slide exists.
4. Rename slides with a two-digit prefix when the order changes.

To add a slide:

1. Create a new file, for example `14-sources.md`.
2. Add a matching block to `../slides.md`:

```md
---
src: ./slides/14-sources.md
---
```

Example slide:

```md
---
layout: apple-default
---

## Position A

# Meat should remain normal

Short intro sentence.

- **Culture:** One useful argument.
- **Nutrition:** Another useful argument.
```
