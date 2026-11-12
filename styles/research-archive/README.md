# Research Archive

**English · [中文说明](README.zh-CN.md)**

Version 1.1.0

A warm, precise visual direction for research portfolios, software indexes, project documentation, and technical personal sites. It combines the visual conventions of a research record—fields, dates, indexes, and tabular metadata—with a restrained software palette.

The style is intentionally not a glassmorphic AI dashboard, a beige lifestyle editorial, or a collection of rounded cards. Structure comes from aligned text and rules, not shadows.

## Files

- `tokens.css`: color, typography, spacing, borders, layout, and motion variables.
- `tokens.json`: equivalent decisions for SVG generators, slide tools, and other non-CSS media.
- `components.css`: optional record grids, index rows, labels, and buttons.
- `preview.html`: standalone style guide with CN/EN language controls and system, light, and dark modes.
- `assets/cover.svg`: catalog and social preview artwork.

## Core palette

| Role | Light | Dark | Use |
| --- | --- | --- | --- |
| Page | `#E8E7E1` | `#151712` | Canvas outside the primary surface |
| Paper | `#FFFFFF` | `#20231C` | Main reading surface; blends into GitHub's native light canvas |
| Wash | `#F7F6F0` | `#20231C` | Warm information bands and selected record groups |
| Ink | `#292C26` | `#E9E9DF` | Headings and primary text |
| Muted | `#5F6459` | `#B4B7AA` | Descriptions and secondary values |
| Faint | `#6A6F64` | `#A2A797` | Small labels and metadata |
| Line | `#D2D2C6` | `#3C4135` | Internal separators |
| Strong line | `#A7AA9C` | `#646B58` | Outer frame and major divisions |
| Accent | `#A94F36` | `#D98565` | One data point, index, arrow, or focus state |

Core text and accent combinations against Paper and Wash start at 4.76:1 in the light theme and 5.68:1 in the dark theme. Recheck contrast when changing a value.

## Typography

- **Display:** Archivo Medium. Tight tracking, moderate weight, no faux bold.
- **Body:** IBM Plex Sans Regular, with Noto Sans SC for Chinese narrative text. Comfortable line height and a roughly 65-character reading measure.
- **Utility:** IBM Plex Mono Regular/Medium. Uppercase labels, dates, indexes, and technical metadata.

The preview loads these families from Google Fonts. The tokens include real fallback stacks. For deterministic SVG rendering, convert finished text to outlines and retain meaningful `<title>`, `<desc>`, and image alt text.

## Web usage

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500;600&display=swap">
<link rel="stylesheet" href="tokens.css">
<link rel="stylesheet" href="components.css">
```

Set `data-theme="light"` or `data-theme="dark"` on the root element for an explicit choice. With no attribute, the style follows the operating system.

```html
<section class="ra-surface">
  <p class="ra-label">01 / Research</p>
  <h1 class="ra-display">Health data, working software.</h1>
</section>
```

## SVG and GitHub usage

Use the values in `tokens.json` as SVG custom properties. A self-contained asset can adapt to the viewer's theme:

```xml
<style>
  svg { --paper: #FFFFFF; --wash: #F7F6F0; --ink: #292C26; }
  @media (prefers-color-scheme: dark) {
    svg { --paper: #20231C; --wash: #20231C; --ink: #E9E9DF; }
  }
</style>
```

Use a separate mobile composition through `<picture>` rather than shrinking a dense desktop asset. Keep each linked project as its own image and provide a plain-text fallback. Do not put the only copy of essential information inside an unlabeled image.

## Composition rules

1. Start with the information record: name, field, current status, and selected work.
2. Use one-pixel rules and generous spacing instead of elevated cards.
3. Keep corners square or nearly square. Avoid generic pills and floating glass panels.
4. Use the terracotta accent sparingly. It should identify a value or action, not paint the page.
5. Use numbers for a real index, sequence, or chronology—not as decoration.
6. Keep metadata readable. Ten pixels is a floor for final SVG labels, not a target for every caption.
7. Let longer descriptions wrap; never compress them with reduced font size.

## Where it fits

Research and engineering portfolios, selected-project indexes, technical CVs, documentation covers, lab or studio sites, and data-aware editorial pages.

For high-emotion consumer branding, playful illustration, dense analytics dashboards, or interfaces that depend on semantic status colors, choose another direction or extend this one deliberately.
