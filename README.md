# cheolkim02.github.io

Personal academic homepage. Static HTML and CSS — no Jekyll, no build step, no JavaScript beyond a portrait fallback.

Layout follows [luost26/academic-homepage](https://github.com/luost26/academic-homepage): sticky profile sidebar on the left, sectioned content on the right.

```
index.html      About / Education / Experience / Honors / Selected Research / Selected Projects
research.html   Ambiguity Resolution for Text-to-SQL, in full
projects.html   Text-to-SQL for Manufacturing Databases, in full
style.css       whole design system
assets/         portrait, figures, CV — add these yourself
```

## Deploy

1. Create a GitHub repository named exactly **`cheolkim02.github.io`**.
2. Copy these files in, with `index.html` at the root.
3. Add your files to `assets/` (see below).
4. Push to `main`.
5. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.

Live at `https://cheolkim02.github.io` within a minute or two.

Preview locally with `python3 -m http.server`, then open `http://localhost:8000`.

## Assets to add

| Path | What |
|---|---|
| `assets/portrait.jpg` | Square headshot, ~600×600. Plain and friendly. Placeholders show until it exists. |
| `assets/Cheol_Kim_CV.pdf` | Same PDF you attach to emails. |
| `assets/ambiguity.png` | Pipeline figure, 3:2. |
| `assets/nl2sql.png` | Coverage/similarity plot, 3:2 — only if confidentiality allows. |

Institution badges are CSS circles with initials, so nothing to download. To use real logos instead, drop an image inside the badge span:

```html
<span class="badge badge--skku"><img src="assets/badges/skku.png" alt=""></span>
```

## Before publishing

**Permissions first.** Both detail pages carry a flag about this.

- [ ] Research page cleared with Prof. Lee and your co-author. No manuscript PDF without explicit approval — the work may still go to a double-blind venue.
- [ ] Projects page checked against the confidentiality terms. Partner name, schema, and data-derived figures restricted until you're told otherwise.

**Content.** Search the HTML for `class="todo"` — every one is a placeholder, and there should be zero left when you publish.

- [ ] Research-goal sentence on the homepage rewritten in your own words
- [ ] Physical AI interest block either backed by a project or removed
- [ ] Worked example of an ambiguous question written
- [ ] "Why the method is shaped this way" written — highest-value section on the site
- [ ] Limitations written
- [ ] Dataset-building difficulties written
- [ ] Honors section filled out or deleted
- [ ] A third project added, ideally in the lab's area

**Housekeeping.**

- [ ] Portrait, CV and figures added to `assets/`
- [ ] GitHub has something real on it, or the icon link is removed
- [ ] "Last updated" correct on all three pages
- [ ] Opened on a phone on mobile data
- [ ] Someone technical but outside your subfield read it and could explain the method back

## Editing

Tokens are at the top of `style.css`. The badge colours (`.badge--skku`, `--dial`, `--sds`, `--scis`, `--mhs`) are set there too.

Adding an experience entry:

```html
<div class="item">
  <span class="badge badge--skku">SKKU</span>
  <div class="item-b">
    <div class="org">Organisation. City, Country</div>
    <div class="adv">Advised by Prof. Name</div>
    <div class="role">Your title</div>
  </div>
  <div class="when">Mon. YYYY ‑ Mon. YYYY</div>
</div>
```

Adding a research or project card: copy a `.pub` block. Keep `<span class="me">Cheol Kim</span>` so your own name stays bold in author lists, and keep the `.status` label on anything unpublished.
