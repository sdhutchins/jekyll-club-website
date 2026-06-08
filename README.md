# Jekyll Club Website Template

[![Deploy Jekyll to GitHub Pages](https://github.com/sdhutchins/jekyll-club-website/actions/workflows/deploy.yml/badge.svg)](https://github.com/sdhutchins/jekyll-club-website/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Jekyll](https://img.shields.io/badge/Jekyll-4.3-CC0000?logo=jekyll&logoColor=white)
![Bulma CSS](https://img.shields.io/badge/Bulma-CSS-00D1B2?logo=bulma&logoColor=white)

A ready-to-fork Jekyll website template for student organizations and clubs,
built with [Bulma CSS](https://bulma.io) and styled with
[UAB brand colors](https://www.uab.edu/brandguide/university/colors).

## Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [Customization](#customization)
- [Directory Structure](#directory-structure)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Authors](#authors)

## Features

- Modern, responsive design powered by Bulma CSS
- Mobile-friendly navbar with burger menu
- Homepage with hero section, upcoming events preview, and latest blog posts
- Events page driven by YAML data files (no code changes needed)
- Executive board page with card grid (driven by `_data/board.yml`)
- Blog with post tags, prev/next navigation, and pagination
- Resources and Contact pages
- SEO-optimized with `jekyll-seo-tag`
- Sitemap generation with `jekyll-sitemap`

## Quick Start

### 1. Fork or Use as Template

Click **"Use this template"** on GitHub (or fork the repo), then clone your
copy:

```sh
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cd YOUR-REPO
```

### 2. Install Dependencies

Requires Ruby >= 2.7 and Bundler (`gem install bundler`).

```sh
bundle install
```

### 3. Customize

Edit `_config.yml` to set your organization's name, description, and social
links. See [Customization](#customization) for details.

### 4. Serve Locally

```sh
bundle exec jekyll serve
```

Open <http://localhost:4000> in your browser.

## Customization

### Essential first steps after forking

1. **`_config.yml`** -- Update `title`, `description`, `email`, `url`, and
   `social` links. The top section is clearly marked with what to change.
2. **Logo** -- Replace `assets/img/logo-placeholder.svg` with your logo and
   update the `logo` path in `_config.yml`.
3. **Colors** -- Edit CSS variables in `assets/css/custom.css` to match your
   organization's brand. The default ships with a UAB theme based on
   the [official UAB Brand Guide](https://www.uab.edu/brandguide/university/colors).
4. **Board** -- Edit `_data/board.yml` with your members and add photos to
   `assets/img/`.
5. **Events** -- Edit `_data/upcoming-events.yml` and
   `_data/previous-events.yml`. Upcoming events can also include optional
   `resource_label` and `resource_url` fields for links such as tutorials,
   articles, or registration pages.
6. **Pages** -- Edit `about.md`, `resources.md`, `contact.md` with your
   content. Look for `<!-- Replace -->` comments.
7. **Posts** -- Delete the example posts in `_posts/` and add your own.

### Adding blog posts

Use standard Jekyll post front matter in `_posts/YYYY-MM-DD-title-slug.md`.
For posts, provide author names as separate first-name and last-name fields so
the site can render both the visible byline and the citation format from the
same source.

```yaml
---
layout: post
title: "Specific Article Title"
subtitle: "Optional one-sentence summary"
author_first_name: Nicola
author_last_name: Rennie
tags: [tag1, tag2]
comments: false
---
```

### Adding nav links

Edit the `nav_links` list in `_config.yml`. Add, remove, or reorder entries.

### Changing colors

Set your school or organization's colors directly in `_config.yml`:

```yaml
colors:
  primary: "#012169"   # main brand color (navbar, footer, hero, links)
  accent: "#F2A900"    # secondary color (buttons, highlights, accents)
  dark: "#00122e"      # dark variant (hero gradient, hover states)
```

The entire site adapts automatically. Some presets:

| School | primary   | accent    | dark      |
| ------ | --------- | --------- | --------- |
| UAB    | `#1A5632` | `#FDB913` | `#033319` |
| Emory  | `#012169` | `#F2A900` | `#00122e` |

### Changing fonts

Pick a site-wide font in `_config.yml`:

```yaml
font: "Poppins"
```

Available options: **Inter** (default), **Open Sans**, **Lato**,
**Poppins**, **Montserrat**. The font is loaded from Google Fonts
automatically.

## Directory Structure

```sh
jekyll-club-website/
├── _config.yml          <- Site configuration (start here)
├── _data/
│   ├── board.yml        <- Executive board members
│   ├── upcoming-events.yml
│   ├── previous-events.yml
│   └── social.yml       <- Social media links for footer
├── _includes/           <- Reusable HTML partials
├── _layouts/            <- Page layouts (default, home, page, post, board)
├── _posts/              <- Blog posts (Markdown)
├── assets/
│   ├── css/custom.css   <- Brand colors and style overrides
│   ├── img/             <- Images (logo, team photos)
│   └── pdfs/            <- Slide decks and documents
├── about.md
├── blog.html
├── contact.md
├── events.md
├── index.html
├── resources.md
├── the-board.md
├── Gemfile
├── CONTRIBUTING.md      <- Contribution guidelines
└── README.md
```

## Deployment

### GitHub Pages

1. Push your changes to the `main` branch
2. Go to **Settings > Pages** in your GitHub repo
3. Set **Source** to "GitHub Actions" or "Deploy from a branch" (`main`)
4. Your site will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`

### Custom Domain

Add a `CNAME` file to the repo root with your domain, and configure DNS per
[GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This template is open source. See [LICENSE](LICENSE) for details.

## Authors

- Shaurita D. Hutchins | [email](mailto:sdhutchins@uab.edu) | [sdhutchins](https://github.com/sdhutchins)
