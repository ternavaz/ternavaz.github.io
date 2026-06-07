# Notes & Reflections

A simple, hand-maintained blog built with [Jekyll](https://jekyllrb.com/) and
hosted on GitHub Pages. Writing focuses on theology, psychology and the social
sciences.

**Live site:** https://ternavaz.github.io

## Writing a new post

1. Create a file in `_posts/` named `YYYY-MM-DD-title.md`.
2. Add front matter at the top, then write in Markdown:

   ```markdown
   ---
   layout: post
   title: "Your title here"
   date: 2026-06-06 09:00:00 +0000
   categories: [Theology]      # one or more of: Theology, Psychology, Social Sciences
   tags: [optional, keywords]
   ---

   Your content here…
   ```

3. Commit and push. GitHub Pages rebuilds the site automatically.

That's it — no build step required to publish.

## Customising

Open `_config.yml` and edit:

- `title`, `tagline`, `description` — shown in the header and sidebar.
- `author`, `email` — used in the footer and About page.
- `github_username`, `mastodon_url`, `rss` — sidebar links (leave blank to hide).
- `categories_list` — the topics shown in the navigation and sidebar.

To change colours, edit the variables at the top of
[`assets/css/style.css`](assets/css/style.css).

## Project layout

```
_config.yml            Site settings
_layouts/              Page templates (default, post, page, category)
_includes/sidebar.html The sidebar widgets
_posts/                Your blog posts (Markdown)
categories/            One page per topic
assets/css/style.css   All styling
index.html             Home page (paginated post list)
about.md               About page
```

## Previewing locally (optional)

You don't need this to publish, but to preview before pushing:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

On Linux you may hit an inotify watch-limit error (`Errno::ENOSPC`). If so,
run without the file watcher:

```bash
bundle exec jekyll serve --no-watch
```