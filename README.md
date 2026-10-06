# murtaza.github.io

Simple black-and-white site for About, blogs, and achievements.

Live URL after Pages is enabled:

https://murtazaa2010.github.io/murtaza.github.io/

## Write a new blog

1. Create a file in `_posts/`.
2. Name it `YYYY-MM-DD-short-title.md` (example: `2026-10-06-hello.md`).
3. Start the file with:

```yaml
---
layout: post
title: Your title
---
```

4. Write the post in Markdown under that block.
5. Commit and push to `main`.

## Update achievements

Edit `_data/achievements.yml`. Add a year block or an item under an existing year.

## Year links

The footer on every page links to each year on the Achievements page. Years are listed in `_config.yml` under `years`.

## Enable GitHub Pages

In the repo: **Settings → Pages → Source → GitHub Actions**.

The first push of this workflow may ask you to approve the `github-pages` environment.
