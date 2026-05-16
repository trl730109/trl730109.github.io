# trl730109.github.io

Personal homepage of Zichen Tang. Built with Jekyll using a hand-written minimal layout (no themes, no `academicpages`).

## Running locally

Requires Ruby ≥ 3.0 (Jekyll 4.x). On macOS:

```sh
brew install ruby
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
bundle install
bundle exec jekyll serve --port 4080
```

Then open <http://127.0.0.1:4080/>.

## Editing content

- **Home / About** — `_pages/about.md` (bio paragraph, links).
- **News** — `_data/news.yml` (newest first; markdown supported in `content`).
- **Publications** — one Markdown file per paper under `_publications/`. Front-matter fields:
  - `title`, `authors` (use `**Zichen Tang**` to bold your own name),
    `year`, `date` (ISO), `venue`, `status`,
    `selected: true` to surface on the home page,
    optional `note` and `links: [{label, url}, …]`.
- **Teaching** — one Markdown file per role under `_teaching/`.
- **CV** — table entries on `_pages/cv.md`; the PDF lives at `files/CV_TANG_Zichen.pdf`.
- **Layout / styles** — `_layouts/`, `_includes/`, `_sass/`.

## Layout structure

```
_layouts/
  default.html   shell (head + main + footer)
  page.html      generic page with H1 title
  home.html      landing page with name banner / news / selected pubs
_includes/
  head.html      meta + stylesheet link
  footer.html    text-nav footer
  publication-item.html
_sass/
  _tokens.scss   colors, type, layout sizes
  _reset.scss
  _base.scss     typography
  _home.scss
  _publications.scss
  _pages.scss
  _footer.scss
  _dark.scss     follows `prefers-color-scheme`
assets/css/style.scss   entry point
```

## Deployment

The repo is configured for plain Jekyll 4 (not the legacy `github-pages` gem). For GitHub Pages we need a GitHub Actions workflow that runs `jekyll build` and publishes `_site/` — to be added when the redesign is merged to `master`.
