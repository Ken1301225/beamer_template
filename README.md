# Beamer Template — Catppuccin Latte Theme

A customized Beamer presentation template with the **Catppuccin Latte** color scheme, Chinese support, and matching code highlighting.

## Features

- **Theme**: Based on the Madrid theme with extensive customizations
- **Color Scheme**: Full Catppuccin Latte palette — crisp cool-white base with vibrant accents
- **Light Mode**: Clean off-white background (`#EFF1F5`) with high-contrast foreground (`#4C4F69`)
- **Chinese Support**: Full `ctex` integration for Chinese documents
- **Code Highlighting**: Pre-configured `listings` package with Catppuccin-matched colors
- **Algorithms**: `algorithm` and `algpseudocode` packages ready to use
- **Bibliography**: `biblatex` with Biber backend configured
- **Auto-framing**: Custom `autoframe` environment using section/subsection titles
- **Left-Accent Blocks**: Clean block style with colored vertical accent lines — no backgrounds, no shadows

## Catppuccin Latte Color Palette

### Neutrals

| Role | Color | Hex |
|------|-------|-----|
| Base (page bg) | Off-white | `#EFF1F5` |
| Mantle (header) | Pale gray | `#E6E9EF` |
| Crust (footer) | Light gray | `#DCE0E8` |
| Surface 0 | Mid gray | `#CCD0DA` |
| Text (body) | Dark blue-gray | `#4C4F69` |
| Subtext 1 (titles) | Medium dark | `#5C5F77` |
| Subtext 0 (secondary) | Medium | `#6C6F85` |
| Overlay 0 (accent line) | Light gray | `#9CA0B0` |

### Accents

| Role | Color | Hex |
|------|-------|-----|
| Blue (structure) | Pure blue | `#1E66F5` |
| Green (example) | Vibrant green | `#40A02B` |
| Red (alert) | Bright red | `#D20F39` |
| Yellow | Golden yellow | `#DF8E1D` |
| Mauve (purple) | Rich purple | `#8839EF` |
| Teal | Teal | `#179299` |
| Peach (orange) | Bright orange | `#FE640B` |

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

```
┌─ Header (mantle #E6E9EF) ───────────────────────┐
══ Blue #1E66F5 bottom line ═══════════════════════
│ Frametitle (transparent, dark text)               │
│ ── Surface0 thin line ────────────────────────── │
│                                                    │
│   │ Block Title (colored bold, no bg)             │
│   │ ─────────────                                 │
│   │ Content here...                               │
│                                                    │
│ ── Surface0 top line ───────────────────────────  │
├─ Footer (crust #DCE0E8) ─────────────────────────┤
└────────────────────────────────────────────────────┘
    ↑ Page background base #EFF1F5
```

| Region | Background | Purpose |
|--------|-----------|---------|
| Page | `base #EFF1F5` | Main content area, clean off-white |
| Header | `mantle #E6E9EF` | Top navigation bar |
| Footer | `crust #DCE0E8` | Bottom info bar |
| Frametitle | Transparent | Ultra clean, no background bar |
| Block | Transparent | No extra color blocks, lines only |

## Block Design — Left Accent Line

```
│  Normal Block Title     ← dark text, no background
│  ───────────────        ← 1pt gray separator
│  Content here...        ← body text, transparent bg
│
│  Alert Block Title      ← red #D20F39 bold text
│  ─────────────────      ← 1pt red separator
│  Content...
│
│  Example Block Title    ← green #40A02B bold text
│  ───────────────────    ← 1pt green separator
│  Content...
│                           ← 3pt colored vertical line
```

- **No background fill** — transparent, blending with the page
- **No border, no shadow, no rounded corners** — pure lines
- **Left accent line** — 3pt thick vertical line:
  - Normal: overlay0 `#9CA0B0`
  - Alert: red `#D20F39`
  - Example: green `#40A02B`
- **Title** — bold text matching the left line color
- **Separator** — 1pt thin line under the title

## Custom Commands

- `\emphblue{text}` — Blue `#1E66F5` bold
- `\emphred{text}` — Red `#D20F39` bold
- `\emphgreen{text}` — Green `#40A02B` bold
- `\empyellow{text}` — Yellow `#DF8E1D` bold
- `\emppurple{text}` — Mauve `#8839EF` bold
- `\empaqua{text}` — Teal `#179299` bold
- `\emporange{text}` — Peach `#FE640B` bold
- `eblock` environment — Custom left-accent tcolorbox
- `autoframe` environment — Frame that auto-uses section/subsection titles

## Why Catppuccin over Gruvbox?

- **No yellow tint** — base `#EFF1F5` is a clean cool white, not aged paper
- **Higher contrast accents** — blue `#1E66F5`, red `#D20F39`, green `#40A02B` pop against the background
- **Modern feel** — crisp, young, suitable for both academic and product presentations
- **Excellent code highlighting** — mauve keywords, green strings, gray comments on clean white

## License

Feel free to use and modify for your own presentations.
