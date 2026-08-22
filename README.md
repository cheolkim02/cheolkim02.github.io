# cheolkim02.github.io

Personal research site. Plain HTML and CSS — no build step, no JavaScript, no web fonts.

## Deploy

1. Create a repository on GitHub named exactly **`cheolkim02.github.io`**.
2. Copy these files into it (`index.html` must be at the repository root).
3. Add your CV as `assets/Cheol_Kim_CV.pdf`.
4. Commit and push to the `main` branch.
5. Repository → **Settings** → **Pages** → Source: *Deploy from a branch* → Branch: `main`, folder: `/ (root)` → Save.

Live at `https://cheolkim02.github.io` within a minute or two. Every push updates it.

To preview locally: `python3 -m http.server` in this folder, then open `http://localhost:8000`.

## Before publishing — checklist

**Permissions first.** Both project pages carry flags about this. Do not publish either until resolved.

- [ ] Ambiguity page cleared with Prof. Lee and your co-author. Do not post the manuscript PDF without explicit approval — the work may still go to a double-blind venue.
- [ ] Wezon page checked against the confidentiality terms. Assume the partner name, schema, and any data-derived figure are restricted until told otherwise.

**Content.** Every red block on the site is a placeholder. Search the HTML for `class="todo"` — there should be zero left when you publish.

- [ ] Homepage intro rewritten in your own words (highest priority)
- [ ] Worked example of an ambiguous question added
- [ ] Design reasoning written — why the method is shaped the way it is, and what failed
- [ ] Limitations section written
- [ ] Dataset-building difficulties written
- [ ] Pipeline diagram checked against what you actually built
- [ ] Coverage figure added, if permitted
- [ ] Third project considered — something in the lab's area

**Housekeeping.**

- [ ] `assets/Cheol_Kim_CV.pdf` added and matching the version you send by email
- [ ] GitHub account has something real on it, or the link is removed
- [ ] DIAL Lab URL in `index.html` verified
- [ ] "Last updated" date correct in all three footers
- [ ] Opened on a phone on mobile data — no horizontal scroll, fast load
- [ ] Someone technical but outside your subfield read it and could explain your method back to you

## Editing

`style.css` holds the whole design. The variables at the top control colour and type:

- `--accent` — the one accent colour, used for links and diagram fills
- `--measure` — prose column width; keep it near 34rem so lines stay at 60–75 characters
- `--serif` / `--mono` — serif for prose, monospace for structured metadata (dates, roles, labels)

The `.todo` block styling can be deleted from the CSS once every placeholder is gone.
