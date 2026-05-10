# Beamer Template

A customized Beamer presentation template with a blue-gray color scheme, Chinese support, and code highlighting.

## Features

- **Theme**: Based on the Madrid theme with extensive customizations
- **Color Scheme**: Custom blue (`#5b668e`) and gray (`#d8d2c3`) palette
- **Chinese Support**: Full `ctex` integration for Chinese documents
- **Code Highlighting**: Pre-configured `listings` package with custom colors
- **Algorithms**: `algorithm` and `algpseudocode` packages ready to use
- **Bibliography**: `biblatex` with Biber backend configured
- **Auto-framing**: Custom `autoframe` environment using section/subsection titles

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

- `\emphblue{text}`: Emphasize text in blue bold
- `\emphred{text}`: Emphasize text in red bold
- `eblock` environment: Custom tcolorbox with theme colors
- `autoframe` environment: Frame that auto-uses section/subsection titles

## Preview

The template produces a clean, professional presentation with:
- Custom section numbering in table of contents
- Rounded blocks with shadows
- Customized itemize bullets per level
- Professional header/footer via infolines outer theme
