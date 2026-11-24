# Bhuvan Makes

Personal site for [Bhuvan Makes](https://bhuvanmakes.github.io), built with Jekyll so GitHub Pages can compile it from the default branch. There is no custom GitHub Actions workflow and no heavy JavaScript framework.

This copy was prepared locally. It has no Git remote yet. Do not create the GitHub repository, push, or change GitHub settings until access to the **bhuvanmakes** account is available and Bhuvan has said to publish.

## Pages

- `/` — landing page (intro, featured projects, writing, about)
- `/projects/` — all featured projects
- `/projects/algaesense/`, `/projects/morse-monkey/`, `/projects/besos/`, `/projects/small-beacon/`
- `/blog/` — post list
- `/blog/algaesense/` — published AlgaeSense write-up
- Drafts in `_drafts/` (Morse Monkey, BESOS, Small Beacon) are not built unless you pass `--drafts`

Public identity is **Bhuvan Makes** only. There is no LinkedIn link. OpenExG-C5, AirCalibre and GoodOne are not on this site.

## Local preview

You need Ruby 3, Bundler, and (the first time) a network connection to install gems.

```bash
cd bhuvanmakes.github.io   # or this folder, /workspace/portfolio/site
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000>. The compiled site is written to `_site/`, which is generated and can be deleted.

To preview unpublished drafts as well:

```bash
bundle exec jekyll serve --drafts
```

## How to publish (once bhuvanmakes access exists)

Do these steps only after Bhuvan grants access to the **bhuvanmakes** GitHub account and asks for the site to go live. The box `gh` CLI may still be signed in as another account; switch or authenticate as **bhuvanmakes** first. Do not push from the wrong account.

1. Sign in as `bhuvanmakes`. Confirm with `gh api user --jq .login`.
2. Create a **public** repository named exactly `bhuvanmakes.github.io` on that account (empty, no README or licence from the GitHub form, so this tree can be pushed as-is).
3. In this folder:

   ```bash
   git remote add origin git@github.com:bhuvanmakes/bhuvanmakes.github.io.git
   git branch -M main
   git push -u origin main
   ```

4. On the repository's Settings → Pages, set the source to **Deploy from a branch**, branch **main**, folder **/ (root)**. GitHub Pages will run Jekyll itself. Do not add a `.nojekyll` file.
5. Wait for the Pages build, then check <https://bhuvanmakes.github.io>.
6. Optional later: replace `assets/img/placeholder-portrait.svg` with the shared profile photograph once Bhuvan supplies it, and fill empty kit fields (see below) as each piece is published.

No custom domain is required. Do not reuse the existing `bhuvanmakes/portfolio` PDF repository as this site.

## Adding a project or a blog post

Projects live in `_projects/` and use the `project` layout. Posts live in `_posts/` as `YYYY-MM-DD-slug.md` and use the `post` layout. Work-in-progress writing goes in `_drafts/` until it is ready.

Copy the front matter below. Keep list fields as YAML lists. **Leave a field out, or leave it empty, if you do not yet have a real, published URL.** The templates only render kit links that exist, so empty fields will not show a broken link.

```yaml
---
title: Project name
# projects only:
# order: 5
# status: In progress
# summary: One sentence used on cards and lists.
# posts only: the date comes from the filename.
lede: Optional short introduction.
hero: /assets/img/projects/example.jpg
hero_alt: Describe the picture.
hero_credit: Optional credit, including the source and date.

# Content kit — fill only verified, published links
instructable:     # one URL, or leave empty
hackster:         # optional extra write-up
tweets:           # list of URLs, or omit
  # - https://x.com/Maker_Bhuvan/status/...
youtube:          # one long video URL
instagram_updates:
  # - https://www.instagram.com/p/...
shorts:
  # - https://www.youtube.com/shorts/...
arxiv:            # one paper URL
# TODO: Set `github` only after the repo is public at
# https://github.com/bhuvanmakes/<repo-name>
# Do not link github.com/bhuvanbagwe — those repositories are private
# and the URLs now 404.
github:
blog:             # path on this site, e.g. /blog/example/
---
```

Then write the body in Markdown. Use only real, published facts. Label anything planned as planned. Do not invent measurements, awards or subscriber counts.

Add a project photograph under `assets/img/projects/` if you have an honest picture of the built hardware. Use the typographic card placeholder if you do not.

After adding a post, it appears on `/blog/` and on the home page. After adding a project file, it appears on `/projects/` and, if you set `order`, in the featured grid on the home page.

## GitHub links

The header, footer and landing-page buttons link to the public profile <https://github.com/bhuvanmakes>.

Project and post `github` kit fields are intentionally empty until each repository is published under that account. When a repo goes public, add its `https://github.com/bhuvanmakes/...` URL to the matching project page and blog post, then rebuild.

## Portrait

`assets/img/placeholder-portrait.svg` is a temporary monogram. Bhuvan is taking a new photograph to use on this site and on the other public profiles. Do not invent a portrait.
