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
- **Card-style Blocks**: Normal, Alert, and Example blocks styled as soft rounded cards with diffused shadows

## Authentic Gruvbox Light Palette

Extracted directly from the official Gruvbox color card:

| Role | Color | Hex |
|------|-------|-----|
| Background (bg0) | Warm paper | `#f9f5d7` |
| Background (bg1) | Light beige | `#f5edca` |
| Background (bg2) | Beige | `#f3eac7` |
| Background (bg3) | Soft tan | `#f2e5bc` |
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

## Block Design — Soft Card Style (方案 C)

All three block types share a unified card aesthetic:

- **Large rounded corners** (`8pt` arc) — soft and friendly
- **No visible border** (`boxrule=0pt`) — clean and modern
- **Diffused shadow** — subtle elevation, color-tinted to match block type:
  - Normal block: warm tan shadow
  - Alert block: warm red-tinted shadow
  - Example block: warm green-tinted shadow
- **Title with colored text** — no background box, just bold colored text
- **1pt separator line** under the title — thin, color-matched divider
- **Light beige card background** (`#f5edca`) — slightly warmer than the slide background

## Preview

The template produces a professional light presentation with:
- Authentic Gruvbox warm paper background with dark brown text
- Custom section numbering in table of contents (aqua/blue circles)
- Soft card-style blocks with colored shadows and separator lines
- Customized itemize bullets per level (aqua → blue → purple)
- Professional header/footer via infolines outer theme
- Matching code blocks with Gruvbox syntax highlighting
- Clean title page: title/subtitle in a light box, author/institute/date without background boxes

## License

Feel free to use and modify for your own presentations.
