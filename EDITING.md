# How to edit this site

The public site is https://bhuvanmakes.github.io, built from this repository. You change a file here (or on github.com), and after a minute or two GitHub Pages updates the live site for free.

Every project and any piece of writing lives at `/projects/your-slug/`. There is no separate blog. The home-page list is sorted by date, newest first. Use the Instructables publish date when there is one, or the video's upload date for a video article.

## The 9-part kit (standing rule)

Every Bhuvan Makes project should go out with all of the following. When we start, discuss, or publish a project, we check this list and note whatever is still missing:

1. Website article (the page in `_projects/`)
2. Instructable
3. Medium blog
4. 4–5 progress tweets
5. 3–4 Instagram update reels
6. 1 long documentary YouTube reference video
7. 4–5 short, well-edited, high-reach videos
8. 1 GitHub repository (under github.com/bhuvanmakes only)
9. 1 open-access or other research paper

Fill the matching front-matter fields as each piece goes up. The project page only shows the links that are set. Hardware write-ups should start from `_templates/hardware-project.md` (see below).

## Add a project

1. For a hardware project, copy `_templates/hardware-project.md` to `_projects/<slug>.md`. For a short video article, a simpler page with `title`, `date`, `hero`, `youtube`, `tags` and the write-up is enough.
2. Fill in the front matter (the bit between `---` lines), then write the page in ordinary Markdown underneath.

```yaml
---
title: The name people will see
date: 2026-10-26
summary: One short line used if you don't write an intro.
intro: >-
  Two or three sentences for the home-page list.
lede: Optional short line at the top of the project page.
hero: /assets/img/your-slug/cover.jpg
hero_alt: A short description of the photo.
hero_credit: Optional, for example where the photo was first published.
instructable: https://www.instructables.com/your-write-up/
medium:
github:
youtube:           # a YouTube video ID, for example dQw4w9WgXcQ
arxiv:
paper:
tags:
  - Arduino
  - 3D printing
---
```

`date` controls the home-page order (newest first).

`intro` is the short paragraph on the home page. If you leave it out, the list uses `summary` instead.

A project or article shows on the home page when it is published (`published` is not `false`) and lives in `_projects/`. If a project is not ready, set `published: false` or move the file into `_unpublished/` so it stays in the repo but off the public site, the sitemap and the site feed. Unpublished work, and anything still without a public write-up or video, should stay hidden.

`youtube` is optional. Put the video's ID (the part after `v=` in the YouTube link), and the project page will embed the video. A full YouTube URL also works.

`tags` is optional. These show as small quiet labels, in the same spirit as Instructables categories (for example Arduino, or 3D printing).

`medium`, `instructable`, `github`, `arxiv` / `paper` and the other kit fields are further reading. The page only shows the ones you fill in.

The usual recommendation is a cover photo plus a YouTube embed. You can also copy a fuller Instructables write-up onto the project page if you like, as long as the images are compressed (see below).

## Hardware project template

`_templates/hardware-project.md` is the starting point for hardware documentation. It follows an Instructables-style structure: Intro, Supplies (a BOM table), Tools, numbered Steps (each with an image placeholder), Code / Files, Results, What's next, Credits, and Further reading, plus front matter for the cover, video, tags, status, and the usual links (Instructable, Medium, GitHub, paper, credits / collaborators). The `_templates/` folder is excluded from the site build.

## Photos

Put a project's images in `assets/img/<slug>/`, for example `assets/img/algaesense/cover.jpg`, and point `hero` at that path.

Resize photos to about 1600 pixels on the long side, and keep each file under about 300 KB (JPEG is usually best). That keeps the site fast, and it also keeps you comfortably inside GitHub's free Pages hosting. A cover image is enough for most projects. If you want the full Instructables picture set on the page, that's fine too, as long as those images are compressed the same way.

The circular picture at the top of the home page is a placeholder until you add a profile photo (replace `assets/img/placeholder-portrait.svg`). The tab icon is a yellow letter B on black (with white counters) at `assets/favicon.svg` and `assets/favicon.png`. There is also an Apple touch icon at `assets/apple-touch-icon.png` and a 512-pixel version at `assets/favicon-512.png`. Swap these files if you later want a different logo.

## Site-wide settings

A few things live in `_config.yml` instead of a project file:

- `about` — the intro text on the home page, under "About me,"
- `collab_url` — where the "Let's collaborate? :)" button and the footer Collaborate link go. It is a placeholder until you add a Google Form (or other) URL
- `instagram_url` and `donate_url` — leave these empty to keep Instagram and Patreon hidden in the footer; paste a URL to show them
- `links` — the other footer links (GitHub, Instructables, Hackaday, YouTube, X)

Don't add an email address or a `mailto:` link, and don't add LinkedIn. Project code links should be `github.com/bhuvanmakes/...` only, once those repos are public.

## After you edit

If you're changing the repo on GitHub, commit the file and wait for Pages to rebuild. If you're previewing on a computer:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000. The generated `_site/` folder can be deleted; GitHub Pages will build its own copy.
