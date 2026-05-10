# Beamer Template — Gruvbox Dark Theme

A customized Beamer presentation template with the **Gruvbox Dark** color scheme, Chinese support, and matching code highlighting.

## Features

- **Theme**: Based on the Madrid theme with extensive customizations
- **Color Scheme**: Full Gruvbox Dark palette (background `#282828`, foreground `#ebdbb2`, accent colors)
- **Dark Mode**: Complete dark background with carefully selected contrast for readability
- **Chinese Support**: Full `ctex` integration for Chinese documents
- **Code Highlighting**: Pre-configured `listings` package with Gruvbox-matched colors
- **Algorithms**: `algorithm` and `algpseudocode` packages ready to use
- **Bibliography**: `biblatex` with Biber backend configured
- **Auto-framing**: Custom `autoframe` environment using section/subsection titles
- **Enhanced Blocks**: Normal, Alert, and Example blocks all styled with Gruvbox colors

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

## Gruvbox Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Background | Dark bg0 | `#282828` |
| Background (alt) | Dark bg1 | `#3c3836` |
| Foreground | Light fg1 | `#ebdbb2` |
| Red (alert) | Bright Red | `#fb4934` |
| Green (example) | Bright Green | `#b8bb26` |
| Yellow | Bright Yellow | `#fabd2f` |
| Blue | Bright Blue | `#83a598` |
| Purple | Bright Purple | `#d3869b` |
| Aqua | Bright Aqua | `#8ec07c` |
| Orange | Bright Orange | `#fe8019` |

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

The template produces a professional dark presentation with:
- Gruvbox dark background with warm foreground text
- Custom section numbering in table of contents (aqua/blue circles)
- Rounded blocks with shadows in matching dark tones
- Customized itemize bullets per level (aqua → blue → purple)
- Professional header/footer via infolines outer theme
- Matching code blocks with full Gruvbox syntax highlighting

## License

Feel free to use and modify for your own presentations.
