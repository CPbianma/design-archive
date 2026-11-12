# Adding a visual direction

A new direction should be reusable across more than one project. Name it after its visual category or character, such as `research-archive`, `industrial-manual`, or `soft-structuralism`, rather than after a person or a single deliverable.

## Required package

Create `styles/<style-slug>/` with:

```text
assets/cover.svg   # 1200 × 630 repository/catalog cover
tokens.css         # Complete light and dark CSS custom properties
tokens.json        # The same decisions for non-CSS media
preview.html       # A standalone, responsive style guide
README.md          # Intent, usage, rules, and anti-patterns
README.zh-CN.md    # Recommended when the style has a Chinese audience
```

Add `components.css` when the direction has reusable web patterns. Keep example-specific markup out of the token files.

Also add the style to:

1. The catalog table in the root `README.md`.
2. The `styles` array in `catalog.json`.
3. The root `index.html` catalog.

## Design review checklist

- [ ] The palette defines background, surface, text, muted text, lines, and one clear accent.
- [ ] Light and dark palettes are both intentional and readable.
- [ ] Normal-sized text reaches at least 4.5:1 contrast.
- [ ] Display, body, and utility type roles are explicit, with real fallback stacks.
- [ ] The preview works at approximately 400 px without horizontal scrolling.
- [ ] Interactive examples have visible keyboard focus and respect reduced motion.
- [ ] All example content is real or clearly identified as a sample; no lorem ipsum or invented metrics.
- [ ] The core has no framework requirement and no hidden runtime service.
- [ ] External assets are limited to documented font hosting or are stored locally.
- [ ] The README explains where the style works and where it does not.

## Keep styles independent

Do not rename or rewrite an existing direction merely to accommodate a new idea. Add a new package instead. Small refinements can use the version field in `tokens.json`; document breaking token renames in the style README.

Fonts Archivo, IBM Plex Sans, and IBM Plex Mono are used under the SIL Open Font License. Loading them from Google Fonts is optional; every package includes fallback stacks.
