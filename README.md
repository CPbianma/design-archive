# Design Archive

**English · [中文说明](README.zh-CN.md)**

A growing collection of reusable visual directions for portfolios, technical documentation, software interfaces, and presentations. Each style is self-contained: copy one package without inheriting a framework or a build step.

![Research Archive style cover](styles/research-archive/assets/cover.svg)

## Catalog

| Style | Character | Includes | Preview |
| --- | --- | --- | --- |
| [Research Archive](styles/research-archive/) | Warm neutrals, precise rules, technical metadata, editorial spacing | CSS + JSON tokens, components, light/dark themes, responsive examples | [Open](styles/research-archive/preview.html) |

## Use this repository

Choose **Use this template** on GitHub, or clone it and copy the style package you need.

```sh
git clone https://github.com/CPbianma/design-archive.git
```

Open `styles/research-archive/preview.html` in a browser. The preview includes CN/EN language controls and system, light, and dark theme controls. It works without a local server.

For a web project, import the tokens before the components:

```html
<link rel="stylesheet" href="styles/research-archive/tokens.css">
<link rel="stylesheet" href="styles/research-archive/components.css">
```

For SVG, slides, or non-CSS tools, use `tokens.json`. The same color roles and type scale apply across media.

## Repository structure

```text
styles/
└── research-archive/
    ├── assets/cover.svg
    ├── components.css
    ├── tokens.css
    ├── tokens.json
    ├── preview.html
    └── README.md
catalog.json
CONTRIBUTING.md
```

Every directory under `styles/` is a complete visual direction. Personal names, project links, and other client-specific content belong in examples, not in reusable tokens or components.

## Design principles

- Define color by role rather than by component name.
- Give both themes the same care; do not simply invert colors.
- Use a small type system with distinct display, body, and utility roles.
- Prefer spacing and alignment over decorative containers.
- Keep the core free of frameworks and runtime dependencies.
- Check keyboard focus, reduced motion, mobile layout, and text contrast before publishing a style.

## Add a new direction

See [CONTRIBUTING.md](CONTRIBUTING.md) for the package contract and review checklist. New styles should describe a reusable category, not a one-off client or task.

## Applied example

The Research Archive direction powers [Peng Cai's GitHub Profile](https://github.com/CPbianma). Its SVG assets use the same color roles and typography, with fonts converted to outlines for deterministic rendering.

## License

[MIT](LICENSE)
