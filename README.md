# Beamer Template — Warm Card Style

A modern Beamer presentation template inspired by warm minimalist card-based slide design.

## Features

- **Theme**: Clean warm-white base (`#F5F0EB`) with brick-red (`#C84B31`) accents
- **Card Design**: Rounded white cards with subtle shadows — matching modern web/PPT aesthetics
- **Highlight Cards**: Red background cards with white text for emphasis
- **Large Title**: Left-aligned `
\LARGE` frametitle with subtitle support
- **Minimal Navigation**: Thin red top line + simple page number footer — no cluttered headers
- **Chinese Support**: Full `ctex` integration
- **Code Highlighting**: Warm-toned syntax highlighting
- **Tag/Badge Commands**: Small colored label badges
- **Bibliography**: `biblatex` with Biber backend

## Color Palette

| Role | Hex | Usage |
|------|-----|-------|
| Page background | `#F5F0EB` | Warm off-white, main slide area |
| Card background | `#FFFFFF` | White card fill |
| Primary text | `#2C2C2C` | Main body text |
| Secondary text | `#6B6B6B` | Subtitles, descriptions |
| Accent red | `#C84B31` | Highlights, alert blocks, top line |
| Divider line | `#E8E3DE` | Card title separator |
| Shadow | `#D5D0CB` | Card drop shadow |

## Usage

1. Edit the title information in `main.tex`:
   ```latex
   \title{Presentation Title}
   \author{Your Name}
   \institute{Your Institution}
   \date{\today}
   ```

2. Add your references to `ref.bib`.

3. Compile with XeLaTeX:
   ```bash
   xelatex main.tex
   biber main
   xelatex main.tex
   xelatex main.tex
   ```

## Page Design

```
═══════════════════════════════════════════  ← 2.5pt red top line
│
│ Title Here                ← \LARGE bold, left-aligned
│ Subtitle description...   ← normal size, gray
│
│ ┌─────────────────┐ ┌──────────────┐
│ │ Card Title      │ │ Red Card     │
│ │ ─────────────   │ │ ──────────── │
│ │ Content...      │ │ Content...   │
│ └─────────────────┘ └──────────────┘
│
│ 1 / 8                     ← page number, bottom-left
```

## Block Styles

### White Card (Normal Block)
```latex
\begin{block}{Card Title}
    Content here...
\end{block}
```
- White background (`#FFFFFF`)
- 6pt rounded corners
- Subtle drop shadow
- Title + thin gray separator line

### Red Highlight Card (Alert Block)
```latex
\begin{alertblock}{Highlighted Title}
    Content here...
\end{alertblock}
```
- Red background (`#C84B31`)
- White text
- 6pt rounded corners
- Red-tinted shadow

### Green Title Card (Example Block)
```latex
\begin{exampleblock}{Example Title}
    Content here...
\end{exampleblock}
```
- White background with green title

## Side-by-Side Cards (Columns)

```latex
\begin{columns}[t]
    \begin{column}{0.24\textwidth}
        \begin{block}{Title}
            Content...
        \end{block}
    \end{column}
    \begin{column}{0.24\textwidth}
        \begin{alertblock}{Highlight}
            Content...
        \end{alertblock}
    \end{column}
\end{columns}
```

## Custom Commands

- `\tagred{text}` — Small red badge with white text
- `\taggray{text}` — Small gray badge with dark text
- `\emphred{text}` — Red bold emphasis
- `\emphgreen{text}` — Green bold emphasis
- `\emphblue{text}` — Blue bold emphasis
- `eblock` environment — White rounded card
- `redcard[title]` environment — Red rounded card

## Comparison with Previous Themes

| | Gruvbox | Catppuccin | **This Theme** |
|--|---------|-----------|---------------|
| Base | Yellow paper | Cool white | **Warm cream** |
| Accent style | Muted | Vibrant | **Brick red** |
| Block shape | Left line | Left line | **Rounded cards** |
| Header | Navigation bar | Navigation bar | **Minimal red line** |
| Feel | Retro terminal | Modern tech | **Warm minimalism** |

## License

Feel free to use and modify for your own presentations.
