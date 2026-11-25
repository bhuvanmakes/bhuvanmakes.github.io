# How to edit this site

Once this folder is on GitHub as the `bhuvanmakes.github.io` repository, GitHub Pages will build the site for free. You change a file in the repo, and after a minute or two the public site updates. You can edit here with me, or you can open the files on github.com and change them yourself.

There is no separate blog. Writing counts as a project and shows up in the same list on the home page.

## Add a project

1. In `_projects/`, add a new file named something short, like `morse-monkey.md` or `novella.md`.
2. Start the file with a front matter block (the bit between `---` lines), then write the page in ordinary Markdown underneath.

```yaml
---
title: The name people will see
order: 5
summary: One short line for the home-page list.
status: in progress
hero: /assets/img/projects/your-photo.jpg
hero_alt: A short description of the photo.
hero_credit: Optional, for example where the photo was first published.

# Links — leave a line out, or leave it empty, until the URL is real and public.
instructable:
hackster:
tweets:
youtube:
instagram_updates:
shorts:
arxiv:
# github: only use a github.com/bhuvanmakes/... URL, once that repo is public
github:
blog:
---
```

`order` controls where the item sits in the home-page list. Lower numbers come first (1, 2, 3…).

`status` is optional. If you set it, it shows as a small quiet word next to the title, for example `draft` or `in progress`. Skip it when the project is simply done.

`summary` is a short one-line description. `intro` is the two or three sentence paragraph shown on the home-page list; if you leave it out, the list uses `summary` instead.

`hero` is the thumbnail on the home page and a modest photo on the project page. Skip it if you don't have a picture yet.

`blog` is optional. If you also write a longer article (see below), put its path here, like `/blog/algaesense/`. The home-page title will then jump straight to that article, and the article won't also appear as a second row in the list.

The other link fields are the content kit. The page only shows the ones you fill in, so empty ones stay hidden.

## Add a longer write-up

1. In `_posts/`, add a file named `YYYY-MM-DD-short-name.md`, for example `2026-11-24-algaesense.md`. The date in the filename is the published date.
2. Use the same kind of front matter as a project (`title`, `lede` or `summary`, `hero`, and any kit links). You do not need `order`.
3. Write the article under that block.

A write-up that already belongs to a project should be linked from that project's `blog:` field, as above. A standalone piece of writing — for example the novella, when you're ready — can be a project file in `_projects/`, or a post in `_posts/` with a `summary` so it appears in the home-page list on its own. You don't need a special novella template. Just add it like any other entry, and link the about-page mention later if you want.

Work that isn't ready to publish can live in `_drafts/` with the same front matter. Drafts only show up if the site is built with `--drafts`, so they stay off the public site.

## Photos

Put images in `assets/img/projects/` and point `hero` at `/assets/img/projects/your-photo.jpg`.

A photo around 1200 to 1600 pixels on the long side, saved as a JPEG, is plenty. Try to keep each photo under about 300 KB so the page stays quick. You don't need huge cover images; the home page only shows a small square thumbnail.

Use a real photo of the work when you have one. The circular picture at the top of the home page is a placeholder until you add a profile photo (replace `assets/img/placeholder-portrait.svg`).

## Site-wide settings

A few things live in `_config.yml` instead of a project file:

- `about` — the intro text on the home page
- `collab_url` — where the "Wanna collaborate? :)" button and the footer Collaborate link go. It is a placeholder until you add a Google Form (or other) URL
- `instagram_url` and `donate_url` — leave these empty to keep Instagram and Patreon/Donate hidden in the footer; paste a URL to show them
- `links` — the other footer links (GitHub, Instructables, Hackaday, YouTube, X)

Don't add an email address or a `mailto:` link, and don't add LinkedIn. Project code links should be `github.com/bhuvanmakes/...` only, once those repos are public.

## After you edit

If you're changing the repo on GitHub, commit the file and wait for Pages to rebuild. If you're previewing on a computer:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000. The generated `_site/` folder can be deleted; GitHub Pages will build its own copy.
