# CLAUDE.md

This is a Jekyll-based personal website/linktree for Josef Adamčík hosted at https://adamcik.me.

## Tech Stack

- **Framework**: Jekyll 4.3.0 (static site generator)
- **Language**: Ruby (gem-based dependencies)
- **Styling**: SCSS/SASS with Basscss utility framework
- **Asset Pipeline**: jekyll-assets with autoprefixer and uglifier
- **Deployment**: GitHub Actions → GitHub Pages

## Common Commands

```bash
# Install dependencies
bundle install

# Serve locally with drafts (development)
bundle exec jekyll serve --watch --drafts
# or equivalently:
rake preview

# Production build
JEKYLL_ENV=production bundle exec jekyll build --baseurl "/"
```

## Content Creation

```bash
rake post['My Post Title']   # Create a new dated blog post
rake draft['My Draft Title'] # Create a new draft (no date in filename)
rake list                    # List available rake tasks
```

## Project Structure

```
_assets/css/        # SCSS source files (partials prefixed with _)
_includes/          # Reusable HTML partials
_layouts/           # Page layout templates
assets/             # Static/compiled assets (fonts, icons)
_config.yml         # Jekyll configuration (site metadata, plugins, social links)
Rakefile            # Task automation
```

## Key Configuration

- Site metadata, social links, and plugin settings live in `_config.yml`
- SCSS variables and design tokens are in `_assets/css/_variables.scss`
- The site uses the Pixyll theme (modified); the MIT license applies to theme/code but NOT to `_posts/`

## Notes

- Generated output goes to `_site/` (gitignored)
- No explicit linting configuration exists; follow existing code style
- Image optimization is available via image_optim but disabled by default in `_config.yml`
