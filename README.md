# Communication in Science

Website for [communicationinscience.com](https://communicationinscience.com) — expert writing support for biomedical researchers and health professionals publishing in English-language journals.

## Built With

- [Jekyll](https://jekyllrb.com/) — static site generator
- [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) — theme by Dean Attali
- [GitHub Pages](https://pages.github.com/) — hosting and deployment

## Site Structure

```
.
├── index.html          # Homepage (hero, services, CTA)
├── services.md         # Services overview
├── workshops.md        # Workshops page
├── editing.md          # Editing services page
├── tutorials.md        # Online tutorials page
├── about.md            # About page
├── contact.md          # Contact page
├── _config.yml         # Site configuration (title, nav, author)
├── _layouts/
│   ├── home.html       # Full-width layout for homepage
│   └── page.html       # Standard content page layout
├── css/
│   └── main.css        # Site styles (theme + CIS custom styles)
└── img/                # Images and logos
```

## Updating Content

All content pages are Markdown files in the root directory. Edit them directly — GitHub Pages rebuilds the site automatically on every push to `master`.

Each page begins with YAML front matter:

```yaml
---
layout: page
title: Page Title
subtitle: A short subtitle
---
```

After the `---`, write standard Markdown.

### Adding a New Page

1. Create a `.md` file in the root (e.g. `resources.md`)
2. Add the front matter above
3. Add a link in `_config.yml` under `navbar-links` if it should appear in navigation

## Configuration

Key settings in `_config.yml`:

| Setting | Purpose |
|---------|---------|
| `title` | Site name shown in the browser tab |
| `description` | Site tagline |
| `navbar-links` | Navigation menu items and dropdown structure |
| `author.email` | Contact email shown in the footer |
| `url` | Full site URL (used for canonical links) |

## Local Development

Requires Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000` in your browser.

Alternatively, use Docker:

```bash
docker build -t cis-site .
docker run -p 4000:4000 cis-site
```

## Deployment

Pushing to `master` triggers an automatic GitHub Pages build. The site is live at [communicationinscience.com](https://communicationinscience.com) within a minute or two.

## Contact

[jonathan@communicationinscience.com](mailto:jonathan@communicationinscience.com)
