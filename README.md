# poojakannanv.github.io

Personal portfolio site for **Pooja Kannan** &mdash; Full-Stack Developer based in Basildon, UK.

Live at: **https://poojakannanv.github.io/**

## Tech stack

This is a zero-build, zero-dependency static site:

- **HTML5** with semantic sectioning
- **Modern CSS3** (custom properties, Grid, Flexbox, `clamp()`, `color-mix()`, `backdrop-filter`)
- **Vanilla JavaScript** (no framework, no bundler)
- **Inline SVG** icons and favicon
- **Google Fonts**: Inter, Fraunces, JetBrains Mono
- **JSON-LD** structured data for search engines
- **Open Graph + Twitter Card** meta for link previews

Hosted on **GitHub Pages** at the root user URL (no build step, no Actions required).

## File map

```
poojakannanv.github.io/
  index.html        Single-file portfolio (HTML + inline CSS + inline JS)
  404.html          Custom 404 page
  assets/
    og-image.svg    1200x630 social preview image
  .nojekyll         Tells GitHub Pages to skip Jekyll processing
  .gitignore        Standard ignores
  README.md         You are here
  DEPLOY.md         Step-by-step deploy instructions
```

## Local preview

Just open `index.html` in any modern browser. No build, no server needed.

If you prefer a proper local server (cleaner for testing relative paths), from the project root:

```bash
# Python 3
python -m http.server 8000
# Then visit http://localhost:8000
```

## Deploying

See [DEPLOY.md](./DEPLOY.md) for the full git push and GitHub Pages walkthrough.

## Editing content

All copy lives directly in `index.html`. The sections are clearly marked with comment banners:

- `<!-- ============ NAV ============ -->`
- `<!-- ============ HERO ============ -->`
- `<!-- ============ ABOUT ============ -->`
- `<!-- ============ SKILLS ============ -->`
- `<!-- ============ PROJECTS ============ -->`
- `<!-- ============ CAREER TIMELINE ============ -->`
- `<!-- ============ EDUCATION / CERTS / LEARNING ============ -->`
- `<!-- ============ CONTACT ============ -->`

To change colours, edit the `:root` CSS variables at the top of the `<style>` block.

## License

All content (copy, design) &copy; 2026 Pooja Kannan. The code is available for inspiration; please don't redistribute the personal content.
