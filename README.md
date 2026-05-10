# Beamer Template — Gruvbox Light Theme

A customized Beamer presentation template with the **Gruvbox Light** color scheme, Chinese support, and matching code highlighting.

## Features

- **Theme**: Based on the Madrid theme with extensive customizations
- **Color Scheme**: Full Gruvbox Light palette (background `#fbf1c7`, foreground `#3c3836`, accent colors)
- **Light Mode**: Warm paper-like background with carefully selected contrast for readability
- **Chinese Support**: Full `ctex` integration for Chinese documents
- **Code Highlighting**: Pre-configured `listings` package with Gruvbox-matched colors
- **Algorithms**: `algorithm` and `algpseudocode` packages ready to use
- **Bibliography**: `biblatex` with Biber backend configured
- **Auto-framing**: Custom `autoframe` environment using section/subsection titles
- **Enhanced Blocks**: Normal, Alert, and Example blocks all styled with Gruvbox colors
- **Clean Title Page**: Author, institute, and date displayed without background boxes

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

## Gruvbox Light Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Background | Light bg0 | `#fbf1c7` |
| Background (alt) | Light bg1 | `#ebdbb2` |
| Foreground | Dark fg1 | `#3c3836` |
| Red (alert) | Soft Red | `#9d0006` |
| Green (example) | Soft Green | `#79740e` |
| Yellow | Soft Yellow | `#b57614` |
| Blue | Soft Blue | `#076678` |
| Purple | Soft Purple | `#8f3f71` |
| Aqua | Soft Aqua | `#427b58` |
| Orange | Soft Orange | `#af3a03` |

## Custom Commands

- `\emphblue{text}` — Blue bold emphasis
- `\emphred{text}` — Red bold emphasis
- `\emphgreen{text}` — Green bold emphasis
- `\empyellow{text}` — Yellow bold emphasis
- `\emppurple{text}` — Purple bold emphasis
- `\empaqua{text}` — Aqua bold emphasis
- `\emporange{text}` — Orange bold emphasis
- `eblock` environment — Custom tcolorbox with Gruvbox theme colors
- `autoframe` environment — Frame that auto-uses section/subsection titles

## Preview

The template produces a professional light presentation with:
- Gruvbox light warm paper background with dark foreground text
- Custom section numbering in table of contents (aqua/blue circles)
- Rounded blocks with shadows in matching light tones
- Customized itemize bullets per level (aqua → blue → purple)
- Professional header/footer via infolines outer theme
- Matching code blocks with full Gruvbox syntax highlighting
- Clean title page: title/subtitle in a light box, author/institute/date without background boxes

## License

Feel free to use and modify for your own presentations.
