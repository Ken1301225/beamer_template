# Beamer Template — Gruvbox Light Theme

A customized Beamer presentation template with the **Gruvbox Light** color scheme, Chinese support, and matching code highlighting.

## Features

- **Theme**: Based on the Madrid theme with extensive customizations
- **Color Scheme**: Authentic Gruvbox Light palette extracted from the official color card
- **Light Mode**: Warm paper-like background (`#f9f5d7`) with high-contrast foreground (`#413829`)
- **Chinese Support**: Full `ctex` integration for Chinese documents
- **Code Highlighting**: Pre-configured `listings` package with Gruvbox-matched colors
- **Algorithms**: `algorithm` and `algpseudocode` packages ready to use
- **Bibliography**: `biblatex` with Biber backend configured
- **Auto-framing**: Custom `autoframe` environment using section/subsection titles
- **Left-Accent Blocks**: Clean block style with colored vertical accent lines — no backgrounds, no shadows

## Authentic Gruvbox Light Palette

Extracted directly from the official Gruvbox color card:

| Role | Color | Hex |
|------|-------|-----|
| Background (bg0) | Warm paper | `#f9f5d7` |
| Background (bg1) | Light beige | `#f5edca` |
| Background (bg2) | Beige | `#f3eac7` |
| Background (bg3) | Soft tan | `#f2e5bc` |
| Background (bg4) | Tan | `#eee0b7` |
| Background (bg5) | Deep tan | `#ebdbb2` |
| Foreground (fg0) | Dark brown | `#5a4735` |
| Foreground (fg1) | Deep brown | `#413829` |
| Red | Muted red | `#c14a4a` |
| Orange | Warm orange | `#c55e0a` |
| Yellow | Golden yellow | `#b47109` |
| Green | Olive green | `#6c782e` |
| Aqua | Sage green | `#4c7a5d` |
| Blue | Steel blue | `#45707a` |
| Purple | Dusty purple | `#945e80` |
| Grey0 | Warm grey | `#a89984` |
| Grey1 | Medium grey | `#928374` |
| Grey2 | Dark grey | `#7c6f64` |

## Usage

1. Edit the title information in `main.tex`:
   ```latex
   \title{Your Title}
   \author{Your Name}
   \institute{Your Institution}
   \date{\today}
   ```

2. Add your references to `ref.bib`.

3. Compile with XeLaTeX (required for `ctex`):
   ```bash
   xelatex main.tex
   biber main
   xelatex main.tex
   xelatex main.tex
   ```

## Page Color Hierarchy

The page is architected with clear layers to avoid the "one big beige blob" problem:

```
┌─ Header (bg5 #ebdbb2, deep tan) ───────────────┐  ← ~8% area
══ Aqua bottom line ══════════════════════════════
│ Frametitle (transparent, dark text)             │  ← ~4% area
│ ── bg4 thin line ────────────────────────────── │
│                                                  │
│   │ Block Title (colored bold, no bg)           │  ← Blocks: ~12% area
│   │ ─────────────                               │     transparent bg
│   │ Content here...                             │
│   │                                              │
│                                                  │
│ ── bg4 top line ─────────────────────────────── │
├─ Footer (bg3 #f2e5bc, soft tan) ───────────────┤  ← ~6% area
└──────────────────────────────────────────────────┘
    ↑ Page background bg0 #f9f5d7 (~70% area)
```

| Region | Background | Purpose |
|--------|-----------|---------|
| Page | `bg0 #f9f5d7` | Main content area, lightest |
| Header | `bg5 #ebdbb2` | Top navigation bar, darkest bg |
| Footer | `bg3 #f2e5bc` | Bottom info bar, medium depth |
| Frametitle | Transparent | Avoids merging with header |
| Block | Transparent | No extra color blocks, lines only |

## Block Design — Left Accent Line

All three block types share a unified minimal aesthetic:

```
│  Block Title              ← bold colored text, no background
│  ───────────────          ← 1pt colored separator line
│  Content here...          ← body text, transparent background
│  More content...
│                           ← 3pt colored vertical line on the left
```

- **No background fill** — block body is transparent, blending with the page
- **No border, no shadow, no rounded corners** — pure lines
- **Left accent line** — 3pt thick vertical line in block-specific color:
  - Normal: dark brown `#5a4735`
  - Alert: red `#c14a4a`
  - Example: green `#6c782e`
- **Title** — bold text matching the left line color, no background box
- **Separator** — 1pt thin line under the title, color-matched but semi-transparent

## Custom Commands

- `\emphblue{text}` — Blue bold emphasis
- `\emphred{text}` — Red bold emphasis
- `\emphgreen{text}` — Green bold emphasis
- `\empyellow{text}` — Yellow bold emphasis
- `\emppurple{text}` — Purple bold emphasis
- `\empaqua{text}` — Aqua bold emphasis
- `\emporange{text}` — Orange bold emphasis
- `eblock` environment — Custom left-accent tcolorbox
- `autoframe` environment — Frame that auto-uses section/subsection titles

## Preview

The template produces a professional light presentation with:
- Authentic Gruvbox warm paper background with dark brown text
- Clear page hierarchy via header/footer color bands
- Clean left-accent blocks with no background clutter
- Custom section numbering in table of contents (aqua/blue circles)
- Customized itemize bullets per level (aqua → blue → purple)
- Matching code blocks with Gruvbox syntax highlighting
- Clean title page: title/subtitle in a light box, author/institute/date without background boxes

## License

Feel free to use and modify for your own presentations.
